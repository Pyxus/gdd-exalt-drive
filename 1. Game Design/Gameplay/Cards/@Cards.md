---
tags:
  - game-design
  - index
categories:
  - cards
description: Combat cards represent the player's combat options. All combat cards can be used to attack, block, or perform utility tactic options.
---
*Brief description*
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

`=this.description`


# Properties

- **Damage:** Amount of damage a card deals
- **Guard:** In offence determines if the card staggers; In defense determines how much damage the card blocks 
- **Range:** The range where this card's attack can hit
- **Is Omnidirectional:** If true the card attacks both sides not just the direction toward the opponent.
- **Speed:** Determines which card resolves first during a clash
- **Link Level**: Used to determine which cards this card can link into
- **Category**:
	- **Unique:** Cards which can only be used by a specific character
	- **Extreme:** Unique cards which cost drive in order to be played. Extreme cards can generated 2 resolve.
	- **Common:** Common cards which can be used by any character
- **Clash Effects:** Effects which occur during the clash phase. They fall under BEFORE, HIT, AFTER, WIN, LOSS, EXALT, and BLOCK conditions.
- **Tactic Effects:** Utility effects one can gain by playing a card as a tactic. They call under 2 categories:
	- **Quick:** Discarded as soon as effect is performed.
	- **Enhance:** Discarded at the end of the next clash.