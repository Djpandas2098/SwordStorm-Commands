### Command Documentation for Testers

This documentation outlines the various commands available in the game for testers, with clear explanations on how to use them effectively.

---

**1. !give [ToolName]**  
- **Purpose**: Gives the player a tool by name.  
- **Usage**:  
    `!give [ToolName]`  
- **Example**:  
    `!give Sword`  
- **Permissions**: Only **Group Owners** can use this command.  
- **What it does**: This command will give the player a tool (e.g., Sword) from the `AdminTools` folder in the script.

---

**2. !mana [Amount]**  
- **Purpose**: Adds a specified amount of mana to the player's character.  
- **Usage**:  
    `!mana [Amount]`  
- **Example**:  
    `!mana 100`  
- **Permissions**: **Group Owners** and **Testers** can use this command.  
- **What it does**: This command adds the specified amount of mana to the player's character by calling the `ManaHandler`.

---

**3. !damage [Amount]**  
- **Purpose**: Deals a specified amount of damage to the player's character.  
- **Usage**:  
    `!damage [Amount]`  
- **Example**:  
    `!damage 50`  
- **Permissions**: **Group Owners** and **Testers** can use this command.  
- **What it does**: This command will apply the specified amount of damage to the player's character using the `DamageHandler`.

---

**4. !mastery [Amount]**  
- **Purpose**: Adds experience to the player's mastery, allowing them to level up.  
- **Usage**:  
    `!mastery [Amount]`  
- **Example**:  
    `!mastery 5`  
- **Permissions**: **Group Owners** and **Testers** can use this command.  
- **What it does**: This command increases the player's mastery level by the specified amount, using the `MasteryHandler`.

---

**5. !wepmastery [Amount]**  
- **Purpose**: Adds experience to the player's weapon mastery.  
- **Usage**:  
    `!wepmastery [Amount]`  
- **Example**:  
    `!wepmastery 10`  
- **Permissions**: **Group Owners** and **Testers** can use this command.  
- **What it does**: This command adds experience points to the player's weapon mastery, which is managed by the `WeaponMasteryHandler`.

---

**6. !yen [Amount]**  
- **Purpose**: Adds a specified amount of yen to the player's total.  
- **Usage**:  
    `!yen [Amount]`  
- **Example**:  
    `!yen 1000`  
- **Permissions**: **Group Owners** and **Testers** can use this command.  
- **What it does**: This command will add the specified amount of yen to the player's character, updating the player data accordingly.

---

**7. !debug [key],[value]**  
- **Purpose**: Change any player's data field dynamically by specifying the key and value.  
- **Usage**:  
    `!debug [key],[value]`  
- **Example**:  
    `!debug Data.Accessories.Neck, Golden Necklace`  
    `!debug Data.Yen, 1000`  
- **Permissions**: **Group Owners** and **Testers** can use this command.  
- **What it does**: This command allows the tester to modify any player's data using dot notation to specify the key and value to change.  
    - The `key` can be a path to any value in the player's data structure (e.g., Data.Accessories.Neck).  
    - The `value` can be a **string**, **number**, or **boolean** (e.g., "Golden Necklace", 1000, or true).  
    - Examples of accepted values:  
        - true (for boolean)  
        - false (for boolean)  
        - 1000 (for number)  
        - "Golden Necklace" (for string)  

---

**8. !corearm**  
- **Purpose**: Equip the player with a Core Arm.  
- **Usage**:  
    `!corearm`  
- **Permissions**: **Group Owners** and **Testers** can use this command.  
- **What it does**: This command equips the player's character with a Core Arm by calling the `Manager.changeCoreArmEquip`.

---

### Important Notes:
- **Permissions**: Testers and Group Owners have access to these commands, except for !give which is limited to Group Owners only.  
- **Command Format**: Ensure the command is entered correctly with the appropriate parameters.  
- **Command Feedback**: Commands that are successful will apply the changes, while invalid commands or parameters will return an error message.

---

This documentation will help testers easily understand how to use the in-game commands and what each one does. The commands are designed to help you test and modify different aspects of player data, tools, and game mechanics.

---
