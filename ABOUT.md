**Disclaimer: While Mathematical Base Defenders may help with mental math skills, Mathematical Base Defenders is NOT a substitute for a legitimate math tutor.**

Latest Revision: July 1, 2025.

Updated for Game Version `0.5.0-rc.6`.

This webpage's text is generated from a [text file in one of the repositories in this game's GitHub Organization](https://github.com/mathematicalbasedefenders/information/blob/main/ABOUT.md).

---

## Welcome
Welcome to Mathematical Base Defenders! Mathematical Base Defenders is a game playable on a web browser that tests your mental math speed. 

Mathematical Base Defenders has Singleplayer and Multiplayer modes and other supplementary features such as leaderboards and replays.

---

## Authentication

**Note: Registration is NOT required to play on Singleplayer or Multiplayer mode.**

### Registering for an Account

To register for an account, go to [https://mathematicalbasedefenders.com/register](https://mathematicalbasedefenders.com/register).

The registration form asks for your e-mail address, username and password.

E-mail addresses are used for confirming an account's owner authenticity to reset an account's password (in case of lost/forgotten passwords).

---

### Logging into your Account

To log in to your account, go to the play subdomain [https://play.mathematicalbasedefenders.com](https://play.mathematicalbasedefenders.com), and you will be asked to log in with your username and password. 

Note that after exiting the opening screen (i.e., closing the login modal), you cannot authenticate due to how authentication in this game is implemented.

The login modal/opening screen can be brought back by refreshing the page, and you can log in again.

---

## Basic Gameplay

Enemies will fall from the top to your "base".

Each enemy has text which is either an integer, an addition math problem, a subtraction math problem, a multiplication math problem, or a division math problem. If an enemy's text is a math problem, both operands of a math problem will be integers.

The integers and problems are randomly generated. However, the integer/answer to a problem will fall within a range (`-100` to `100`, inclusive).

As of Game Version `0.5.0-rc.6`, it is guaranteed that the if the enemy's text is an integer, it will be between `-100` and `100` (inclusive), and if the enemy's text is a math problem, the answer will be between `-100` and `100`. Additionally, answers to division problems will always be an integer (i.e., no decimals), and there will not be any problems that ask you to divide an integer by zero.

The main objective of Mathematical Base Defenders is to type the number on the enemies or solve the math problems on the enemies to kill them before the enemies come and reach your "base" (the line).

If an enemy's text is an integer (not a math problem), you must type the integer and submit it as your answer.

If an enemy's text is a math problem, you must solve the math problem, then type the answer to the math problem, then submit it as your answer.

### Examples
| Enemy Text | What to Type | Explanation
| --- | --- | --- |
| `4` | `4` | For enemies without a math problem as its text, type the number on it.
| `-20` | `-20` | For enemies without a math problem as its text, type the number on it. Note that integers can be negative.
| `5 + 3` | `8` | The answer to `5 + 3` is `8`. |
| `6 - 2` | `4` | The answer to `6 - 2` is `4`. |
| `8 × 8` | `64` | The answer to `8 × 8` is `64`. |
| `10 ÷ 2` | `5` | The answer to `10 ÷ 2` is `5`. | 
| `2 - 6` | `-4` | The answer to `2 - 6` is `-4`. Note that answers to problems can be negative. |
| `8 × -9` | `-72` | The answer to `8 × -9` is `-72`. Note that answers to problems can be negative. |
| `-10 ÷ 2` | `-5` | The answer to `10 ÷ -2` is `-5`. Note that answers to problems can be negative. | 
| `-3 × -9` | `27` | The answer to `-3 × -9` is `27`. |
| `-40 ÷ -2` | `20` | The answer to `-40 ÷ -2` is `20`. | 

In non-custom Modes, your base will start with 100 health points and each enemy that reaches the base (fail to kill) will reduce your base health by 10 points. To keep the game playable for longer periods of time, your base health will also passively regenerate.

The game is over once your base health reaches or goes below 0 health points. At this point, you can play again.

---

## Input
You can either use the number-row or the number-pad on your keyboard to type in your numbers. For enemies that have a negative answer, you can also type in the minus sign. (`-`). You can also press `Backspace` to delete your last entered digit, and you can either press `Enter` or `Space` to submit in your answer.

For mobile and/or touchscreen devices, or for devices with no keyboard, there is a on-screen (virtual) keyboard, accessible at the green button in the bottom left corner's menu. You can increase or decrease the height of the on-screen keyboard with the `+H` or `-H` buttons respectively to match your preferred height.


### Input Constraints

Your answer will only "correctly" submit and your input bar will be cleared only if you submit a valid and correct answer. Your answer must already be "simplified", fot example, `45` and `-32` are acceptable, but not `100-50` for `50` or `--33` for `33`.

---

## Enemies
Enemies have a predetermined chance of spawning every predetermined time interval.

| Mode | Interval | Chance |
| --- | --- | --- |
| Easy Singleplayer | 150ms | 7.5% |
| Standard Singleplayer | 100ms | 10% |
| Default Multiplayer | 100ms | 10% |

As you progress further through a singleplayer game, the time between enemy spawn chance intervals will be decreased by 1.25% compounding per level. The chance will stay the same.

Additionally, an enemy will also spawn if no enemies have spawned for 2500ms less than combo time.

Additionally, there will always be at least one enemy on the playfield at any given time. If there are no enemies on the enemy playfield, one will instantly spawn.

Enemy text can either be integer, an addition math problem, a subtraction math problem, a multiplication math problem, or a division math problem. The chances are the same for every mode.

| Enemy Type | Chance |
| --- | --- |
| Integer (No Math Problem) | 3 out of 7
| Addition Math Problem | 1 out of 7
| Subtraction Math Problem | 1 out of 7
| Multiplication Math Problem | 1 out of 7
| Division Math Problem | 1 out of 7

---

## Modes
Mathematical Base Defenders currently has 4 game modes. Easy Singleplayer, Standard Singleplayer, Custom Singleplayer, and Default Multiplayer. More will be added in the future.


### Singleplayer

In singleplayer, your main objective is to get as many points as possible.

There are no penalties for incorrect/invalid answers.

You get `100 + max(0, (sPosition - 0.5) * 50) * max(1, combo * 0.1 + 1)` points for killing an enemy.


#### Additional Information for Custom Singleplayer

Before starting a Custom Singleplayer game, you may set the parameters of the game.

You can hover over each field to see a tooltip that explain what it does. All times are in milliseconds.

To prevent abuse, there is a limit on how extreme the parameters can be. If you set a value to be too extreme, the game will refuse to start telling you the offending value(s). Additionally, no experience points will be awarded in Custom Singleplayer games.

---

### Multiplayer

In multiplayer, your main objective is to be the last player alive.

If you kill an enemy, and it qualifies certain criteria, you will "send" enemies to other players' "stock". For each enemy you send, it has an equal chance of going into an opponent's stock.

The number of enemies you will send for each enemy killed is `max(0, floor((combo + 1) / 3)) + max(0, floor((sPosition - 0.5) / 0.1))`

Enemies that aren't from enemy stocks (e.g., generated enemies that come up) will have the same text.

There is a penalty for invalid/incorrect answers. If you submit an invalid or an incorrect answer, all your enemies in your stock will spawn instantly at the same time.

Randomly generated enemies are the same for every player in a multiplayer room. Default Multiplayer uses the same speed settings as Standard Singleplayer.


#### Multiplayer Enemy Stock

Once enemies land into a player's stock, they do not immediately spawn yet.


##### Spawning

Enemies in stock spawn when the owner of the stock submits an incorrect (a valid answer but there is no enemies that match the answer) or invalid answer. Enemies in stocks will spawn all at once. This means that if you have a enemy stock of `30` and submit an incorrect answer, 30 new enemies will instantly spawn on your playfield.

Enemies in stocks spawn at `sPosition = 1`.


##### Cancelling

You can "cancel" (reduce) the amount of enemies in your stock by killing your current enemies. The number of enemies you cancel for each enemy killed uses the same formula as the send-to-stock formula.

When killing an enemy, if there are enemies in your stock, the enemies that are supposed to be "sent" to other players will be used to cancel your stock at a rate of 1 to 1. However, if you successfully cancel your stock (i.e., `stock = 0`), the remaining enemies will be sent to other players, therefore adding to their stock.

---

## Technical Details

### Score Formula

There are two variables in the score/attack formula for Singleplayer/Multiplayer mode respectively. The variables are `combo` and `sPosition`.

#### `combo`

The combo is how many enemies you have managed to kill consecutively. 

For each enemy killed, your combo time will be set back to the highest combo time, which drops down as time passes, and you earn +1 combo.

Note that `combo` starts at `-1`, which means that you have to kill 2 enemies to get a combo of `1`.

When your timer runs out, the combo resets back to `-1`.

#### `sPosition`
Due to the number of different window dimensions this game can be played on, calculating how far an enemy is from your base from the number of pixels on your screen would not lead to consistent results. 

As such, a measurement called `sPosition` is created. When an enemy first spawns, that is, when the enemy is at the topmost position, its `sPosition` is `1`, and when an enemy reaches your base, its `sPosition` is `0`.

---

## Implementation
Mathematical Base Defenders is written primarily using TypeScript. 

It also uses `Node.js` for server-side code, `uWebSockets.js` for bidirectional communication of game data, and `PixiJS` for drawing graphics.

---

## Contributing
Contributions and comments are welcome. File an issue or open a pull request, and the maintainer will take a look at it. 

Contributing also gives a special rank to your user account.

---

## Social Media
Mathematical Base Defenders is also on social media!
- Discord Server: [https://goto.mistertfy64.com/mbddc](https://goto.mistertfy64.com/mbddc)
- Facebook: [https://facebook.com/mathematicalbasedefenders](https://facebook.com/mathematicalbasedefenders)
- Instagram: [https://instagram.com/mathematicalbasedefenders](https://instagram.com/mathematicalbasedefenders)
- X (Twitter): [https://x.com/MathematicalBD](https://x.com/MathematicalBD)

---

## Donations
Donations are always welcome! Either sponsor mistertfy64 through GitHub or donate to him through Patreon.

**Please note that donations do NOT give gameplay perks.**

**Donations give cosmetic perks, however, these aren't implemented yet. If you want these once they're implemented, contact the maintainer.**
