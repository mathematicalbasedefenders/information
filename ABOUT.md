**Mathematical Base Defenders is NOT a subsitute for a legitimate math tutor.**

Latest Revision: 2023-04-10

Welcome to Mathematical Base Defenders. This is a mental-math/number-cruncher game aimed at hardcore players. This document will cover the mechanics of this game.

This webpage's text is generated from a [text file in one of the repositories in this game's GitHub Organization](https://github.com/mathematicalbasedefenders/information/blob/main/ABOUT.md).

# About
Enemies will fall from the top to your "base". Each enemy has text which is a math problem. Your objective is to solve those math problems before the enemies come and reach your "base" (the line).

For example, if an enemy has the text `3 + 4`, you must type `7` and submit the problem to kill the enemy.

For each enemy you missed (i.e., for each enemy that reached the base), you will lose base health. If your base health is 0, the game is over.

This game has a leaderboards system and a multiplayer mode, so you can enjoy this game with friends and other people around the world.

# Input
You can either use the number-row or the numpad to type in your numbers. For enemies that have a negative answer, you can also type in the minus sign. (`-`). You can also press `Backspace` to delete your last entered digit, and you can either press `Enter` or `Space` to submit in your answer.

For mobile and/or touchscreen devices, there is a on-screen keyboard, accessible at the green `KB` button in the bottom left corner. You can increase or decrease the height of the on-screen keyboard with the `+H` or `-H` buttons respectively to match your preferred width.

Note that your answer will only "correctly" submit and your input bar will be cleared only if you submit a valid and correct answer. Additionally, your answer should already be "simplified", not `100-50` for `50` or `--33` for `33`.

# Enemies
Enemies have a predetermined chance of spawning every predetermined time interval.

| Mode | Interval | Chance |
| --- | --- | --- |
| Easy Singleplayer | 250ms | 5% |
| Standard Singleplayer/Default Multiplayer | 100ms | 10% |

Additionally, an enemy will also spawn if no enemies have spawned for 2500ms less than combo time.

Solutions to enemies' problems is an integer from `-100` to `100`, inclusive. Enemies can either be a number, or an addition, subtraction, multiplication or division problem. You can just type the number on number enemies.

# Modes
Mathematical Base Defenders has 3 game modes. Easy Singleplayer, Standard Singleplayer, and Default Multiplayer. More will be added in the future

## Singleplayer
In singleplayer, your main objective is to survive as long and get as many points as possible.

There are no penalites for incorrect/invalid answers.

The scoring for each enemy killed is determined by this formula: `100 + max(0, (sPosition - 0.5) * 50) * max(1, combo * 0.1 + 1)`.

## Multiplayer
In multiplayer, your main objective is to be the last player alive.

If you kill an enemy, and it qualifies certain criteria, you will send enemies to other players' stock. (This also applies vice versa.)

The number of enemies you will send for each enemy killed is determined by this formula: `max(0, floor((combo + 1) / 3)) + max(0, floor((sPosition - 0.5) / 0.1))`

Once you send enemies to other players' stock, or if enemies get sent to your stock, they do NOT spawn yet. 

If you have enemies waiting in your stock, you can reduce that stock by solving math problems. Your enemies in stock will be reduced by the same formula used by attacking. If there are leftovers, those will be converted into stock enemies against other players.

There is a penalty for invalid/incorrect answers. If you submit an invalid or an incorrect answer, all your enemies in your stock will spawn instantly at the same time.

Randomly generated enemies are the same for every player in a multiplayer room. Default Multiplayer uses the same speed settings as Standard Singleplayer.
