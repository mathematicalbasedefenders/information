## 0.4.0-rc.2
25 March 2023

Feature: The user information modal now shows the origin of the server you're connected to.

Change: Disabled font ligatures.

Change: Made the on screen keyboard use `−` (`\u2212`) instead of just a hyphen.

Fix: Hopefully fixed the case where deleting a room might cause the whole app to crash.

Fix: Fixed the buttons in the settings menu from having a top border

Fix: When typing an answer with more than one minus sign, all minus signs instead of just the first minus sign will use `−` (`\u2212`) instead of a hyphen.

---
## 0.4.0-rc.1
8 March 2023

**Change: You now solve math equations instead of creating math equations on enemies.**

Change: Revamped user interface.

Change: Enemies now fall instead of moving left.

---

<details><summary>Tiled (Pre-Reversal) Era</summary>
  
## 0.3.0-beta.4
18 October 2022

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
6 October 2022

Change: Added keybind presets.

Change: Added more items in user modals.

---
## 0.3.0-beta.2
11 September 2022

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
14 August 2022

**New Features**

You may now report users. Note that you must be registered, haven't reported someone in the last 5 minutes, and actions will be taken on your account if you misuse it. You can always send an e-mail if you don't want to register and would like to report.

**Changes**

Under your and your opponents' game instance(s), names are now colored according to rank.


---
## 0.3.0-beta
7 July 2022

*Note: This update is big, and will likely cause problems. If you find problems, please report them to the Game Master.*

**Changes**

Changed WebSocket implementation, therefore, code is rewritten.

---

## 0.3.0-alpha.14
28 May 2022

**New Features**

Discord Server webhooks now display other stats of your Top 50 game rather than just the scores.

**Changes**

Made it explicitly clear that Mathematical Base Defenders is in development.

Huge server-side refactoring.

Bug fixes.

---

## 0.3.0-alpha.13
5 April 2022

**New Features**

Personal bests and the Leaderboards now saves and shows other stats of your game rather than just the scores.

**Changes**

Bug fixes.

---

## 0.3.0-alpha.12
27 March 2022

**New Features**

Custom Singleplayer Mode. It's pretty much self-explanatory. Scores will not be submitted nor you will earn experience points in Custom Singleplayer Mode.

Every time someone gets a score on the Top 50 (Easy or Standard Singleplayer), a message will be sent to the [Discord Server](https://discord.gg/tJdwzjSgHh).

**Changes**

Bug fixes.

---

## 0.3.0-alpha.11
18 March 2022

Fixed a bug with the rewritten code.

---

## 0.3.0-alpha.10
17 March 2022

Rewrote some code.

---

## 0.3.0-alpha.9
16 March 2022

New multipliers for combos in Singleplayer. For more information why this change was made, read this: https://mistertfy64.com/blog/post/2

Main menu now shows your general information if you logged in. If you haven't logged in, it will tell you to do so.

Bug fixes and minor improvements.

---

## 0.3.0-alpha.8
20 February 2022

New Easy Mode.

In Easy Mode:
- Combo time is 10 seconds instead of 5 seconds.

- The enemy spawn chance is 2.5× more rare than Standard Mode.

- Every enemy is 50% slower than Standard Mode.

- Only a maximum of 5 enemies can appear on the playfield.

- Only 50% Experience Points is awarded compared to the Standard Mode.


---

## 0.3.0-alpha.7
3 February 2022

New toast notification system. (These only show when you click on the Statistics button or someone gets Top 50 for now.)

Bug fixes and minor improvements.

---

## 0.3.0-alpha.6
23 January 2022

New leveling system.

Bug fixes and minor improvements.

---

## 0.3.0-alpha.5
13 January 2022

Bug fixes.

---

## 0.3.0-alpha.4
9 January 2022

Made multiplayer look more real-time by adding other players' statuses on the screen. (Please note that this is in its first stage, and hasn't been tested lol, so it will probably break)

---
## 0.3.0-alpha.3
3 January 2022

Better support for non-PC devices or devices with weird screen resolutions.

---
## 0.3.0-alpha.2
30 December 2021

Bug fixes, improvements, and server-side changes and improvements.

---
## 0.3.0-alpha.1
24 December 2021

**New Features**

You can now set a picture to be the background for EVERY enemy.

Pressing Tab now shows you a status bar.

**Changes**

Removed the text compression algorithm, making the game almost 20x faster and 3x more expensive. (bruh)

Bug fixes, improvements, and server-side changes and improvements.

---
## 0.3.0-alpha
26 November 2021

**New Features**

Multiplayer*!!!!!!!!!!!!

*Please note that the game is only developed by 1 person, therefore, only 1 person tested it. Multiplayer is also in its very early stage. If there is a bug or a problem (there probably will), please [report it to the Game Master!](https://github.com/mathematicalbasedefenders/issuetracker)

**Changes**

When playing the game at a weird window size (e.g. width is lower than height), the game will be centered instead of staying at the top.

Bug fixes, improvements, and server-side changes and improvements.

---
## 0.2.1
23 October 2021

Bug fixes. Improvements.

---
## 0.2.0
23 September 2021

New UI design.

You can know rebind keys. Note that one key can be used per tile, and each tile may can only have one key bound to it.

---
## 0.1.1
23 September 2021

Fixed a bug with restoring settings.

---
## 0.1.0
22 September 2021

Initial release of Mathematical Base Defenders.
<details>
