!!! **Mathematical Base Defenders is NOT a subsitute for a legitimate math tutor.** !!!

Latest Revision: 2022-08-30

Current Website Version: 0.4.9

**Content here is subject to change without notice. Mathematical Base Defenders is in its development stage.**

# About
Mathematical Base Defenders is a speed math game where you can play alone, or with other players around the world.

# Objective
Many math games want you to solve math problems quickly to get points. However Mathematical Base Defenders is the opposite. Instead of solving problems, you create the problems.

# Play
To play, you use the 49 tiles to form math problems.

When sending the problem, if the problem evaluates to at least one enemy's requested value, the enemy/ies are killed, and you earn points.

The enemies will keep moving to your "base" (the building), when one reaches your base, your base loses a health point. If your base runs out of health points, the game is over.

## Controlling
To select or a tile to add it to your problem, click or press the corresponding key on your keyboard to select it.

To deselect a tile with your mouse, simply click on the tile again.

To deselect a tile with your keyboard, press the `Backspace` key.

The keybinds for each tile can be changed. Note that the numberpad will always be one of the keys for number and operator tiles.

| Tile | Default Keybind | Numpad Keybind |
| --- | --- | --- |
| 0 | `KeyM` | `Numpad0` |
| 1 | `KeyJ` | `Numpad1` |
| 2 | `KeyK` | `Numpad2` |
| 3 | `KeyL` | `Numpad3` |
| 4 | `KeyU` | `Numpad4` |
| 5 | `KeyI` | `Numpad5` |
| 6 | `KeyO` | `Numpad6` |
| 7 | `Digit7` | `Numpad7` |
| 8 | `Digit8` | `Numpad8` |
| 9 | `Digit9` | `Numpad9` |
| + | `Slash` | `NumpadAdd` |
| - | `SemiColon` | `NumpadSubtract` |
| × | `KeyP` | `NumpadMultiply` |
| ÷ | `Digit0` | `NumpadDivide` |
| = | `Quote` | `NumpadEnter` |
| a | `KeyW` | (None) |
| b | `KeyE` | (None) |
| c | `KeyS` | (None) |
| d | `KeyD` | (None) |

## Mechanics

### Game Modes

#### Singleplayer

One of the modes in Mathematical Base Defenders is Singleplayer.

Currently, there are only two default game modes and a custom game mode on Singleplayer. Click the Singleplayer to be able to select between the Easy mode and the Standard Mode.

When playing Singleplayer mode, you can quickly exit the game by pressing Escape.

When a default Singleplayer game is finished, all games finished by registered users have their scores submitted.

Mathematical Base Defenders keeps track of your personal best score. In addition, it also tracks the 50 highest scores on default Singleplayer games on the leaderboards. If you finished the game with a new personal best and/or top 50, the game will tell you.

Only your best score is stored on the leaderboards and your account (Note from mistertfy64: This may change!!!). (i.e. you can only see your username once on the leaderboards.)

#### Multiplayer

One of the modes in Mathematical Base Defenders is Multiplayer.

Currently, there is only one multiplayer room, called the Default Room. Click the Multiplayer button to go to the Multiplayer menu.

Rooms need at least 2 players to start, when a room reaches 2 players, the game will automatically start in 30 seconds.

Instead of gaining points when you kill enemies, when you kill an enemy, depending if you meet certain conditions, you may send enemies to other players.

When a player's base loses all health points in Multiplayer, that player is eliminated.

Be the last one standing to be the winner. The results of the current (or last depending on the state) game is shown on the left of the screen.

You can chat with other players in multiplayer rooms.

#### Tiles

There are always 49 tiles in the game.

There are a total of 19 types of tiles in the game.

When generating new tiles, the game uses an algorithm similar to block-stacking games (e.g. "7 bag"), where a tile type is guaranteed to appear exactly x times every 49 generated tiles.

| Tile | Appear Rate |
| --- | --- |
| 0 | 4 per 49 |
| 1,2,3,4,5,6,7,8,9 | 3 each per 49 |
| +,-,×,÷,=,a,b,c,d | 2 each per 49 |

### Enemies

Enemies are generated randomly.

Enemies' values can be anywhere from -1000 to 1000 with or without a variable.

### Variables
Variables are "storage containers", where you can store a value inside a variable.

To assign a variable, select the variable, then select the equals sign, then select the wanted value. (e.g. `a = 20`)

The value will then be stored in the variable. You can select the variable to substitute for the value in the variable.

To kill an enemy with a variable that isn't assigned to a value, just create the problem.

To kill an enemy with a variable that is assigned to a value, just create the problem, or substitute the value of the variable as the variable.

(e.g. To kill a `100` enemy with `a = 20` as one of your variables, `100`, `99+1` or `5a` will all work, and to kill a `5a` enemy with no variables assigned, `5a` will work. (Note from mistertfy64: `3a+2a` doesn't work yet, this will be implemented but im too stupid to do it.))

### Problem
The problem is the expression/equation created from selected tiles.

In Singleplayer, there is no penalty for invalid/incorrect problems sent.

In Multiplayer, if you have enemies pending and you've sent an invalid/incorrect problem, all the pending enemies will now become actual enemies, however, if you've sent a valid and correct problem, the enemy will be killed and pending enemies will not spawn, even if the problem did not send any enemies.

### Combo
You start with 0 (stored as -1 internally) combo.

When you kill an enemy, a timer starts (5 seconds in Standard Singleplayer and Default Multiplayer, 10 seconds in Easy Singleplayer). If the timer hits 0, the combo will be reset.

If you kill an another enemy within the timer period, the timer resets (to 5 or 10 seconds, depending on game mode), and your combo increases.

## Additional Information

Developer/Game Master: mistertfy64 ([https://mistertfy64.com](https://mistertfy64.com))

Issue tracker (feature requests also accepted): [https://github.com/mathematicalbasedefenders.com/issuetracker](https://github.com/mathematicalbasedefenders.com/issuetracker)

Remaining for this file: Experience and Technical

Donations: [https://patreon.com/mistertfy64](https://patreon.com/mistertfy64)
