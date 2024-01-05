**Mathematical Base Defenders is NOT a substitute for a legitimate math tutor.**

Latest Revision: 2024-01-05

Updated for game version `0.4.5`.

This webpage's text is generated from a [text file in one of the repositories in this game's GitHub Organization](https://github.com/mathematicalbasedefenders/information/blob/main/ABOUT.md).

# Welcome
Welcome to Mathematical Base Defenders! Mathematical Base Defenders is a game playable on a web browser that tests your mental math speed. It has both singleplayer and multiplayer modes, an account system, two leaderboards, and many more.

# Authentication

**Note: Registration is NOT required to play.**

## Registering for an Account

To register for an account, go to [https://mathematicalbasedefenders.com/register](https://mathematicalbasedefenders.com/register). 

## Logging into your Account

To log in to your account, go to the play subdomain [https://play.mathematicalbasedefenders.com](https://play.mathematicalbasedefenders.com) and log in through the `Settings` > `Online` menu.

# Basic Gameplay
Enemies will fall from the top to your "base". Each enemy has text which is either a number or a math problem. Your objective is to type the number or solve those math problems before the enemies come and reach your "base" (the line).

If an enemy has the text `10`, you must type `10` and submit the problem to kill the enemy.

If an enemy has the text `3 + 4`, you must type `7` and submit the problem to kill the enemy. (`3 + 4 = 7`)

For each enemy you missed (i.e., for each enemy that reached the base), you will lose base health. If your base health is 0, the game is over.

# Input
You can either use the number-row or the number-pad on your keyboard to type in your numbers. For enemies that have a negative answer, you can also type in the minus sign. (`-`). You can also press `Backspace` to delete your last entered digit, and you can either press `Enter` or `Space` to submit in your answer.

For mobile and/or touchscreen devices, or for devices with no keyboard, there is a on-screen (virtual) keyboard, accessible at the green button in the bottom left corner's menu. You can increase or decrease the height of the on-screen keyboard with the `+H` or `-H` buttons respectively to match your preferred height.

## Input Constraints

Your answer will only "correctly" submit and your input bar will be cleared only if you submit a valid and correct answer. Your answer must already be "simplified", fot example, `45` and `-32` are acceptable, but not `100-50` for `50` or `--33` for `33`.

# Enemies
Enemies have a predetermined chance of spawning every predetermined time interval.

| Mode | Interval | Chance |
| --- | --- | --- |
| Easy Singleplayer | 150ms | 7.5% |
| Standard Singleplayer/Default Multiplayer | 100ms | 10% |

As you progress further through a singleplayer game, the time between enemy spawn chance intervals<!--  --> will be decreased by 1.25% compounding per level. The chance will stay the same.

Additionally, an enemy will also spawn if no enemies have spawned for 2500ms less than combo time.

Solutions to enemies' problems is an integer from `-100` to `100`, inclusive. Enemies can either be a number (3/7), or an addition, subtraction, multiplication or division problem (1/7 each). You can just type the number on number enemies.

# Modes
Mathematical Base Defenders currently has 4 game modes. Easy Singleplayer, Standard Singleplayer, Custom Singleplayer, and Default Multiplayer. More will be added in the future

## Singleplayer
In singleplayer, your main objective is to get as many points as possible.

There are no penalties for incorrect/invalid answers.

You get `100 + max(0, (sPosition - 0.5) * 50) * max(1, combo * 0.1 + 1)` points for killing an enemy.

### Additional Information for Custom Singleplayer

Before starting a Custom Singleplayer game, you may set the parameters of the game. You can hover over each field to see what it does. All times are in milliseconds.

To prevent abuse, there is a limit on how extreme the parameters can be. If you set a value to be too extreme, the game will refuse to start telling you the offending value(s). Additionally, no experience points will be awarded in Custom Singleplayer games.

## Multiplayer
In multiplayer, your main objective is to be the last player alive.

If you kill an enemy, and it qualifies certain criteria, you will send enemies to other players' stock. (This also applies vice versa.)

The number of enemies you will send for each enemy killed is determined by this formula: `max(0, floor((combo + 1) / 3)) + max(0, floor((sPosition - 0.5) / 0.1))`

Once you send enemies to other players' stock, or if enemies get sent to your stock, they do NOT spawn yet. 

If you have enemies waiting in your stock, you can reduce that stock by solving math problems. Your enemies in stock will be reduced by the same formula used by attacking. If there are leftovers, those will be converted into stock enemies against other players.

There is a penalty for invalid/incorrect answers. If you submit an invalid or an incorrect answer, all your enemies in your stock will spawn instantly at the same time.

Randomly generated enemies are the same for every player in a multiplayer room. Default Multiplayer uses the same speed settings as Standard Singleplayer.

# Technical Details

## Score Formula

There are two variables in the score/attack formula for Singleplayer/Multiplayer mode respectively. The variables are `combo` and `sPosition`.

### `combo`
The combo is how many enemies you have managed to kill consecutively. For each enemy killed, your combo time will be set back to the highest combo time, which drops down as time passes, and you earn +1 combo.
When your timer runs out, the combo resets back to `-1`.

### `sPosition`
Due to the number of different window dimensions this game can be played on, calculating how far an enemy is from your base would not lead to consistent results. As such, a measurement called `sPosition` is created. When an enemy first spawns, that is, when the enemy is at the topmost position, its `sPosition` is `1`, and when an enemy reaches your base, its `sPosition` is `0`.

## Implementation
Mathematical Base Defenders is written primarily using TypeScript. It also uses `Node.js` for server-side code, `uWebSockets.js` for bidirectional communication of game data, and `PixiJS` for drawing graphics.

### Contributing
Contributions and comments are welcome. File an issue or open a pull request, and the maintainer will take a look at it. Contributing also gives a special rank to your user account.

# Social Media
Mathematical Base Defenders is also on social media!
- Discord Server: [https://discord.gg/pDTZvrTXm9](https://discord.gg/pDTZvrTXm9) 
- Facebook: [https://facebook.com/mathematicalbasedefenders](https://facebook.com/mathematicalbasedefenders)
- Instagram: [https://instagram.com/mathematicalbasedefenders](https://instagram.com/mathematicalbasedefenders)
- X (Twitter): [https://twitter.com/MathematicalBD](https://twitter.com/MathematicalBD)

# Donations
Donations are always welcome! Either sponsor mistertfy64 through GitHub or donate to him through Patreon.

**Please note that donations do NOT give gameplay perks.**

**Donations give cosmetic perks, however, these aren't implemented yet. If you want these once they're implemented, contact the maintainer.**
