---
tags:
  - game-design
---
**Title:** Exalt Drive
**Genre:** Turn-Based Strategy, PVP, Multiplayer, Card Battler, Roguelite Deckbuilder (CONSIDERING)
**Platforms:** PC

# Goal

My goal for this game is to convince people to pay me to draw characters. I'm half joking but I want to use this as an interesting way to use character concepts I've never had the chance to implement anywhere else because they were created for projects way out of my scope. With any luck if the project does well I'll be able fund projects including the characters people are most interested in. Worse case I make a game I can plan with friends while learning how to write netcode in the process.

# Pitch

- **This game is a:**  Strategic card battler that emulates the decision-making of a fighting game, where players navigate their options in order to outmaneuver their opponents with tactical precision.
- **Playing as:** Unique characters with distinct cards, abilities, and passives.
- **Where you have to:** Carefully manages your resources and read your opponent in order to execute clashes while maintaining your momentum.
- **However:** There is risk involved with each clash, the unpredictability of your opponent can disrupt your plans forcing you to adapt and rethink your strategy on the fly.

# Inspiration

- **Exceed board game by Level 99 Games**: A huge inspiration for this project and where many of the gameplay concepts originate from.
- **Memories of Lemon Tea:** An on hold personal project of mine. Mechanics, systems, and characters which I designed for this game were repurposed to be used in this project.

# Key Features

1. **Simultaneous Clash Combat**:
	- Combat in this game occurs simultaneously. When the turn player attacks or blocks with a card, a clash is initiated. During the clash, the opponent must choose a response: they can either do nothing, play their own card defensively to reduce damage, or play their own card offensively to deal damage. Both players' chosen cards remain hidden until they are ready to be revealed.
	- Once revealed, the card with the highest speed is resolved first. In the event of a tie, the turn player's card takes precedence. If one card is an attack and the other a block, the attack card resolves first. If both cards are blocks, the clash concludes without further action.
	- If the aggressor's card deals enough damage to break the responder's card, the responder's card is ignored. Otherwise, the responder's card will resolve after the aggressor's. It is common for both players to take damage when a clash finishes. Luck and strategy are crucial to safely clash with your opponent.
2. **Unique Resource Management:** 
	- Players can take 2 actions per turn, including drawing, attacking, moving, and more.
	- Cards are the primary resource; there is no mana system. Each card can be used offensively, defensively, or for support effects. If a player has a card in hand, they can play it. The only exception is **Extreme cards**, which require **Drive** to be used for attacks but can still be freely played for support and defense.
	- Cards generate supplementary resources: 
		- **Drive** is earned by dealing damage (when attacking) or reducing damage to zero (when blocking) during a clash. It is required for using Extreme cards offensive, and additionally can be converted into resolve when needed.
		- **Resolve** is gained by discarding cards and used as a cost for certain actions like moving.
3. **Board Game Strategy:** 
	- Characters occupy a 9-tile board, with each attack having a specific range. Players must strategically position themselves to dodge enemy attacks and set up their own. Some cards allow repositioning in the middle of a clash, enabling players to surprise opponents by being deceptively out of range or evading attacks during a clash.
	- Certain characters possess abilities that can place traps on board spaces or create projectiles that move down the board as players act.

# Themes

"Exalt Drive" centers on the theme of determination in the face of adversity. The title itself underscores the concept of elevating and harnessing one’s drive to achieve aspirations. To exalt means to uplift and manifest a superior version of oneself, and the game encourages players to strive for excellence by tapping into their inner drive and resolve.

In the game, **Drive** is earned through winning clashes, mirroring how progress toward meaningful objectives invigorates and motivates individuals. Just as achieving milestones in life fuels one’s determination, emerging victorious in battles replenishes and enhances your drive, propelling you closer to success. This reflects the real-world necessity of taking calculated risks to advance toward your goals.

The act of discarding cards to generate **Resolve** symbolizes shedding distractions to make resolute decisions. It’s a metaphor for the clarity and focus required in the pursuit of significant goals. By discarding, players are metaphorically clearing away the noise, enabling themselves to face challenges with renewed strength and determination.

