---
tags:
  - game-design
  - index
categories:
  - characters
description: Characters are the playable combatants players control during battles. Each possesses a distinct set of advantages, allowing for strategic play and potentially dominating the fight.
---
`=this.description`

> [!infobox]+
> # `=this.file.name`
> ![[]]
> 
> | %%Empty%% |
> | ---- | ---- |
> ###### Section Info
> | %%Empty%% |
> | ---- | ---- |
> | Field | Value |

# 
# Combat

All characters have a set of stats which determine various aspects of the character during combat.

- **Ability / Exalted Ability:** Active ability unique to each character.
- **Affirmation / Exalted Affirmation:** Passives one gains while they possess a certain amount of drive (Not all characters have an affirmation).
- **Health:** Amount of hits a character can take before the game ends.
- **Composure / Exalted Composure:** Amount of interrupts a character can take before a composure break occurs.
	- Some characters gain more composure when exalted.
- **Deck:** Set of cards available to a character. For now characters will have fixed decks but deck building can be a thing.
- **Acts:** Acts are spent in order to perform actions during a turn.

# List of Characters

```dataview
TABLE WITHOUT ID
	embed(link(portrait, "150h")) AS "Character",
	file.link as "Name",
	description,
	archetype,
	race,
	gender,
	age,
	health,
	composure
FROM #game-design AND -#index AND -"misc"
WHERE contains(categories, "characters")
```