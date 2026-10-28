# Nova V2.4 (Input Buffer)

**By AlQuerez23.** Discord: **alquerez23**

Clicked a hair too early? Instead of dying, the click waits for the first moment it's safe and goes through then.

## How it works

- Every click is checked first: the mod plays it forward on a hidden copy of your player (jumps, orbs, pads, portals, moving objects).
- **Safe click:** goes through right away, untouched.
- **Deadly click:** held, then fired on the earliest tick where it survives, as long as that's inside your stage's window.
- **Can't be saved:** goes through as you made it.
- Clicks only move later, never earlier, and nothing is pressed for you. Double taps, releases and hold lengths are kept.
- Works with or without Click Between Frames, at any TPS. Platformer is left alone.

## Stages

How early a click can be and still get saved (60fps frames, 1 frame = 16.7 ms):

- **Off:** nothing (raw input)
- **Stage 1:** 1 frame early
- **Stage 2:** 2 frames early
- **Stage 3:** 3 frames early (2 for ship)
- **Extreme:** 20 frames early (12 for wave, 2 for ship), with live re-planning
- **Custom:** your own values for each gamemode, set in Tuning (Stage tab)

**Tuning** (Stage tab > Open Tuning, Custom only): *Tick Tuning* sets each gamemode's Min / Max shift (4 ticks = 1 frame); *Click & Release* sets how early a click / release can be (0.5 to 30 frames). Export / Import save and load a tuning as a file.

**F6** cycles the stages.

## The window

**Left Alt** shows / hides it (or the key you set as Window Key). Or the **Nova button** in the pause menu (green circle with the target icon), the way to open it on phones.

- **Log:** what happened to each click (Windows: or in a console window)
- **Stats** (click the version badge 5 times): accuracy, your rhythm, windows, performance, your system
- **Stage:** stage, options, your Custom values at a glance (Open Tuning: per gamemode)
- **Modes:** buffer on / off per gamemode
- **Tools:** Your Path, Show rays, Show path, your saved stats, Export report

## Online users

The top of the window shows how many people are online and offline. Each game sends the Nova server an anonymous random ID every 90 seconds, nothing else. Turn it off with the **Show Online Users** setting.

## Platforms

**V2.4 works on:** Windows, macOS (Apple Silicon and Intel), iOS and Android (32 and 64-bit).

The full version list is in the Changelog tab.
