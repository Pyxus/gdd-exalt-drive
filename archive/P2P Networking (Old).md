# Resources

- https://godotforums.org/d/32987-understanding-rpcs-with-client-server/4

# Naming Conventions

- **request** - Called on client, executed on server
- **notify** - Called on server, executed on client

# Setting Up The Network

- `ENetMultiplayerPeer`: ENet is a peer implementation built on top of UDP. The peer will be used to create/connect to the desired server.
- `SteamPeer`: The steam peer is provided by the GodotSteam library and makes use of steam's relay server in addition to providing other steam integration functionality.
- `Enet` vs `SteamPeer`: For development the ENet should be used over steam as steam requires 2 separate computers to test. Enet can be swapped out for the steam peer with minimal refactoring at a later point. 
- `Node.multiplayer.multiplayer_peer = peer`:  All nodes have a reference to the same MultiplayerAPI. Setting the peer from any node essentially enables networking for the whole tree.
- `Scene Tree Parity`: Godot's high level multiplayer relies on node paths being identical on both the client and the server. Due to this you have to be mindful of the tree structure when communicating between clients
- `Network Singleton`: To make the tree parity easier to manage, and help with the separation of server and client I've moved all of my network related code to a network singleton. Each client will have an instance of this singleton meaning it can reliably serve as point of communication within Godot's multiplayer api. The network singleton will contain 3 things available to all clients:
	- `Service Getters`: The network can be split into multiple services to help organize code. Getters will be used for clients to reference these services.
	- `RPC Request functions`: RPC request functions will be what the client calls in order to make a change on the server. This is how the client will send information to the server.
	- `RPC Notification functions and signals`: RPC Notifications only exist to emit signals as signals can not be remotely emitted. When the server wants to communicate with the client it will invoke a notify function. This is how the server sends information to the client. These technically exist on the client, but they only execute on the client they are never called by the client. They are called by the server remotely.

# Separating Client and Server

- `Seperation of client and server`: Since this is a P2P setup, the server is technically a client and therefore a lot of server-only logic will also exist on the clients. To make the code easier to reason about I try to separate the client and server logic as much as possible going so far as to treat the client hosting the server as just another client.
- `Seperation of state`: Even though I'm just adding multiplayer to a simple card game I still implement things with cheating in mind. No one is likely to try cheating their friends but it's good practice to design things in a way where it would be difficult. For this reason the server should only inform the client about what is necessary. For instance in my card game the server knows both player's hand, but each player is only informed of their own hand.
- `ServerScope:` To help with separation of state and separation of client and server i've come up with a useful pattern I call "ServerScope". I create an inner class to contain all of the state and functions exclusive to the server. I then store an instance of this in a private variable in the network class, an instance which only the server creates. This doesn't provide any actual security, it just helps to visually separate code which is meant to only exists on the server. It also makes it difficult for me to accidently try to access something which only exists on the server. If I tried to the clients would get an error for trying to access a null value