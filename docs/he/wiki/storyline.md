## **Storyline in DragonMine Z**

##### This page is still a work in progress. Please check back later for more information.

### **Overview**

In DragonMine Z, the storyline is a crucial part of the game, guiding players
through various sagas, quests, and objectives. Players can track their progress,
complete tasks, and unlock new content as they advance through the storyline.
The following sections provide detailed information about the available commands to manage
and interact with the storyline.

### **Commands**

#### **1. /storyline get**

Commands to retrieve information about the storyline.

- **/storyline get saga <id>**

  - Get details about a specific saga, including completion status and its quests.
- **/storyline get quest <id>**

  - Get details about a specific quest, including its objectives and completion status.
- **/storyline get progress**

  - Get a summary of all sagas and quests completed by the player.
- **/storyline get objective <id>**

  - Get details about a specific objective, including progress.

#### **2. /storyline set**

Commands to set or modify storyline data.

- **/storyline set saga <id> <true|false>**

  - Forcefully mark a saga as completed (true) or incomplete (false). Useful for debugging.
- **/storyline set quest <id> <true|false>**

  - Forcefully mark a quest as completed (true) or incomplete (false).
- **/storyline set objective <id> <true|false>**

  - Forcefully mark an objective as completed (true) or incomplete (false).

#### **3. /storyline reset**

Commands to reset storyline data.

- **/storyline reset saga <id>**

  - Reset a saga to its initial state (removing quest and objective completions).
- **/storyline reset quest <id>**

  - Reset a specific quest to its initial state.
- **/storyline reset all**

  - Reset all storyline progress for the player. Use this cautiously!

#### **4. /storyline list**

Commands to list sagas, quests, or objectives.

- **/storyline list sagas**

  - Show all sagas available in the game.
- **/storyline list quests**

  - Show all quests.
- **/storyline list objectives**

  - Show all objectives.

#### **5. /storyline debug**

Commands for debugging purposes.

- **/storyline debug data**

  - Print the raw capability data for the player’s storyline in JSON format.
  - Example output:
    ```json
      {
        "sagas": [
          { "id": "frieza_saga", "completed": 0, "quests": ["..."] }
        ]
      }
    ```
- **/storyline debug dependencies <quest_id>**

  - Check if all dependency requirements are fulfilled for a specific quest.
- **/storyline debug start <saga/quest> <saga_id/quest_id>**

  - **Force-starts a saga/quest. In a more detailed level, it only removes the prerequisites of such item.**
