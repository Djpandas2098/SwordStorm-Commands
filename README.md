### Tester Documentation for Debug Commands

This document outlines the available debug commands for testers and group owners, including their usage, expected behavior, and required permissions. 

---

### **General Notes**
1. **Group Permissions:**
   - **Group Owner** (Rank: 255): Has access to all commands.
   - **Tester** (Rank: 3): Has limited access to commands (denoted below).

2. **Command Format:**  
   All commands are typed into the chat box and start with a **prefix (`!`)** followed by the command name and parameters (if any).

---

### **Command List**

#### 1. `!give [ToolName]`
- **Description:** Gives a specified tool to the player.
- **Syntax:** `!give ToolName`
- **Example:** `!give Sword`
- **Permissions:** **Group Owner Only**
- **Behavior:**  
  - If the tool exists in `script.AdminTools`, it is cloned and placed into the player's `Backpack`.
  - If the tool doesn't exist, a message is logged in the server output: `"dontexist"`.

---

#### 2. `!mana [Amount]`
- **Description:** Adds a specified amount of mana to the player.
- **Syntax:** `!mana Amount`
- **Example:** `!mana 50`
- **Permissions:** **Group Owner and Tester**
- **Behavior:**  
  - Calls the `ManaHandler.ChangeMana()` function to add the specified amount of mana to the player's character.

---

#### 3. `!damage [Amount]`
- **Description:** Applies a specified amount of damage to the player.
- **Syntax:** `!damage Amount`
- **Example:** `!damage 25`
- **Permissions:** **Group Owner and Tester**
- **Behavior:**  
  - Calls the `DamageHandler.ApplyDamage()` function to apply the damage to the player’s character.

---

#### 4. `!mastery [Amount]`
- **Description:** Adds mastery experience to the player’s character.
- **Syntax:** `!mastery Amount`
- **Example:** `!mastery 5`
- **Permissions:** **Group Owner and Tester**
- **Behavior:**  
  - Calls `MasteryHandler:AddExp()` repeatedly for the specified number of times.

---

#### 5. `!wepmastery [Amount]`
- **Description:** Adds weapon mastery experience to the player’s character.
- **Syntax:** `!wepmastery Amount`
- **Example:** `!wepmastery 10`
- **Permissions:** **Group Owner and Tester**
- **Behavior:**  
  - Calls `WeaponMasteryHandler:AddExp()` repeatedly for the specified number of times.

---

#### 6. `!yen [Amount]`
- **Description:** Adds a specified amount of yen to the player's total.
- **Syntax:** `!yen Amount`
- **Example:** `!yen 1000`
- **Permissions:** **Group Owner and Tester**
- **Behavior:**  
  - Calls `Manager.changeYen()` to add the specified amount of yen to the player’s current total.

---

#### 7. `!debug shadowcallout`
- **Description:** Resets all Shadow Callout mastery milestones for the player.
- **Syntax:** `!debug shadowcallout`
- **Permissions:** **Group Owner and Tester**
- **Behavior:**  
  - Calls `Manager.changeData()` to set all Shadow Callout mastery milestones (`30`, `40`, and `60`) to `false`.

---

#### 8. `!debug mastery`
- **Description:** Resets the player's mastery level and experience for their current element.
- **Syntax:** `!debug mastery`
- **Permissions:** **Group Owner and Tester**
- **Behavior:**  
  - Resets the player’s element mastery level to `1` and experience to `0` by calling:
    - `Manager.ChangeMasteryLevel(player, element, 1)`
    - `Manager.ChangeMasteryExp(player, element, 0)`
  - Reloads the player’s character.

---

#### 9. `!corearm`
- **Description:** Equips the player with the Core Arm accessory.
- **Syntax:** `!corearm`
- **Permissions:** **Group Owner and Tester**
- **Behavior:**  
  - Calls `Manager.changeCoreArmEquip()` to equip the Core Arm for the player.

---

### **Command Usage Summary Table**

| **Command**               | **Permissions**      | **Description**                                           | **Syntax Example**       |
|---------------------------|----------------------|-----------------------------------------------------------|--------------------------|
| `!give [ToolName]`        | Group Owner Only     | Gives a specified tool to the player.                     | `!give Sword`           |
| `!mana [Amount]`          | Owner & Tester       | Adds the specified amount of mana.                        | `!mana 50`              |
| `!damage [Amount]`        | Owner & Tester       | Applies the specified amount of damage.                   | `!damage 25`            |
| `!mastery [Amount]`       | Owner & Tester       | Adds mastery experience to the player’s character.        | `!mastery 5`            |
| `!wepmastery [Amount]`    | Owner & Tester       | Adds weapon mastery experience to the player.             | `!wepmastery 10`        |
| `!yen [Amount]`           | Owner & Tester       | Adds the specified amount of yen to the player.           | `!yen 1000`             |
| `!debug shadowcallout`    | Owner & Tester       | Resets Shadow Callout mastery milestones for the player.  | `!debug shadowcallout`  |
| `!debug mastery`          | Owner & Tester       | Resets the player's mastery level and experience.         | `!debug mastery`        |
| `!corearm`                | Owner & Tester       | Equips the Core Arm accessory for the player.             | `!corearm`              |

---

### **Testing Workflow**
1. **Group Owner and Tester Validation:**
   - Ensure you are part of the group with the required rank (`255` for Owner, `3` for Tester).
2. **Execute Commands:**
   - Type the commands in the in-game chat as per the syntax provided.
3. **Observe Changes:**
   - Verify the effects, such as tools appearing, stats being updated, or mastery being adjusted.
4. **Debugging:**
   - Use the developer console (`F9`) to check for errors or logs (`dontexist`, warnings).

If you encounter issues, escalate with proper logs for troubleshooting!
