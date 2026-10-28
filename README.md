# Nova V2.4 (Input Buffer)

**An input buffer for Geometry Dash** (Geode mod) by **AlQuerez23**. Discord: **alquerez23**

Clicked a hair too early? Instead of dying, the click waits for the first moment it's safe and goes through then.

## How it works

1. **Every click is checked before the game uses it.** The mod runs your click on a hidden copy of your player and plays the next moment forward: your jump, gravity, orbs, pads, portals, moving objects.
2. **Safe click?** It goes through right away, untouched.
3. **Deadly click?** It's held, and the mod finds the **earliest tick where the same click survives**. It fires there, as long as that's inside your stage's window.
4. **Can't be saved?** It goes through as you made it.

A few rules it always keeps:

- Clicks only ever move **later**, never earlier. Nothing is ever pressed for you.
- Every input is kept: double taps, releases and hold lengths survive.
- Works with or without **Click Between Frames**, at any TPS (60, 240, 480+).
- Held clicks follow their plan: the path is predicted once when you click, then only checked each tick, so it stays light on CPU and keeps input lag low.
- Platformer levels are left alone.

## Stages

One setting, **Stage**, picks how early a click can be and still get saved. Frames are 60fps frames (1 frame = 16.7 ms), the same at any TPS.

| Stage | Saves clicks up to |
|-------|--------------------|
| Off | nothing (raw input) |
| Stage 1 | 1 frame early |
| Stage 2 | 2 frames early |
| Stage 3 | 3 frames early (2 for ship) |
| Extreme | 20 frames early (12 for wave, 2 for ship) |
| Custom | your own values for each gamemode, set in Tuning (Stage tab) |

Extreme and Custom also re-plan held clicks live, every tick, so long holds stay safe. **Tuning** (Stage tab > Custom > Open Tuning; Custom only), per gamemode with your icons: *Tick Tuning* sets Min / Max, the smallest shift a click gets and the latest it can ever go in (240 ticks a second, 4 = 1 frame); *Click & Release* sets how early a click can be (0.5 to 30 frames), and a release on ship, wave and robot. **Export** saves your tuning to a file to share; **Import** loads one. **F6** cycles through the stages (you can change the key in the mod settings).

## The window

**Left Alt** shows / hides it (change it in the settings: *Window Key*). You can also use the **Nova button** in the pause menu (green circle with the target icon), which is the way on phones; the window is bigger there too. The tabs are in the sidebar on the left.

- **Log**: what the buffer did with each click: buffered, fired, raw, deaths. On Windows, **console** opens it in its own command-prompt window instead.
- **Stats** (hidden: click the version badge 5 times): prediction accuracy, your rhythm, windows, performance, and your system. The same 5 clicks show the **Dev** tab (live details to send when something's off).
- **Stage**: pick the stage, the options (Log: more detail), and your Custom values at a glance - Open Tuning sets them per gamemode: Tick Tuning (Min / Max ticks) or Click & Release (frames). Modes switched fully off are greyed out.
- **Modes**: switch the buffer on or off per gamemode.
- **Tools**: Your Path (in practice, the clicks you live a second past and the line you flew are saved, and every run adds on; an early click later waits for that spot), Show rays (your hitbox, the press / release paths, a live pathfinder and what the buffer thought, as lines in the level), Show path (your path only: the line you flew and your clicks), your saved stats, and Export report (one file with everything, to send when something's off).

## Versions

✅ = works on that platform, ❌ = not available there

<!-- versions:start -->
| Version | Platform | Works |
|---------|----------|:-----:|
| **v2.4.3** | Windows | ✅ |
|  | macOS | ✅ |
|  | iOS | ✅ |
|  | Android | ✅ |
| **v2.4.2** | Windows | ✅ |
|  | macOS | ✅ |
|  | iOS | ✅ |
|  | Android | ✅ |
| **v2.4.1** | Windows | ✅ |
|  | macOS | ✅ |
|  | iOS | ✅ |
|  | Android | ✅ |
| **v2.4.0** | Windows | ✅ |
|  | macOS | ✅ |
|  | iOS | ✅ |
|  | Android | ✅ |
<!-- versions:end -->

<!-- whats-new:start -->
## What's new in V2.4

### v2.4.3
- iOS Crash Fixes
- Dash orb Fix
- Learn From Attempts readded
- Log > Wave
- Updates now found when GAPI is busy

### v2.4.2
- Updates are now pulled every 5 minutes

### v2.4.1
- Misc Bug Fixes
- Settings Redesign (bottom left)

### v2.4.0
- Tuning: Custom per gamemode, with Import / Export
- Your Path: early clicks wait for where you clicked and lived
- Show Path: the line you flew and your clicks, in the level
- Autoplay (Beta) - Dev tab: click the version 5 times
- Cleaner rays, smoother animations, new easter eggs

**Bug fixes**
- Custom Min / Max no longer go back to 1 when you change stage, and save the moment you change them.
- The Modes tab's icons (and the easter-egg gamemodes) change as soon as you pick new icons or colours in the garage.
- Show Rays: your hitbox and the label above you follow you every frame (they lagged behind you).
- Autoplay clicks in the middle of the safe timings, with room from hazards (it clicked too early or too late).
- Autoplay / pathfinder: blocks away from the screen are solid again (a far-off ship flew through them).
- The version next to NOVA always matches the version installed.
<!-- whats-new:end -->

Every version's full changes are in [changelog.md](changelog.md).
