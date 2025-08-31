# Tester & Admin Commands Documentation

## Press ` to access the command line

## Dont forget to do ":" before every command.

---

## General Tester Commands

These commands are accessible to general testers for basic gameplay testing and simulation.

| Command | Description |
|--------|-------------|
| `SetGold (player) (amount)` | Sets the player's Yen/Gold to the specified amount. |
| `ChangeElement (player) (elementname)` | Changes the player's current element to the specified element. |
| `ChangeRace (player) (racename)` | Changes the player's race to the specified race. |
| `ChangeWeapon (player) (weaponname)` | Changes the player's weapon to the specified weapon. |
| `GiveExp (player) (amount)` | Gives the player a specified amount of experience. |

---

## Advanced Tester Commands

These are advanced commands for simulating more specific gameplay scenarios and character customization.

| Command | Description |
|--------|-------------|
| `GiveClothing (player) (clothing/armor name)` | Gives the specified clothing or armor to the player. |
| `GiveMobDrop (player) (biome/folderpath) (dropname)` | Gives the specified mob drop to the player from a specified biome or path. |
| `GiveItem (player) (itemname)` | Gives the specified item to the player. |
| `ResetPoints (player)` | Resets all of the player's invested stat points and returns them to be reassigned. |

---

## Miscellaneous Tester Commands

Commands that help with quality-of-life testing functionality and player management.

| Command | Description |
|--------|-------------|
| `GotoTester (player) (player_to_teleport_to)` | Teleports one player to another tester. |
| `HealTester (player)` | Fully restores the player's health. |
| `KillTester (player)` | Kills the tester. Can only be used on yourself. |
| `ResetTester (player)` | Resets the tester's state (alternative to kill). |

---

## Admin Commands

High-level admin-only commands used for advanced access and debug features.

| Command | Description |
|--------|-------------|
| `GiveAdminSpecs (player)` | Grants special admin-specific specs to the player. |
| `GiveEarlySpecs (player)` | Grants early-access or developer specs to the player. |
| `SpiritualPressure (player)` | Activates or simulates a spiritual pressure effect on the player. |

---

> Note: Always double-check arguments. Improper use of commands may result in unexpected behavior.
