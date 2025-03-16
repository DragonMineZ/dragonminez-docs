# Commands Information for Servers

DragonMine Z offers a few commands to help server owners and players manage other player stats. There's also a command to make debug, commands related to the storyline, and more.
These commands are available only to players with the appropriate permissions.

## **_Player_ Commands:**

1. `/dmzalignment <set|add|remove> <points> <player>`
     - `Set`: Set the alignment points of a player, overwriting the current value.
     - `Add`: Add alignment points to a player.
     - `Remove`: Remove alignment points from a player.
2. `/dmzstats <set|add|remove> <stat|all> <quantity> <player>`
     - `Set`: Set the value of a stat of a player, overwriting the current value.
     - `Add`: Add points to a stat of a player.
     - `Remove`: Remove points from a stat of a player.
     - `Stat` should be replaced by the name of the stat you want to change, for example, `strenght`.
3. `/dmzpoints <set|add|remove> <points> <player>` - ZPoints = TPs
     - `Set`: Set the points of a player, overwriting the current value.
     - `Add`: Add points to a player.
     - `Remove`: Remove points from a player.
4. `/dmzrestart <player>`
     - Restart the player, resetting all stats, skills, and everything else to the default values.
     - The player can create their character again after using this command.
     - This is the same as using the `Reset Character` option from the Dende NPC.
5. `/dmzrevive <player>`
     - Revive a dead player.
     - Also removes the Halo from the player.
6. `/dmzpermaeffects <give|take> <effect> <player>`
     - `Give`: Give a permanent effect to a player.
     - `Take`: Remove a permanent effect from a player.
     - `Effect` should be replaced by the name of the effect you want to give or remove, for example, `majin`.
7. `/dmztempeffects <give|take> <effect> <duration> <player>`
     - `Give`: Give a temporary effect to a player.
     - `Take`: Remove a temporary effect from a player.
     - `Effect` should be replaced by the name of the effect you want to give or remove, for example, `mightfruit`.
     - `Duration` should be replaced by the duration of the effect in seconds.
8. `/dmzskill <give|set|take> <skill> <level> <player>`
     - `Give`: Give a skill to a player.
     - `Set`: Set the level of a skill of a player, overwriting the current value.
     - `Take`: Remove a skill from a player.
     - `Skill` should be replaced by the name of the skill you want to give, set, or remove, for example, `fly` or `potential_unlock`.
9. `/dmzforms <give|set|take> <form_id> <level> <player>`
     - `Give`: Give a form to a player.
     - `Set`: Set the level of a form of a player, overwriting the current value.
     - `Take`: Remove a form from a player.
     - `Form_id` should be replaced by the id of the form you want to give, set, or remove, for example, `super_form`.

## **_Storyline_ Commands:**

1. `/dmzstoryline set <saga|quest|objective> <id> <completed>`
     - Set the status of a saga or quest of a player.
     - If `Saga` is used, the `id` should be the saga id, for example, `saiyan`.
     - If `Quest` is used, the `id` should be the quest id, for example, `saiyQuest3`.
     - If `Objective` is used, the `id` should be the quest id, for example, `saiyQuest3`.
     - `Completed` should be replaced by the status you want to set, `true` or `false`.
2. `/dmzstoryline get <saga|quest|objective> <id>`
     - **TBD**
3. `/dmzstoryline reset <saga|quest|all> <id>`
     - Reset the status of a saga or quest of a player.
     - If `Saga` is used, the `id` should be the saga id, for example, `saiyan`.
     - If `Quest` is used, the `id` should be the quest id, for example, `saiyQuest3`.
     - If `All` is used, no `id` is needed.
4. `/dmzstoryline list <sagas|quests|objectives>`
     - If `Sagas` is used, it will list all sagas.
     - If `Quests` is used, it will list all quests.
     - If `Objectives` is used, it will list all objectives.
5. `/dmzstoryline debug data`
     - **TBD**
6. `/dmzstoryline debug start <saga|quest> <id>`
     - **TBD**

## **_Server Useful_ Commands:**

1. `/dmzlocate <structure>`
     - Same use as the `/locate` command, but for DragonMine Z structures.
     - You need to be in the same dimension as the structure you want to locate, otherwise, the command will not work.
     - The available structures are: `KamiLookout`, `HyperbolicTimeChamber`, `KorinTower`, `GokuHouse`, `KameHouse`, `KingKaiPlanet`, `ElderGuruHouse`.
2. `/data get entity <Player> ForgeCaps.dragonminez:mod`
     - Will return all the Player's data related to DragonMine Z.
     - This command is useful for debugging everything related to the mod.
3. `/daga get entity <Player> ForgeCaps.dragonminez:storyline`
     - Will return all the Player's storyline data.
     - This command is useful for debugging specifically the storyline.