## 0.4.13
2025-03-13

### New Features
- (Default) Multiplayer mode's status "indicator", last game results "indicator", and chat has been redesigned and added with new features. ([#128](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/128))
  - Names in the user interface are now colorized according to player rank. ([#124](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/124), [#125](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/125))
  - You can now click on the username of a registered player's name in the user interface to view that player's stats. ([#123](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/123), [#126](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/126))
    - This also works for your "name card" on the top-right corner of the screen.
- Opening screen that now allows for easy authentication at game startup, instead of having to find it in the Settings menu. ([#120](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/120))
    - Therefore, signing in is no longer possible in the Settings menu.
### Changes
- Changed how opponent playfields are rendered in (Default) Multiplayer mode. ([#127](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/127))
- Toast notifications now slide in instead of just simply appearing on-screen.
### Fixes
- Added more arrow key navigation destinations and missing arrow key navigation destinations ([#129](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/129))
- Clickables now have the `pointer` cursor instead of the `default` cursor, allowing clear distinction of what can/can't be clicked. ([#130](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/130))
- Other bug fixes that I forgot lol ([#117](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/117))
### Miscellaneous Changes
- General refactoring of codebase and components. ([#112](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/112), [#114](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/114), [#115](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/115), [#116](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/116), [#118](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/118),[ #119](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/119), [#122](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/122))
- Better accessability ([#131](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/131))
- Updated test suites ([#132](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/132))
- Updated dependencies, including but not limited to: updating PixiJS to version 8.
  
---
## 0.4.12
2024-11-24

### New Features
- Added a global chat, which is located opposite to the status tray. ([#101](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/101))
  - There are currently no filters on the global chat, but things may change if they don't go as planned.
- Added custom backgrounds. ([#106](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/106))
- Added a quick method to log in while logged out. ([#107](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/107))
### Changes
- Changed it so that there is always at least one enemy on the playfield at any given time ([#109](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/109))
  - In other words, if you killed every enemy on your playfield, one will immediately spawn.
  > I believe this would make the "flow" harder to break as you no longer have to wait (e.g.) 2500ms for the next enemy and the "fun" harder to break when you lose all your Combo. —mistertfy64
- Changed the UI's font to `Noto Sans`.
  - However, gameplay font (enemies and input) are still `Computer Modern Unicode Serif`.
- Added `en-US` locale formatting to most numbers.
  - This includes commas on numbers. ([#103](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/103))
  - Additionally, most floats are now 3 decimal places.
- Made the Singleplayer Game Over screen look *slightly* better. ([#102](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/102))
- Attempted to better harden authentication security ([#110](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/110))
- Once again, due to location differences, rate-limiting that disconnects the socket limit is now quintupled.
### Fixes
- Fixed *some* of the keyboard navigation issues. ([#104](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/pull/104))
- Additional bug fixes not mentioned here.

Well, this patch-level semver update took a "while" (3.5 months), didn't it? Sorry for the delay, the next update probably won't be that long, or not conforming to actually a patch-level semver update. This can be thought of as a large update, with changes to over 1,400 lines of code.

A considerable amount of time, effort, and resources when into this update that only one person worked on. If you like the game, consider recommending it to your friends, or consider supporting me finacially on GitHub Sponsors! If you find a bug, you could also help me by filing a new issue so that I could take a look at it.

Finally, while my code quality or game design quality isn't the best, I will be listening to your suggestions so that this game could improve. You can join the Discord server on the website or file an issue as well. 

Thank you for reading this far!
 —mistertfy64

---
## 0.4.11
2024-08-01

Stability Change: Made it so much more fewer WebSocket messages are sent, saving server resources and reducing chance of getting disconnected from keyboard mashing.
- Examples of when a WebSocket message is not sent is when there are already eight characters on the input field.
- However, the disconnection threshold has been lowered because of that. Still, try not to mash your keyboard without reason.

---
## 0.4.10
2024-07-27

Feature: Added a server system monitor that displays when the server is under high load.

Stability Change: Made it so that once a socket sends too many messages in a time period, it instantly gets disconnected.
- Therefore, **PLEASE DO NOT MASH YOUR KEYBOARD!**

Fix: Fixed text and bar alignment issues on buttons.

---
## 0.4.9
2024-06-17

Feature: Added a “how-to-play” text while in game screen.

- This will be hidden after 5 games in the session for the session, or you can hide it in the Settings menu.

Change: Beautiful Score Display is now enabled by default.

---
## 0.4.8
2024-05-10

Feature: Added arrow key navigation to user interface.

Feature: Brought back Beautiful Score Display and made it more beautiful.

---
## 0.4.7
2024-02-01

Change: Changed the default setting value for enemy width:height ratio from 1:1 to 2:1

Change: Allowed Enemy Speed Coefficient in Custom Singleplayer Mode to go down to 0.25 instead of 1.

Fix: Fixed a bug that clogs up logs.

---
## 0.4.6
2024-01-30

Change: Enlarged text in many areas.

Fix: Other players leaving multiplayer rooms should no longer display `#0 ??? ???` ranks

---
## 0.4.5
2024-01-16

Feature: Global Alerts
- These alerts are sent to all players when it is sent.
- For now, these only show up when someone gets a new personal best AND a Top 100 global rank.

Feature: Discord Server Alerts
- Just like Global Alerts, everytime someone gets a new personal best AND a Top 100 global rank, a message will be sent in the official [Discord server](https://discord.gg/pDTZvrTXm9)

Feature: Enemy Color Palettes
- You can now select between 3 different enemy color palettes, so that the enemy colors can "go in" together.
- Of course, the old enemy color options are still available.

Feature: Adjustable Enemy Scale
- You can now adjust the enemy scale (both the enemy and its text) from 100% up to 200%. This is to prevent unreadable text.

Change: Easy Singleplayer's enemy spawn interval is now 150ms (from 250ms).

Change: Easy Singleplayer's enemy spawn chance is now 7.5% (from 5%).

Change: Some buttons have had their text enlarged.

Change: Toast notifications (on the bottom right) now have different colored borders based on meaning.

Change: Enemies should now slide down/spawn from above the viewport, not spawned below the top.

Fix: Game Over screen results shouldn't be cut off if now.

Fix: Made text on some buttons wrap instead of clip. 

---
## 0.4.4
2024-01-02

Fix: Percentage to next level should update most of the time instead of racing against the database write operation now.

Fix: Custom Singleplayer Intermission buttons should not have extra borders now.

---
## 0.4.3
2023-12-01

Change: Add more information to Game Over screen.

Fix: New score submissions will now display APM.

---
## 0.4.2
2023-11-26

Fix: Enemies' increasing speed now show properly.

Fix: Custom Singleplayer games' base health will now no longer be set to 100 if set to something else.

---
## 0.4.1
2023-11-25

Fix: Made authentication work again. Sorry about that!

Fix: Game Over screen no longer shows `Global Rank #0`.

Fix: Game Over screen now show correct number of enemies spawned.

---
## 0.4.0
2023-11-24

_This update is very large and will likely cause problems. If there are problems present, please [create an issue on the GitHub repository](https://github.com/mathematicalbasedefenders/play.mathematicalbasedefenders.com/issues)._

Feature: Singleplayer gamemodes (both Easy Singleplayer and Standard Singleplayer) now have new mechanics:

- Levels: Kill enough enemies to advance a level. In higher levels, enemy spawn time interval decreases, enemy moves faster, decreases base health regeneration amount, but you get more points.
- Base Health Regeneration: Every second, if your base health is below the maximum limit, it will regenerate.

Feature: Added a 3-mode current level display in Singleplayer games.

Change: Changed the UI on larger screens: added a logo, made buttons have a different layout, etc. (Note: Smaller screens still have a similar layout before this update.)

Change: *Finally* added a 404 page.

Change: Most game statistics (excl. score) now show 3 decimal places.

Change: Added a [CSS reseter](https://necolas.github.io/normalize.css/).

Change: Refactored code.

Change: Added a link to the accompanying website on the Welcome pop up.

---
## 0.4.0-rc.8 (1,000-day anniversary update)
2023-07-13

Feature: Score-gain Popups

Feature: Pop-up modals

---
## 0.4.0-rc.7
2023-04-28

Feature: Client-side rendering
- Before this release, all rendering is done only after the server sends out game data (around 60 times per second, ~36KB/s for empty Singleplayer field).
  - This may have caused problems for players with slow internet/when there is high traffic, due to the rendering function only being able to trigger when data is received from the server.
- This release makes it so that the browser can now render game data by itself without having to rely on the server, while still receiving data from the server in order to synchronize the game state between the server and the browser.
  - In other words, the browser will now calculate what the next frame would look like without needing data from the server, and will render that.
  - Because of this functionality and other factors, the server now sends out game data at 5 times per second, hopefully to reduce bandwidth usage.
- This is experimental, but it will probably be kept to fix performance issues, but it might create new problems. If that happens, please contact mistertfy64 and/or file an issue.


Change: Slowed down the enemy speed from 0.15 units per second to 0.1 units per second.


Change: Doubled the enemy speed in Easy Singleplayer mode. (now 0.05 units per second)


Change: Temporarily disabled Beautiful Score Display.


Change: Added a notice when connection is lost.


Change: A database is no longer required for selfhosting/contributing.
- Note that without a database, user accounts and score submissions can not be used.

---
## 0.4.0-rc.6
2023-04-17 

Feature: Custom Singleplayer Mode

- As of release, you can set your starting base health, the combo time, the enemy spawn trigger time, the enemy spawn trigger chance, the enemy speed and the forced enemy spawn trigger time. (All times are in milliseconds.)
- Note that setting the values to be an invalid value, an extremely high value, or an extremely low value will cause the game to refuse to start.
- Scores from custom game modes do not submit nor allow you to earn experience points.

Fix: Added back favicon.

---
## 0.4.0-rc.5
2023-04-11

Fix: Made the text on the results screen not overflow.

---
## 0.4.0-rc.4
2023-04-09

Feature: Multiplayer

Feature: An option for wider enemies. Use this if you have trouble reading text on square enemies.

Change: Made enemy spawning more forgiving once again.

Change: Added a "forced" enemy spawn clock. If no enemy has spawned for some time, an enemy will be spawned. This is to prevent your combo timer running out.

Change: Added player names below playfields.

---
## 0.4.0-rc.2
2023-03-25

Feature: The user information modal now shows the origin of the server you're connected to.

Change: Disabled font ligatures.

Change: Made the on screen keyboard use `−` (`\u2212`) instead of just a hyphen.

Fix: Hopefully fixed the case where deleting a room might cause the whole app to crash.

Fix: Fixed the buttons in the settings menu from having a top border

Fix: When typing an answer with more than one minus sign, all minus signs instead of just the first minus sign will use `−` (`\u2212`) instead of a hyphen.

---
## 0.4.0-rc.1
2023-03-08

**Change: You now solve math equations instead of creating math equations on enemies.**

Change: Revamped user interface.

Change: Enemies now fall instead of moving left.

---

<details><summary>Tiled (Pre-Reversal/Old Gameplay) Era</summary>
  
## 0.3.0-beta.4
2022-10-18

New Experiemental Feature: Enemies can now be "stacked". This is merely just a visual change and doesn't *directly* affect gameplay. When this feature is enabled, overlapping enemies will instead be displayed in a stacked manner. This is to fight with the issue of enemies blocking requested values of other enemies.

**Change: Slowed down the enemies on Easy and Standard Singleplayer again, this time by 75%**

Change: Instead of Easy mode having a constant enemy limit, the enemy limit will now grow linearly, starting at 5 enemies, adding 1 to the limit every 30 seconds after 60 seconds, stopping at 25.

Change: Added an intermission screen for non-custom Singleplayer game.

Change: Added icons to main menu buttons.

Change: Game Instances can now be scaled and/or moved (indirectly).

Fix: Combo text incorrectly showing/hiding

Fix: Skipping splash screen text is no longer limited to having to click the text instead of anywhere on the screen.

---
## 0.3.0-beta.3
2022-10-06

Change: Added keybind presets.

Change: Added more items in user modals.

---
## 0.3.0-beta.2
2022-09-11

New Feature: You can now earn experience points when playing Multiplayer games.

- Currently, it has a flat rate of 1 experience point for every second you survive.
- Additionally, winning a multiplayer game gives you 50% more experience points.

New Feature: The game will now count the number of Multiplayer games you counted/won. You need to be registered for the game to count.

New Feature: You can now control how much information is displayed in the user interface while in game.

Change: Refactored some code, but it still looks terrible.

Fix: Chat now goes in the "correct" direction now.

Fix: Modal buttons should now look more good.

Fix: Users can no longer send messages with whitespaces only.

Fix: Removed the "Double Everything" ~~bug~~ event.

---
## 0.3.0-beta.1
2022-08-14

**New Features**

You may now report users. Note that you must be registered, haven't reported someone in the last 5 minutes, and actions will be taken on your account if you misuse it. You can always send an e-mail if you don't want to register and would like to report.

**Changes**

Under your and your opponents' game instance(s), names are now colored according to rank.


---
## 0.3.0-beta
2022-07-07

*Note: This update is big, and will likely cause problems. If you find problems, please report them to the Game Master.*

**Changes**

Changed WebSocket implementation, therefore, code is rewritten.

---

## 0.3.0-alpha.14
2022-05-28

**New Features**

Discord Server webhooks now display other stats of your Top 50 game rather than just the scores.

**Changes**

Made it explicitly clear that Mathematical Base Defenders is in development.

Huge server-side refactoring.

Bug fixes.

---

## 0.3.0-alpha.13
2022-04-05

**New Features**

Personal bests and the Leaderboards now saves and shows other stats of your game rather than just the scores.

**Changes**

Bug fixes.

---

## 0.3.0-alpha.12
2022-03-27

**New Features**

Custom Singleplayer Mode. It's pretty much self-explanatory. Scores will not be submitted nor you will earn experience points in Custom Singleplayer Mode.

Every time someone gets a score on the Top 50 (Easy or Standard Singleplayer), a message will be sent to the [Discord Server](https://discord.gg/tJdwzjSgHh).

**Changes**

Bug fixes.

---

## 0.3.0-alpha.11
2022-03-18

Fixed a bug with the rewritten code.

---

## 0.3.0-alpha.10
2022-03-17

Rewrote some code.

---

## 0.3.0-alpha.9
2022-03-16

New multipliers for combos in Singleplayer. For more information why this change was made, read this: https://mistertfy64.com/blog/post/2

Main menu now shows your general information if you logged in. If you haven't logged in, it will tell you to do so.

Bug fixes and minor improvements.

---

## 0.3.0-alpha.8
2022-02-20

New Easy Mode.

In Easy Mode:
- Combo time is 10 seconds instead of 5 seconds.

- The enemy spawn chance is 2.5× more rare than Standard Mode.

- Every enemy is 50% slower than Standard Mode.

- Only a maximum of 5 enemies can appear on the playfield.

- Only 50% Experience Points is awarded compared to the Standard Mode.


---

## 0.3.0-alpha.7
2022-02-03

New toast notification system. (These only show when you click on the Statistics button or someone gets Top 50 for now.)

Bug fixes and minor improvements.

---

## 0.3.0-alpha.6
2022-01-23

New leveling system.

Bug fixes and minor improvements.

---

## 0.3.0-alpha.5
2022-01-13

Bug fixes.

---

## 0.3.0-alpha.4
2022-01-09

Made multiplayer look more real-time by adding other players' statuses on the screen. (Please note that this is in its first stage, and hasn't been tested lol, so it will probably break)

---
## 0.3.0-alpha.3
2022-01-03

Better support for non-PC devices or devices with weird screen resolutions.

---
## 0.3.0-alpha.2
2021-12-30

Bug fixes, improvements, and server-side changes and improvements.

---
## 0.3.0-alpha.1
2021-12-24

**New Features**

You can now set a picture to be the background for EVERY enemy.

Pressing Tab now shows you a status bar.

**Changes**

Removed the text compression algorithm, making the game almost 20x faster and 3x more expensive. (bruh)

Bug fixes, improvements, and server-side changes and improvements.

---
## 0.3.0-alpha
2021-11-26

**New Features**

Multiplayer*!!!!!!!!!!!!

*Please note that the game is only developed by 1 person, therefore, only 1 person tested it. Multiplayer is also in its very early stage. If there is a bug or a problem (there probably will), please [report it to the Game Master!](https://github.com/mathematicalbasedefenders/issuetracker)

**Changes**

When playing the game at a weird window size (e.g. width is lower than height), the game will be centered instead of staying at the top.

Bug fixes, improvements, and server-side changes and improvements.

---
## 0.2.1
2021-10-23

Bug fixes. Improvements.

---
## 0.2.0
2021-09-23

New UI design.

You can know rebind keys. Note that one key can be used per tile, and each tile may can only have one key bound to it.

---
## 0.1.1
2021-09-23

Fixed a bug with restoring settings.

---
## 0.1.0
2021-09-22

Initial release of the web version of Mathematical Base Defenders.
<details>