The game’s mechanics are not just tools for gameplay but carry deeper significance. Progressing in battle requires calculated risks, similar to how pursuing life’s meaningful goals often involves stepping out of comfort zones and embracing uncertainty. "Exalt Drive" emphasizes that true progress comes from a relentless pursuit of improvement and the courage to confront and overcome obstacles.

In essence, the game embodies the journey of self-improvement and the power of determination. It champions the idea that in both the game and life, success is achieved by continually striving to elevate oneself, maintain focus, and harness one’s drive to face challenges head-on.

# Design Pillars

Pillars are the high-level designs for making the whole game from every aspects. If you look at the pillars you should have a good idea of what kind of game is being made. The pillars are the foundation upon which the entire game rests. Different aspects of the game design may have their own set of pillars which steer their design, however below are the core pillars which drive the entire project.

## Dynamic Combat and Player Agency

**Key Concept:**  
Dynamic Combat and Player Agency serve as the foundation of the game, emphasizing meaningful choices and player-driven outcomes. The game is designed to offer a rich and engaging experience where players have the freedom to explore diverse strategies and express their unique playstyles.

**Supporting Features:**
- **Simultaneous Clashes:** Players initiate and respond to attacks at the same time, allowing players to always have the opportunity to react.
- **Strategic Card Play:** Each card can be used offensively, defensively, or for support giving the player plenty of options when planning their strategy.
- **Positioning and Timing:** Players must consider their positioning on the board and the timing of their actions to maximize the effectiveness of their attacks and defenses.

**Elements That Would Oppose This Pillar**:
- **Strict Upgrades**: Cards or characters that are functionally an upgrade to one another would oppose this pillar as it presents the player with a false choice; There would be no reason to use the inferior cards. Anything that seems like an upgrade must come with some kind of trade-off.

**Goal:**  
To create an engaging combat experience that rewards strategic thinking, and adaptability. Players should feel that every decision they make has a significant impact on the game, leading to a dynamic and exciting gameplay environment.


## Avoidance of False Choices

**Key Concept:** 
A false choice is a decision where two near-identical options are presented, except one is functionally superior to the other. Such as 2 cards that consume the same resources but one deals more damage. This principle applies to all aspects of gameplay, including deck building, character selection, and decision-making during combat; The player should never be given the opportunity to make such a decision.

**Supporting Features:**
- **Diverse Options:** Each decision point offers a range of viable choices, with distinct advantages and drawbacks, ensuring that players have the opportunity to explore different strategies and approaches.
- **Balanced Design:** Game elements, such as cards, abilities, and character attributes, are  balanced to avoid situations where one option significantly outperforms others in similar circumstances.

**Goal:**  
The primary objective of this pillar is to cultivate a gameplay experience that values player choice, where decisions matter and have a meaningful impact on the outcome of the game. By avoiding false choices, players are encouraged to engage more deeply with the game's mechanics, explore diverse strategies, and experience a richer and more satisfying gameplay experience overall.

## Present With Style and Avoid Friction

**Key Concept:**  
"Present With Style and Avoid Friction" emphasizes the importance of delivering a visually captivating experience while ensuring that interactions are smooth and intuitive. The goal is to create a game world where every element, from combat to menu navigation, is designed with both aesthetic appeal and user-friendly functionality in mind.

**Supporting Features:**
- **Intuitive User Interface:** User interface elements are crafted to be visually appealing and easy to navigate, minimizing the effort required to access and understand game information and options.
- **Low-Friction Interactions:** There are no deeply nested menus in combat. 
	- Ex. To play a card for any of it's 3 uses (offense, defense, support) the player only needs to drag it onto one of 3 sections of the board and click a confirmation popup
	- Ex. There is no button to initiate a move, to move the player just needs to select a tile and then generate the resolve to move by offering cards and/or drive.
	- Ex. To draw the player clicks on their deck
	- Ex. To ignite the player drags the card to the button of the screen and click a confirmation popup
	- Ex. For unique character actions unique HUD elements will be added to perform them with a button click.

**Goal:**  
The goal of "Present With Style and Avoid Friction" is to create a game that not only looks good but also offers a seamless and enjoyable user experience. By combining aesthetic excellence with intuitive and low-friction interactions, the game aims to keep players engaged and immersed, making every moment of gameplay a visually rewarding and fluid experience.

**Inspiration:**
- Persona 5
- Persona 3 Reload