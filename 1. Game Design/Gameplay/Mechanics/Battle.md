---
tags:
  - game-design
categories:
  - mechanics
description:
---
`=this.description`
> [!infobox]+
> # `=this.file.name`
> ![[Image.png|cover hsmall]]
> 
> | %%Empty%% |
> | ---- | ---- |
> ###### Section Info
> | %%Empty%% |
> | ---- | ---- |
> | Field | Value |

# Description

# Setup

1. Both players start in the 3rd and 7th spot
2. Both players start with the amount of life their character card indicates
3. A coin is flipped to decide who gets to choose who goes first
4. The first player draws 5 cards, the 2nd player draws 6 cards
5. Before the game starts each player has the option of setting aside any number of cards and then drawing the same amount set aside. The set aside cards are then shuffled back into the deck
6. The game is then started.

# Phases

- **Act Phase:** Turn player can perform any action.
- **Clash Phase:** Initiated by turn player; The aggressor must initiate with a card, the responder can choose to respond with a card.
- **Resolution Phase:** Occurs after a clash
- **End Phase:** If a clash did not occur this turn, the turn player draws a card.

# Resolving Clashes

When you initiate an clash you become the aggressor and your opponent the responder.

1. The aggressor sets their Attack card(s) face-down.
2. The responder can choose to set Attack card(s) face-down.
3. Both players reveal their attacks.
4. The attack with the higher speed goes first. 
	1. If there is a tie in speed the aggressor is prioritized.
	2. If one side plays a card defensively the offensive side the offensive card is prioritized.
	3. If both sides play a card defensively the clash is concluded
	4. If the aggressor plays a card defensively and the responder plays no card then the responder can choose to perform an **Uncontested Clash**.
5. For both players when their card is active:
	1. Check if you are staggered, if so skip remaining steps.
	2. Perform all **Before** effects
	3. Check Range to opponent from the attack's origin
	4. If the opponent is in Range, your attack hits. Perform all **Hit** effects if their condition is satisfied, then damage the opponent.
	5. Perform all **After** effects
	6. Perform all **Clash Win** / **Clash Loss** effects
6. After resolving both player's attacks trigger:
	1. Resolve any **Resolution** effects.
	2. Discard all unsustained enhance tactics
	3. If you hit your opponent even if it was guarded, add your attack card to your drive gauge.
7. Now it is the responder's turn unless the aggressor has advantage.
