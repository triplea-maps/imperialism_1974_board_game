# Imperialism - 1974 Board Game

This map is an adaptation of the 1974 board game Imperialism to the TripleA engine:  
[https://boardgamegeek.com/boardgame/14544/imperialism](https://boardgamegeek.com/boardgame/14544/imperialism)

It has a number of unique mechanics that differ from other TripleA maps. At the same time, various features of the original game are not currently possible with TripleA; these are documented later.

The map is generally playable. AIs do not work properly with TripleA 2.5, but are better on 2.6 where they're able to play effectively on the main continent, but are not able to explore yet.

### Overview

In this game, players start in the "old world" and sail to explore and gain control of "new world" territories. When a territory is first captured, it will get a "wealth production" rating (max 6 for new world or 4 for old world other than starting territories).

On your turn, you roll a die to determine which territories generate wealth. Each territory with wealth production higher or equal to the die roll will spawn one wealth unit (so territory wealth of 6 always succeeds and the lower the wealth roll the better). These wealth units must be brought to ports so they can be used for purchasing units. A city will increase the wealth production of a territory by 1.

### Additional rules

*   Players choose their starting territory, which must be on a coast in the old world (top left island).
*   Battles are optional and are limited to one round. When not decisive, armies will remain and territory control does not change.
*   Armies and fleets attack and defend on 2. Forts provide defense support with an extra strength 2 first strike roll per defending army. Note: This is different from the original board game combat rules, which TripleA isn't able to support.</li>
*   Armies, fleet and wealth have a movement of 1\. A fleet can transport an army or a wealth.
*   Structures and wealth are capturable.
*   Production and placement are before movement. No separate non-combat move.
*   Newly-built armies cannot participate in attacks.
*   Territories with no armies in them will revert to Neutral control and will not generate wealth.
*   Unit production is done at ports and requires spending wealth units present in the port. To build structures, you will first purchase and place corresponding "build" units in the port territory with the required wealth, following which you'll be given the actual unit to place elsewhere on the map.
*   Ships are built in a similar way as structures, except the player should (honor system) then place them next to the port where they were built.
*   Loading and unloading units requires fleets to be on coasts, represented by separate sea zones.
*   Armies attacking mountain territories attack on a 1 instead of 2.

### Unit summary and victory points

The goal is to have the most victory points at the end of the game, based on:

| **Entity**    | **Victory Points**      | **Note**                                           |
|---------------|-------------------------|----------------------------------------------------|
| Territory     | 2 * wealth production # | Produces wealth if die roll &lt;= value.           |
| Port          | 10                      | Factory building. Capturable.                      |
| City          | 6                       | Increases territory wealth production. Capturable. |
| Fort          | 2                       | Gives Fort Defense bonus to Armies. Capturable.    |
| Wealth        | 2                       | Spent to produce units at Ports. Capturable.       |
| Fleet         | 2                       | Att/Def 2, Move 1, Transports 1 Army or 1 Wealth.  |
| Army          | 1                       | Att/Def 2, Move 1. Fort Defense bonus at own Forts.|
| Fort Defense  | 0                       | Armies at own Forts get a First Strike 2 Def roll. |

Victory points are automatically tracked by the game as a resource.

The board game specifies that the game ends when the last card is drawn from the deck, but the card mechanics are not implemented in this version. Players can instead agree on a predetermined round number to end the game - or play until surrender.

### Original board game functionality missing from this adaptation

*   Randomization of player order, which can be done outside TripleA before starting
*   Drawing and playing cards from the deck
*   Random Storm/Pirate events
*   Border terrain types - mountains, rivers, etc and their effects
*   Combat dice calculations matching the original game
*   Land battles being optional (except with TripleA 2.6+)
*   Being able to select which opponent(s) you fight when 3+ players in territory
*   Being able to leave contested land territories (except with TripleA 2.6+)
*   Being able to capture wealth cargo at sea
*   Being able to load newly-built armies on fleets
*   Ships on coasts being able to participate in adjacent sea combats
*   Ports being treated as a "territory"
*   Ships having to "retreat" from captured territory ports

### Illegal moves allowed by the engine (honor system for humans)

*   Units being able to be loaded and unloaded on the same turn
*   Placing built fleets in ports elsewhere than where the wealth to build them came from
*   Splitting up placement of the initial fleet

### Credits

Some of the images (port icon, gear icon, etc) come from [OpenMoji](https://openmoji.org/) – the open-source emoji and icon project. License: CC BY-SA 4.0
