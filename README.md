# Forge Bot 1.16.5

Forge Bot is a mod designed for Minecraft 1.16.5, allowing users to execute pre-configured commands by reading from `.txt` files. This bot automates tasks by parsing commands listed in configuration files, enabling smooth and efficient gameplay.

## Installation

1. **Download and Install Forge 1.16.5**: Ensure you have the correct version of Forge installed.
2. **Add the Mod**: Place the downloaded Forge Bot mod file into your `mods` folder.
3. **Run Minecraft**: Launch the game with Forge to activate the mod.

## Usage

### Command Overview

- **`.load "file_name"`**: Load a configuration file in folder **`config`** by its name (omit the `.txt` extension). This step is necessary each time you update the configuration file.
- **`.start`**: Begin executing the loaded commands.
- **`.stop`**: Stop the execution of commands.

### Command File Structure

- **File Format**: Commands must be listed in a `.txt` file.
- **Line-by-Line**: Each command must be on its own line. Multiple commands on one line are not supported.

### Primary Commands

1. **`СЕК "время"`**: Sets a delay between commands.  
   - Example: `СЕК 20` (20-second delay).
   - Variants: `МИН "время"` for minutes, `ЧАС "время"` for hours.

2. **`ЧАТ "message"`**: Sends a message in chat.  
   - Example: `ЧАТ "/spawn"` (Sends "/spawn" in chat).

3. **`ПОВТОРИ "количество"`**: Repeats a set of commands a specified number of times.  
   - Example:
     ``` 
     ПОВТОРИ 10 {
     ЧАТ "привет"
     СЕК 2
     }
     ```
     (Repeats the chat and delay command 10 times).

4. **`АВТОВЫХОД "количество блоков"`**: Automatically leaves the server if a player is within the specified block radius.  
   - Example: `АВТОВЫХОД 20` (Leaves if a player is within 20 blocks).

5. **`АТАКОВАТЬ "true|false"`**: Toggles attacking all entities.  
   - Example: 
     ```
     АТАКОВАТЬ true
     СЕК 20
     АТАКОВАТЬ false
     ```
     (Attacks for 20 seconds).
   - Short form: `АТАКОВАТЬ 1` (true), `АТАКОВАТЬ 0` (false).

6. **`ПРЫЖОК "true|false"`**: Toggles auto-jump.  
   - Example: 
     ```
     ПРЫЖОК true
     сек 30
     ПРЫЖОК false
     ```
     (Jumps for 30 seconds).
   - Short form: `ПРЫЖОК 1` (true), `ПРЫЖОК 0` (false).

7. **`ПРИСЕСТЬ "true|false"`**: Toggles crouching.  
   - Similar logic to `АТАКОВАТЬ` and `ПРЫЖОК`.

8. **`НАПРАВО "количество градусов"`**: Rotates the view to the right by the specified degrees.  
   - Example: `направо 90` (Turns 90 degrees right).

9. **`НАЛЕВО "количество градусов"`**: Rotates the view to the left by the specified degrees.  
   - Example: `налево 90` (Turns 90 degrees left).

## Support

If you have any questions or need further assistance, feel free to reach out on Discord: **asm.abuse**.

