# Changelog

## v2.4.3
- iOS Crash Fixes
- Dash orb Fix
- Learn From Attempts readded
- Log > Wave
- Updates now found when GAPI is busy

## v2.4.2
- Updates are now pulled every 5 minutes

## v2.4.1
- Misc Bug Fixes
- Settings Redesign (bottom left)

## v2.4.0
- Tuning: Custom per gamemode, with Import / Export
- Your Path: early clicks wait for where you clicked and lived
- Show Path: the line you flew and your clicks, in the level
- Autoplay (Beta) - Dev tab: click the version 5 times
- Cleaner rays, smoother animations, new easter eggs

### Bug fixes
- Custom Min / Max no longer go back to 1 when you change stage, and save the moment you change them.
- The Modes tab's icons (and the easter-egg gamemodes) change as soon as you pick new icons or colours in the garage.
- Show Rays: your hitbox and the label above you follow you every frame (they lagged behind you).
- Autoplay clicks in the middle of the safe timings, with room from hazards (it clicked too early or too late).
- Autoplay / pathfinder: blocks away from the screen are solid again (a far-off ship flew through them).
- The version next to NOVA always matches the version installed.

### More
- Tuning (Stage tab > Open Tuning): the Custom stage per gamemode, with your icons - Tick Tuning (Min / Max ticks) or Click & Release (how early a click / release can be). Modes switched off are greyed out; your old Custom values carry over. Export saves your tuning to a file to share; Import loads one.
- Your Path keeps every input: two of yours on one attempt are always two spots (quick ones - ship, wave, fast taps - were joined into one, so a quarter of a level showed ~16). Forget Path and play it again to fill in a level from before.
- Your Path (Tools): in practice, every click you live past (Counts After, 1 s by default) and the line you flew are saved for the level, and every run adds on. Later an early click waits for your spot, when the prediction says it lives there. Forget Path clears it.
- Show Path (Tools): your path in the level - its line and a dot at each click (press cyan, release pink), gone the moment you pass it. With Show Rays on too: your path where it goes, the rays past it.
- Stage 4 is gone: Stage 4 users move to Stage 3 (Custom and Tuning cover anything in between).
- Orb buffering is built in (the Orb Helper switch is gone): a press just before an orb waits and goes in the tick you touch it, when that gets you through. Log > Orbs shows every decision.
- Show Rays: thinner, cleaner lines, and inputs as small dots.
- Autoplay (Beta, Dev tab - click the version 5 times): Use Path plays your path where it goes; Remember is called Memory.
- What's New: after an update - and on a first install - the window opens once with this version's changes; Stage > Quick > Changelog brings them back any time.
- Extreme is a vivid version of your accent colour. The window and Tuning settle in smoothly instead of bouncing.
- Click N, V or A in NOVA: one of your gamemodes (not the swing) comes out of a wormhole just off the window and runs across it with its own GD physics - jumps, flaps, gravity flips, teleports - landing on the buttons and tabs (the ship, UFO and wave fly freely over everything; the wave leaves its trail the whole way), a different way every time, then dives into another wormhole. (It no longer turns up on its own.) And four new easter eggs to find - hints: the O (click it again and again), a word, the late-night sky, and something rare.
- Removed, code too: Level Scan, Learn From Attempts (and Forget Level), autoplay's Learning Run and Noclip, theme presets.

## v2.3.0
- Nova look, round 2 (2.2 Nova):
  - Settings: a round button with a cog, bottom right next to the online count (the cog turns under the mouse). The gear at the top of each page is gone; page names sit back at the left.
  - Sidebar: the logo without its purple square, the version as plain violet text (no bubble; still 5 clicks for Dev mode), the galaxy and the sidebar's old stars removed (code too).
  - NOVA is a real neon sign: each letter is a bright tube with a tight glow and a wide bloom made from the letter itself (blurred, not a bigger copy). It hums softly, a letter flickers on and burns bright under the mouse, and the whole sign flickers on when the window opens. The O is a ring galaxy (blue-white inner edge, violet and pink dust, stars, a warm core) that slowly turns, faster under the mouse.
  - Space background: the shooting stars are gone (code too). Behind the page: slow parallax stars in three depths that twinkle, a few four-point sparkles, and soft violet / blue / pink nebulae that breathe. A few slow stars in the sidebar too.
  - Card outlines glow: when a tab opens, each section's outline lights up violet one after another and settles to a soft glow; the section under the mouse glows brighter. A light also runs along the line under the page name. The light that ran round the window's edge is removed (code too).
  - Nova Run (replaces the icons running across the bottom of the sidebar): a little GD level in its own framed box under the tabs. One of your icons at a time - cube, ship, ball, UFO, wave or swing, your icons and colours - goes through GD-style obstacles (spikes, blocks, pillars, wave slopes), then a portal: the gamemode changes and so do the obstacles and the background colour. Every section is beaten by its own inputs - the path is made first and the obstacles are placed where it leaves room (checked by tests/course_tests.cpp: 2520 sections, no hits). Click the icon and it explodes and goes again from the section's start ("Attempt 2").
  - Modes tab rebuilt: a tile per gamemode with your own icon for it (ship and UFO with your cube in them), a Normal | Mini switch under it, and click the icon to switch both. Off modes go grey; a dot shows on / half / off; the count of buffered modes is at the bottom with All On / All Off.
  - Easter egg: every 10 seconds there's a 1 in 5 chance a rocket with your cube in the porthole lands on the window (on top of it, or on the footer line if the window is at the top of the screen) - engine fire trailing on the way down, smoke on touchdown, a little squash, then it takes off again. Click the logo to call one; click a landed rocket to send it off.
  - The window is a little taller and the sidebar a little wider: more room in every card (Stage, Tools), and room for Nova Run. The Log's Console / Clear buttons sit left of the online count.
- Nova look, round 3:
  - GD's real gamemode portals in Nova Run: the coloured ring with a white edge, the black drum with its blue grille behind it, the half-round tab with the mode's symbol, the dots, and squares of its colour drifting off it - green cube, pink ship, red ball, orange UFO, cyan wave, yellow swing, white robot, purple spider.
  - Robot and spider added to Nova Run (8 gamemodes now). Robot: GD's held jump - short taps over spikes, long holds over pillars and up steps, fire under its feet while the jump is held, no ceiling. Spider: teleports between floor and ceiling (walking the ceiling upside down), with a line of light where it jumped. Both use GD's running animation when the sprite has it (the names it has are written to the log once).
  - Trails like GD: ship / UFO / swing leave your trail in your second colour; the wave's solid trail is your second colour too (GD's default); cube, ball, robot and spider have no trail, just squares off the surface they run on. Ship fire out of its back while you hold, swing fire on the side it's pushed from, robot fire under its feet. (The ball and swing no longer burst on every click - GD doesn't.)
  - Sidebar: the logo is gone (code too); NOVA is bigger at the left, "Input Buffer" under it, and V2.2 glows like the sign (brighter under the mouse).
  - Stage: the Quick card's All Settings tile is gone - the cog does that.
  - Extreme looks like the top stage: a hot pink button with a glowing edge, a light sweeping across it, and embers rising off it while it's your stage; its name and the stage pill turn pink too.
  - The rocket is replaced by your robot: now and then it drops in at the left of the page and jumps across from button to button (and along the cards' tops) - fire under its feet on the way up, the button bounces when it lands - then off the right edge. Click NOVA to call it; click the robot and it explodes.
- Nova look, round 4:
  - The stage pill at the top right gets Extreme's look too when you're on Extreme: hot pink, glowing edge, the sweep and the embers.
  - Sidebar header: NOVA bigger with V2.2 right beside it, "by AlQuerez23" centred under them (the "Input Buffer" line is gone); the sidebar is a little wider for it. The galaxy O's halo is smaller.
  - Modes tab: no more box behind the icon under the mouse - a round violet light instead.
  - Nova Run spider: its teleport leaves GD's white streak (thin where it left, wide where it arrived) and a faint ring where it left.
- Custom Min / Max are reset whenever you pick any stage other than Custom (they only ever applied to Custom).
- Ship straight fly: a ship input queued behind a held one now fires exactly on its schedule - your tap keeps the length you made it. Since releases got the same live check as presses, a release in a straight fly could wait for a "safe" tick, which turned the tap into a longer hold and the ship rose by itself.
- Level scan / buffer, GD techniques:
  - Straight fly: the scan's ship can now tap (press, let go a tick later - saved as a press and its release) as well as hold, and flying at an angle costs it a little, so of the ways through it keeps the level, tapped one - like a player straight flying - instead of long holds. Same in A* (the stuck-spot search and Show Rays' pathfinder).
  - Buffer clicks: the scan's ball and spider can hold a press into the landing (it fires the moment they touch down, GD's buffer click), like the cube already could. (UFO and swing have nothing to buffer - every click acts in the air.)
  - Dual: the scan goes through dual parts. At a dual portal player 2 appears where player 1 is with gravity flipped (like GD), gets the same inputs, and has to live too; a solo portal takes it away. You can also start a scan inside a dual part. (2-player levels, where player 2 has its own button, still can't be scanned in dual.)
  - Mini wave: twice as steep, so the buffer holds a mini-wave input at most half as long (the same distance as a normal wave), and the scan / A* tell heights apart twice as finely there.
  - Slopes and speed portals: the wave rays are straight lines at one speed, so with a slope (the wave slides along it) or a speed portal in reach, the full simulation decides instead of the rays.
- "by AlQuerez23" moved out of the sidebar: NOVA and V2.2 alone up there (centred), and the empty Log says "Questions? Ask AlQuerez23 on Discord (alquerez23)."
- Snap To Scan finds the scanned (pink) line now: it checked your height against the height at the scanned input up ahead, which in a wave (45 degrees) is a different height, so it almost never matched. Now it checks you're on the line at your own x (within 12 px), then uses the next scanned press / release ahead (the prediction still has to put you on it and survive). Releases snap only while you're on the line - snapped from another path, wave releases came out late.
- Sidebar: the line and the tabs sit higher, closer to NOVA. The robot that jumps across the window is bigger.
- Robot releases: letting go ends the robot's jump boost, so a late release is a higher jump. A robot release is now held at most 2 frames (like the ship), and one queued behind a held press keeps exactly the hold you made.
- New scan method - the sprint. One hidden player plays the level with the button as it is; when it dies it goes back and tries the input one step earlier at a time (latest first, like a player clicking as late as is safe), keeping the first that lives well past the death with a little room from hazards. That's one simulation per stretch instead of dozens of versions every 2 ticks, so long levels finish. Where no input in its last second saves it, the old version search (beam, A*, tries) takes that spot from a second back, and the sprint carries on 3 blocks past it.
- Scan watchdog: a scan always finishes. A spot the version search hasn't got 1 block past in 8 seconds of scanning is gone through (marked unsolved in Export Scan) and the scan carries on.
- The mod is Nova now: id alquerez.nova (the file is alquerez.nova.geode), name "Nova". Geode keeps saved data per id, so on the first start Nova brings over Input Buffer's saved data once - stats, Custom frames, the online id, your settings (not the two keys - set those again) and the scans / learned spots / reports. Delete the old alquerez.inputbuffer.geode from the mods folder (both at once would both buffer your clicks).
- Sidebar: NOVA is centred between the top of the panel and the line under it (measured from the letters themselves); the tabs follow the line.
- Everything says V2.3 (the window, mod.json).
- Online count: you tell the server you're here every 1.5 minutes (was 2) and the totals are fetched when the window opens and every 30 seconds while it's up (not while you play - Cloudflare's free plan allows 100 000 requests a day), so everyone's numbers stay in step. Every version (Input Buffer 2.2 and Nova) uses the same server, so they all count. Server: "online" is now the last 3 minutes (server/worker.js - deploy it again with `npx wrangler deploy` in server/).
- Custom Max starts at 1 (like Custom Min), and goes back to 1 when you pick another stage.
- The mod's settings (the cog): the window steps aside and comes back by itself when you close them - on phones there was no key to bring it back.
- Double-click the page header: the window goes back to its starting spot (top right).
- The cog and the Window Key: while the mod's settings are open the key does nothing and nothing else brings the window up over them (it used to pop up over the settings, and the next press moved it); it comes back where it was when they close - also if you changed Window Size / Opacity in them.
- Nova Run looks like GD 1.0 (Every End's style): blocks have one clean white outline round the whole block and faint lines between its tiles, and every outline (blocks, spikes, the wave's slopes, floor and ceiling) is a smooth line - GD's own lines have no anti-aliasing, so diagonals came out as stairs. The wave's slopes are one straight line per run.
- Key names the window's font can't draw (some keyboards / Macs) no longer leave a blank: "  to toggle" says "the Window Key to toggle" instead.
- Nova Run gets Every End's background: big panels with gaps between them, two layers scrolling at different speeds behind the course, tinted with each section's colour. The sections use GD's own bright colours (blue cube, purple ship, crimson ball, orange UFO, ...), the blocks are a darker shade of that colour with glowing white outlines, and the spikes glow too.
- Nova Run always has a top: every section has a ceiling now, cube and robot too.
- Two windows fixed: if the old Input Buffer mod is still installed next to Nova, Nova uninstalls it on start (your data was already brought over) and asks you once to restart the game.
- The menu text says V2.3: the mod page's "works on" line, the README's versions table, and the settings (Window Key, Pause Menu Button, Window Size / Opacity, Show Online Users) say Nova instead of Input Buffer.
- The Discord tile glows and shines like Extreme (a pulsing blurple edge and a light sweeping across it).
- Custom, Export Report and Scan Level glow and shine like Extreme too, in Nova's violet (Custom's glow pulses brighter while it's your stage).
- Online count: closing the game (or a phone putting it in the background) tells the server right away, so you show as offline at once instead of up to 3 minutes later (server: new POST /bye). The totals refresh every 15 seconds while the window is open (was 30).
- Phones: the window is smaller - iOS and Android each have their own size (1.1x, was 1.5x), and on a phone it's never taller than half the screen, whatever Window Size says (PC: 90%). It's never wider than 70% of a phone's screen either - on iPad it was wider than the screen, so it could only be dragged up and down.
- Engine - escape search: "could you still save this yourself?" (the check that decides whether a ship / wave / robot / UFO / swing click that dies later is the click's fault) is a real search now. It tries up to 3 follow-up inputs a person can make - the first no sooner than your own rhythm, a few ticks apart - picking where to put them from where each try died (the try that got furthest is extended first), and the first follow-up has to still work a little late (no frame-perfect ways out). It used to try 1-3 guessed moments with one follow-up each (one per candidate in the delay search), so clicks you'd have saved looked deadly and got held back (late wave / ship releases), and every ship crash further than 100 ms out was called avoidable without a check. Up to 14 tests for your click as made, 4 per delay tried, 8 for the live re-check; out of tries = the old rule of thumb. Dev tab: "Escape search" counts.
- Engine - truer simulation: the hidden player turns (updateRotation) at the end of each step, after its collision check - GD's order (it turned before); its collision log is cleared like GD clears it (which object it touched on each side last - Click Between Frames does the same, "necessary for wave"); and it starts with your rotation (GD's own checkpoints keep it; it had the last test's). Scan states keep the rotation too.
- Show Rays: the two ghosts ("press now", "let go now" / "keep not pressing") look 1.5 s ahead - well past the screen - redone ~15x a second (they were one click's lookahead, a quarter to two thirds of a second); where a ghost would die its last stretch is red, with the X. The pathfinder looks 1.5 s ahead too (was 1 s).
- Removed: the escape check's sampling (escapeSamples) and the ship's "a crash past 100 ms isn't your fault" rule (SHIP_JUDGE_BASE), code and all.
- Portals in predictions (ship / wave focus): speed portals are applied the way GD does it - its own speed change for the player (updateTimeMod, no effects; the values ReSpeed documents: 0.7 / 0.9 / 1.1 / 1.3 / 1.6) - not just the speed number, and the cut-off checks use the new speed per tick. Gamemode portals no longer stop a prediction (setting "Predict Through Portals", on): it switches gamemode like the scan does and keeps itself inside the new floor / ceiling. Mirror portals only flip the picture, so they don't stop a prediction either. Gravity portals (yellow / blue / green) are counted in the Dev tab.
- Prediction check (setting, on): every 32 ticks the next 100 ms are predicted with the button as it is and followed against the real player tick by tick. Dev tab "Prediction (100 ms)": per gamemode ("+portal" when the prediction went through a portal) how often it's exact (within half a pixel), the average / worst miss, from which tick it goes off, and deaths it got wrong (false / missed). The first clear miss per gamemode goes in the Log with where it went off.
- Autoplay (Tools tab, a test): the mod plays the level itself with the buffer's own hidden-player physics - plans 0.5 s ahead (the button as it is when that lives, else the escape search finds where to press / let go), follows the plan tick by tick, plans again every quarter second. When you part from the plan it logs a "drift" (gamemode, how far, how many ticks in); when it dies it logs on what and whether the plan said you'd live there ("PREDICTION BUG" - what to fix) or it found no way through. Dev tab "Autoplay": plans, drifts, deaths per gamemode, the last notes. Your clicks are ignored while it plays; a level it played saves no progress (no %, no completion, no new best) until you leave it.
- Every prediction starts with the hidden player in your gamemode (switched before your state is copied): a prediction through a gamemode portal, or a level scan, used to be able to leave it in another one.
- Autoplay plans the whole way, before it gets there: a route is planned continuously from where you are toward the end of the level (up to 10 s ahead), with a slice of CPU every tick - like the scan's sprint: carry on as is, and where that dies try an input one step earlier at a time from just before the death back up to a second (latest first, the cleanest one); nothing saves it -> take the last input back and look before it (up to 8 times). It plays the route's button tick by tick and checks you against the route's states every tick (a drift = a prediction miss, logged, then it plans again from where you are). A death says whether the route said you'd live there ("PREDICTION BUG", with how far the route went on), where the route got stuck and why, or that planning hadn't reached that far. Past the route's end it falls back to the 0.5 s plan. Show Rays draws the route (violet) with its inputs; Dev tab "Route": how far ahead, inputs, restarts, tests.
- Off-screen collisions: GD only loads the level around the camera, so a hidden player further out gets no objects from GD and the mod's own list fills in. That list now goes in inside GD's collision step (just before it settles landing / ground - a hook on PlayerObject::postCollision), not after the step had finished: before, off screen the hidden player sank into blocks instead of landing on them - Every End's thin floor slabs: autoplay's route fell through the floor, everything past the screen looked deadly, and the route "gave up" (stuck everywhere). Predictions past the screen (Show Rays' ghosts, the pathfinder, the scan) use the same fix.
- Autoplay sends its inputs straight to the player (an input mod like Click Between Frames would re-time them and split the step), and counts whole steps (a split step no longer moves the route on twice).
- The hidden player knows where it was at the start of each step (m_lastPosition, which GD's step sets before moving you and its collision check uses to land you on a block you came down onto). It kept a stale one: on the first tick of every test it could sink into thin blocks instead of standing on them - Every End's 6 px floor slabs: autoplay's route fell through the floor at every new run (the violet line going down through the ground, the drifts "64t into the route ... the route in the air"), and the one-tick check was ~1 px off there.
- Autoplay's route tries an input on every tick before a death (was every 2nd: a press window can be one tick wide - FINAL DESTINATION's first spike). When it's stuck, the Log says how many inputs it tried over which stretch, what they died on, and - if the level scan has an input there - what that input does from the route's own state there (lives = the search missed it; dies = the hidden player sees that spot differently).
- Prediction check for inputs: right when an input goes in - yours as you made it, or one the mod sends ("(sent)") - the next 100 ms are predicted with it and followed against you tick by tick, per gamemode and press / release: "robot release", "ship press (sent)", ... in the Dev tab (exact %, average / worst miss, from which tick it goes off). That's where a release that's consistently off shows: how far, from which tick.
- Export Report has the Dev tab in it too (prediction checks, input timing, portals, autoplay, route).
- Input timing: the first result is always logged (also "0 ticks - on time"), not only a change.
- Show Rays while autoplay plays: only autoplay's route (violet) and its inputs - the pathfinder (and its blue / pink input marks, which aren't autoplay's) and the two ghosts are off, and the pathfinder doesn't run (CPU).
- GD's anticheat spike is never a death for the hidden player: GD puts an invisible spike where you start (to catch noclip) and ignores it - the predictions didn't, so at the start of every level the hidden player "died" (false deaths, and autoplay's route stuck at x 0 - both of your reports). Dev tab counts the ignored touches.
- Autoplay's route search carries on over the next ticks when its time is up (it used to give up and call that spot "stuck" - FINAL DESTINATION's first spike, which the scan solves), and it uses much less CPU: 0.7 ms a tick (0.25 ms when the route is 3 s ahead), 4 ms only when the route is under 0.5 s ahead (was 1.2 / 12 ms, and a search could take 48 ms) - it was very laggy.
- Autoplay drifts: logged at 1 px (once per route) with what you stand on (the block's top against your feet) and whether the route thought it was on the ground; it only plans again from 3 px (a 1 px difference standing on a block made it start over every second).
- New setting "Old Hidden-Player Step" (off): the hidden player steps the way it did before 2.3 (turns before its collision check, old collision record) - to compare the Dev tab's prediction checks with it on and off (Every End's 1 px one-tick miss standing on thin blocks).
- Input timing check (every input the mod sends - buffered or autoplay): right before it goes out, one tick is predicted with it and one without; when they clearly differ in y speed, the next ticks show which one really happened - on time, or 1-3 ticks late. Once 3 checks agree it's in the Log (orange when late: every buffered input lands that late) and the Dev tab ("Input timing", every check); autoplay sends its inputs that much earlier, the route and the quick plan both.
- Autoplay's route: when it's stuck it tries again every 30 ticks from where you are (the start of a level can look deadly for a moment - its start triggers haven't run yet; FINAL DESTINATION's start did that and it never tried again), and it waits 8 ticks after a respawn (was 4). "Route stuck" is logged at most 6 times a level.
- Autoplay in cube / ball / spider / UFO / swing taps (press, let go a tick later) instead of holding: its quick plan held the button after a press, and holding in cube re-jumps on every landing - it jumped at every chance instead of right before the spikes. The route starts let go in those modes too, a level without a known length no longer counts as "already at the end", and the route doesn't call empty air (a start position in the open) "off the level". When the route doesn't reach where you are, the Log says so once.
- Autoplay: a respawn no longer reports a dozen deaths (only real deaths count - the start's grace calls the death hook for nothing), and a respawn / start position / teleport moving you starts the route again instead of logging a "prediction bug". The prediction check skips the first ticks after a respawn too, and its Log line says the state it started from (y, GD's y, y speed, on ground, held) - for the one-tick mismatch at start positions.
- Dev tab: "Portals in predictions" (speed / gravity / gamemode / size / mirror portals the predictions went through) and your floor / ceiling in ship / wave (from the portal you came through).
- Tools tab: the two lines under Forget Scan ("Snap To Scan uses it...") make room for the Autoplay button.
- Removed: isModeOrSizePortal (unused), code and all.
- Custom's line under the stages just lists your frames ("(Extreme engine)" is gone).
- Phone text says "the Nova button in the pause menu"; the report, dev info and log file say Nova.
- Off-screen blocks and spikes really counted now: GD switches off objects outside the area it's running (off screen), and the predictions skipped those - so the hidden player fell through floors below / ahead of the screen and the route made random clicks over holes that aren't there (seen at Every End's start). Only objects a trigger turned off are skipped now. Dev tab (Portals in predictions): "Off-screen objects" counts how many were used.
- Updates: on the main menu, once a session, Nova looks up the newest release on its GitHub page. Newer -> the Nova window shows an update box in its own look (dimmed window, a glowing card: what's out and the version you have, Later / Update; then Downloading..., then Restart - or Try Again if it failed; the window comes up for it even if you'd hidden it, and Later hides it again) and an Update tile on the Stage tab (the Quick tiles split in three). Update downloads that release's .geode over this one and asks to restart. Nothing downloads unless you press it. Setting "Check For Updates" (on) turns it off.
- GitHub build: on the main branch it now makes a release named after mod.json's version (e.g. v2.3.0) with alquerez.nova.geode attached and that version's changelog as notes - once per version (bump the version to release again). The package check looks for the alquerez.nova binaries (it still listed the old inputbuffer names).
- Autoplay / level scan clicked as late as possible: before each obstacle they took the LATEST input that lived, so on easy levels every click was at the last moment (barely clearing). Now they look through the whole window of safe inputs (up to 30 ticks before the latest) and use the middle of the ones with the most room from hazards - where a human clicks, and where a small timing error still lives.
- Autoplay route: short clicks. Before, every input it tried was "flip the button and leave it" - in the ship / wave / robot a press stayed held until the next obstacle forced a release, so a spot that needs a quick tap (ship), a short robot jump or a quick wave zig-zag had no single input that lived, and it threw itself at the spike. Now each timing is tried flipped-and-left first, then (nothing safe that way) as a short click / short let-go of every length from 1 tick to ~0.4 s. Of everything that lives it takes the most room from hazards - late when only late lives, the middle of the window when there's room. The click's release counts as an input (a later fix can take it back and try another length).
- Autoplay route: orbs and portals are options too. In cube / ball / UFO / spider / swing the short-click pass now also tries holds of every length, so it can hold into an orb (GD fires an orb you hold into) or jump again right on landing. And when nothing near a death saves it but a portal was taken shortly before (gamemode, gravity, size or speed), it looks for inputs before that portal too - going into a different portal, or into the same one at another height (Dev tab: "looked back past a portal").
- Autoplay route stops giving up (it died at a spot from the level's start, but got past it from a checkpoint right before):
  - The route is planned up to 10 s ahead with the level as it was then - triggers move / show / hide things meanwhile, and far parts were planned from objects GD hadn't switched on yet. Now the next 2 s are checked again every 12 ticks with the level as it is now (each stretch between button changes replayed from its own start); a stretch that now dies or ends somewhere else is cut and planned again from there. Dev tab: "Route check". (A spot that doesn't replay exactly twice in a row turns the check off for that route, so it can't loop.)
  - Take-backs: up to 64 (was 8), counted until the route really gets past the spot (they used to reset on every stretch it lived through).
  - Stuck further ahead: it keeps the route and fights that spot again every 30 ticks (it used to throw the whole route away and start over from you).
  - Orbs: the route remembers the tick each orb is used on, so a stretch replayed or planned again can use its orb, and orbs after a take-back are free again (they stayed "used"). Off-screen orbs can be used too.
- Crash fix (autoplay): the route search could read past the route's end when you got there while it was still searching (access violation in autoStep). It also no longer adds an input that's already behind you.
- Ship / UFO / wave / ball floor and ceiling: GD puts a portal's band floor on the 30px grid (rounded down), not exactly half a band under the portal. Time Machine's ship portal at y 255 -> floor 90 (the mod had 105), so the hidden ship slid along above the floor spikes at the end - they never counted as deaths.
- Orbs follow GD's rules: the y speed is GD's jump speed for the current speed times the orb's factor for the gamemode (pink 0.72, red 1.38, blue = flip + 0.4, green = flip + jump, black = straight down 15, ship / UFO / ball / robot / spider / swing their own), x0.8 mini, x0.7 ball / spider. The learned orb table had wrong entries (yellow orb for a mini cube -11.88, blue orb for a cube "doesn't flip" -7.40...) - that's why Deadlocked's start "died after using an orb" for every input. A learned value is now only used when it agrees with the rules. Dev tab: "Orb rules".
- Debug: a drift is now taken apart - the first route tick where you and the route part, every field of the player that differs there and the tick before (by name), and the button both had (Log: "drift detail").
- The real reason the hidden player fell through floors off screen (every level, not one): GD's own object check skips every object GD has switched off (m_isDisabled), and GD switches off everything outside the area around the camera. So far ahead (where autoplay's route plans) blocks gave no landing and slabs were holes ("you on block 1220, the route in the air"; "none of 1567 inputs saves it, they died on a spike below"). For each hidden-player step, the blocks / spikes / slopes near it now count as switched on, and go back off right after the step. Objects a trigger turned off (groups) stay off. Dev tab: "Off-screen collisions on". (Found in the open reconstruction of GD 2.2081's collisionCheckObjects.) Checked by tests/offscreen_tests.cpp (a stand-in for GD's step on an Every End-like stretch: with the fix the route is tick for tick the one with the whole level on; without it, it goes wrong at 455 of 1600 ticks; every object back to GD's state after every step; a trigger-disabled group stays a hole).
- Wave / ship spam lag: each input could take 6 ms for its first test alone (12 ms worst) - at 240 fps a frame is 4.2 ms, so spamming dropped frames every few inputs (reports: "worst click cost 193% of a frame") and the inputs after a dropped frame landed late. Inputs inside a wave / ship stream now get 1.5 ms (2.5 ms worst), and Show Rays doesn't record their tests. A stream can't carry over a respawn either.
- Robot easter egg: it now falls in from the top of the screen (not just above the window), and when it's done it hops off and falls to the bottom of the screen (it used to jump off the right edge).
- Nova Run (the little level in the sidebar) is hidden for now - that spot gets GUI customization (colours etc.) next. Its code stays (NOVA_RUN_SHOWN).
- GUI colours (in the sidebar, where Nova Run was): two rows of 6 dots - Accent (Violet, Blue, Cyan, Green, Amber, Rose) and Background (Night, Midnight, Ocean, Forest, Ember, Graphite). Click a dot and the window is built again in it (saved). The accent turns the window's glow, buttons, outlines, tabs, the NOVA sign, the galaxy O and the tinted text to that colour; the background turns the dark panels, keeping their brightness. White, grey and status colours (green / yellow) never change, Extreme stays hot pink and Discord stays blurple. Violet + Night is exactly the old look. With Dev mode on (more tabs) the card gets smaller: two rows of dots, no titles (a click says which). Under the mouse a dot glows in its own colour and its row's title shows its name in that colour.
- Cleanup (works the same, less code - about 760 lines gone):
  - Removed: the real-game scan (off since 2.2), moving-hazard tracking (off since 1.26), the click guide (removed in 2.2, its drawing code was still there).
  - Removed: the setting "Old Hidden-Player Step" (the 2.3 step order is the only one now).
  - Removed: the orb press check (it tested 3 ways a press on an orb could play out). Presses on orbs now always use the one it settled on: the orb on the press tick, no flap (0.2 px from the game in your runs).
  - Removed: Snap To Scan (Tools tab). The Assists card has Orb Helper, Show Rays and Show Scan.
- The hidden player's clock: GD moves every player's clock (m_totalTime) on each step outside PlayerObject::update - the prediction never did, so in every prediction time stood still (738 ticks into a route its clock was still where the route began). GD times landings, jump buffering and gamemode / flip grace with that clock. Its stored position (m_position) and, on the ground, the last grounded position now follow it each step too. Found with the drift detail (your state vs the route's, field by field).
- Route / scan states carry the rest of the player's plain physics state (about 50 more fields: jump speed for the speed, the other ground flags, slope / dash / squish state...). A state saved far ahead used to get those from wherever you were when it was replayed - why a spot failed from the level's start but worked from a start position right before it.
- Autoplay: when the route's search finds nothing at a spot but the level scan pressed there, the scan's press is tried from the route's own state and used if it lives (the log said "that press lives - the search missed it"). Dev tab: "from the level scan".
- Theme: the Extreme stage (its button, glow, embers, the header pill) and the Discord tile's glow follow the accent colour now (Discord pulsed blue).
- Autoplay route stays ahead of you: its re-check cut and re-planned a stretch whenever a replay from its saved state ended more than 0.5 px off - and replays are a little off by themselves (sub-pixel to ~3 px), so far ahead the route was cut again and again (Final Destination: "199 stale") and never got ahead; the next jump was planned while you were already at it, and its input kept moving back. Now a stretch is only stale when it dies or ends more than 4 px off (what a changed level does); small misses are logged with every field that differs (Log: "replay check"), to fix next.
- A route uses one step length for all its tests (taken when it starts), and a test from a saved state no longer depends on the orb you're touching right now - the same test always gives the same answer.
- When the level scan's press saves a spot the search missed, the Log says what the search got for that tick and whether the same test gives the same result twice (to find why it missed).
- More autoplay logs: up to 40 drifts, stuck spots and re-checks per session (were 6-12), and the Dev tab keeps the last 30 notes (was 8).
- The hidden player's collision record, the way GD keeps it: GD clears it at the END of each step and keeps the object you stood on (and hit with your head) as "last step's" (m_unk50C / m_unk510) - it uses that to keep you on a floor from one step to the next. The prediction cleared it before each step and never kept last step's ground, so it left edges a tick early ("m_stateOnGround -2/-3" in the replay check) and fell through thin floors it should have landed on (Every End's slabs, "you on block 1220, the route in the air"). Found with the drift detail: your floor's id was in m_unk50C, the route's was -1. Also from it: a stored position GD keeps every tick (m_shipRotation) and its step time (m_unk838).
- Blocks / spikes when GD hands the hidden player nothing (its sections aren't loaded out there): GD's object check doesn't run at all then, so the mod's own nearby blocks now get GD's block collision (landing / sides) and its spikes kill, inside GD's step. Dev tab: "Collision path" (how often GD's check ran, how often it was skipped and the mod did it).
- More debug: every stuck spot logs what's in the level there (each block / spike / slope: id, box, rotation, and whether GD has it switched off / grouped off / hidden / no-touch); a drift where you stand on something the route fell past replays the route's last ticks before it and logs, tick by tick, how many objects GD and the mod gave the hidden player, whether GD's object check ran, whether your floor was among them, and GD's collision result (Log: "landing diag").
- Step audit (Dev tab, three rows): learns from the real game, field by field, what the hidden player gets wrong - while you play, autoplay or not. (1) Between steps: what GD changes on you after a step's last part and before the next (things the hidden player's step never does). (2) One tick from your exact state, the route's way, with your button: how often it comes out exact, and which fields don't. (3) 12 ticks in one run vs 12 one-tick runs from saved states: state a saved state doesn't carry. The last report showed a route state falling through a slab that a replay from 2 ticks earlier landed on - a long run and a restarted one disagree; (3) names what differs.
- Autoplay knows the level moves: GD moves, turns and switches blocks and spikes on / off with triggers, and every prediction saw the level frozen the way it was at that moment - a block sliding into the way later wasn't in the plan, one sliding out of the way still blocked it. That's why Every End died at the same spots every attempt ("route re-checked with the level as it is now: now dies", the route falling past block 1220 you then land on, "none of 1502 inputs saves it" - every input tested against blocks that weren't going to be there). Now every block / spike / slope that leaves its place is tracked: where it is and how it moves right now, plus a timeline of where it was when you were at each x (your x is the level's clock: the triggers go off at an x and you cross at a set speed). Each hidden-player step puts the ones near it where they'll be at that moment - the timeline if it has that x and matched this attempt so far, else its current motion carried on (up to ~1 s) - and back right after. Only their collision position changes; nothing drawn moves. For this session only (nothing saved). Dev tab: "Moving objects".
- Autoplay learning run (Tools: Learning Run, on): autoplay's first run of a level each session plays it once with deaths off, start to end, recording how its blocks and spikes move; then the level restarts and autoplay plays for real with those moves in its plan. Real attempts keep adding to the timeline. No end screen or progress for the learning run. Dev tab: "Learning run".
- Autoplay options in the Tools tab (the Autoplay card, under a smaller Level Scan card - Export / Forget Scan side by side): Learning Run (the first run of a level with deaths off), Noclip (autoplay never dies - watch it play the whole level; its moving-object timeline still records), Retry Deaths and Use Saved Run. The Learning Run setting in the mod's settings is gone (it's this toggle now). Dev tab: "Autoplay options", "Retry Deaths", "Saved run"; the label above you says practice / checkpoints / retry N at x, NOCLIP or the saved run's progress.
- Autoplay Retry Deaths (on): autoplay plays in practice mode and puts its own checkpoints down (removed again, see below) - about every second, where its route is safe a second ahead, on the ground (button up) for cube / ball / spider / robot, and never in the 1.3 s before a spot it died at. A death respawns at the last one and that jump is played again with another input: the input it died with (the last one since the checkpoint - after 3 deaths there, the one before it too) is never used there again, so every retry is a new timing / hold; where its predictions say nothing lives but it died there before, it tries for real the input that got furthest (predictions can be wrong). Six deaths at one spot: that checkpoint is taken back and it goes from the one before. Turning autoplay off leaves practice mode (GD restarts the level).
- Autoplay saves the run that beats the level: its real inputs (back to the checkpoint on every death) go to Nova's save folder, routes/<level>-autoplay.txt, when it reaches the end (not with Noclip / the learning run). Use Saved Run (on): from the same start, autoplay plays those inputs - no planning, no learning run; if the saved run dies it plans again. Forget Scan deletes it too.
- Retry Deaths, fixed: it never put a checkpoint down (it waited for the route to be done searching and not stuck anywhere ahead - 10 s ahead it nearly always is), so every retry started from x 0; now it only needs the route safe a second ahead. And it didn't really try anything new: it picked "the input that got furthest" - which was the press 1 px before the spike every time. Now every input its search tested at a spot it died at goes on that spot's list, nearest miss first (how deep into the spike / block the prediction ended - a near miss is the likeliest to live if the prediction is a little off), and each retry plays the next one on the list for real - earlier, later, press, release, short and long holds - never one that died. One that gets past is kept and used on the next attempts. The Log says which one it's trying ("3 of 412 on the list, predicted 0.8px into it").
- Autoplay pathfinding: an input that gets past a spot and dies later counts now. A try only counted if it lived on with NO other input, so a jump that clears a row of spikes and then needs a second jump for what comes next was thrown away - Every End's 3 spikes at x 3761 (one jump, well before them): every try "died", the search ended with last-moment presses and called it stuck. Now, when nothing lives with one input, the input that gets furthest past the spot is kept and the route plans the next input from there (taken back like any other if that leads nowhere). Dev tab: "Autoplay options" counts them.
- Your Clicks (Tools, Autoplay card, on): autoplay keeps playing the whole time; when you click, your click goes into the game too (held as long as you hold it) and autoplay plans on around it right away. Only your own presses count - GD letting go of the button on a respawn isn't you (that showed "YOU are playing" when you weren't). A click you live a second past is a good one: kept, saved for the level (Nova's save folder, routes/<level>-clicks.txt, next sessions too) and made again at that x on every later attempt; one that dies later is forgotten. Forget Scan deletes them. With Show Rays on, every kept click is a tall bright cyan line where autoplay makes it (taller than the route's own input ticks), so you both see the clicks known to be right. Dev tab: "Your Clicks".
- Wave spam, on time first: in a spam stream every input - press or release - goes in when you made it whenever that's safe, and only takes the stream's shift when on time dies. Every press of a spam came late before (2.2's "balanced" rule kept one shift for the whole stream), and on a fixed tick schedule, which threw away Click Between Frames' between-ticks timing - so the same spam came out different each time at high frame rates.
- Ship taps stay taps: a ship release is held at most a third of how long you held the button (it could be held up to 8 ticks - on a 2-3 frame straight-fly tap that nearly doubled it, and the ship rose more than you tapped for).
- Pick another icon or colours in the garage while the window is up: the easter-egg robot (even mid-jump) and the Modes tab's icons change to them (checked twice a second).
- Learned margin (with Learn From Attempts on): per input type (cube, UFO, swing, robot, ship press / release - not wave), when a click the buffer moved dies anyway within half a second and you made no other input since, the predictions there were a little off for your setup (frame rate, Click Between Frames), so next time it fires 1 tick deeper into the safe window (up to 3). Every moved click that lives eases it back a quarter tick. Saved; the Log says when it changes; Dev tab: "Learned margin".
- Source: the online counter's URL (src/OnlineURL.hpp), the server folder and the .bat helpers stay off GitHub (.gitignore); GitHub's build makes OnlineURL.hpp from the NOVA_ONLINE_URL secret.
- GitHub releases have no notes (just the .geode).
- Raw Wave Spam (Tools > Assists, off): in a wave spam stream (inputs less than ~150 ms apart) every input goes in exactly as you make it - nothing held back, nothing judged (one still held from before the stream goes in first, so the order stays). The first input of a spam is still judged - it isn't a stream yet.
- Hitboxes (Tools > Assists): your outer box (red - spikes, saws, orbs) and inner box (blue - hit a block with it and you die), both players in dual.
- Theme presets (sidebar colour card): "Presets" applies the next whole look (accent + background) - Nova, Royal, Deep Sea, Toxic, Inferno, Sakura, Stealth, Sunset - and "+" saves the current look as one of yours (up to 6, the oldest goes; they're in the cycle). Not shown in the small colour card (Dev tabs on).
- Empty Log says why: Stage is Off (nothing is buffered), or "N clicks so far - all went in as you made them" (the Log only lists clicks Nova moved; Log: More Detail lists all), or no clicks reached Nova on this level (gamemode off in Modes, or another mod takes the input first).
- Tools: the Assists card is taller (5 rows: Orb Helper, Raw Wave Spam, Hitboxes, Show Rays, Show Scan) and Your Stats shorter.
- Autoplay moved to Dev mode: the Tools tab only shows the Autoplay card (and its options) with the Dev tab on (5 clicks on the version); otherwise Level Scan has the whole column again, as before. Turning Dev mode off stops autoplay. The Autoplay card's "no progress saved" note is gone (it showed all the time).
- Remember (Tools, replaces Use Saved Run): autoplay remembers as it plays. Every input it (or you) made that it lived at least a second past, further than ever before, is remembered and saved for the level (routes/<level>-autoplay.txt, loaded when you open the level - the trace says how far it remembers). The next attempts play those same inputs through that stretch with no planning - it used to plan the spot again and get stuck on inputs it had already got past - and plan again only where the memory ends. Practice runs stitch together (back to your checkpoint on a death, then on). A remembered stretch that dies (it didn't play the same) is cut back to 1.5 s before that spot. Beating the level remembers all of it. Forget Scan deletes it. Dev tab: "Remember".
- Crash fix: opening the window outside a level (the Dev tab's Retry Deaths row read the level's checkpoints with no level open) crashed the game at start.
- Your Clicks, only the good ones: a click is kept (and drawn) only if it gets you somewhere new - past the furthest any attempt had got when you made it (or a second past it, if you were already beyond that) - not just alive a second later. A new one replaces kept clicks for the same jump (within ~1.5 blocks). A kept click that dies before getting as far as it did is forgotten after 3 such deaths (it was forgotten on the first). Remove one like a practice checkpoint: Remove Click Key (setting, Backspace) or Undo Click (Tools, next to Autoplay) - the last kept click you passed. The kept clicks are saved per level and loaded when you open it (the Log's trace says how many; Dev tab "Your Clicks" names the file). The cyan lines show with Show Rays on.
- Autoplay FPS: its planning time is per frame now, not per tick. When the frame rate dipped, a frame held several ticks and each got its full planning time - more time per frame, lower frame rate, more ticks per frame. All of a frame's ticks now share 2 ms (5 ms when the route is about to run out). Dev tab: "Autoplay options" counts ticks it skipped planning on.
- Autoplay tries the other way: when no input near a spot gets it past (after a few inputs taken back), it searches every way through from 2.5 s back - then 4.5 s - with A*: at every step both press and don't-press are kept, the high road and the low road, best first, merging states that are the same - instead of changing one input near the death and always picking the same line (down into the pit, straight at the obstacle). A way it finds goes into the route, each step replayed with the route's own tests. Dev tab: "Every-way search".
- Retry Deaths: autoplay no longer puts checkpoints down - you place them (the code is gone). It still switches practice mode on, respawns at your last checkpoint, and retries the jump there with another input.
- Autoplay looks forward too: when no input saves a spot it takes the last input back - and then only searched BEFORE it, so every fix was an earlier and earlier input ("always looking further back"). At Every End's 3 spikes (x 3761) the route's jump off the upper platform at x 3639 landed on the 3rd spike; the fix is that jump a little later (further off the edge = further), which it could never try. Now the whole stretch from the input before it to the death is searched again - earlier and later - without the one taken back (inputs taken back at a spot aren't tried there again).
- Retry Deaths: never goes back a checkpoint any more - it keeps trying new inputs at the spot until one gets past (it used to drop the checkpoint after 6 deaths and start further back). The list is spread out first: the first tries are at least 6 ticks apart per press / release and hold length (early, late, tap, held), then the ones in between - it was stepping 1 tick (1.3 px) at a time. Its try now also gets the rest of the route planned after it (it used to be the last input).
- Route stuck lines say what killed the tries and where ("killed by: spike (3765,525) x500, ...") and how far the furthest one got.
- Moving Objects toggle (Tools, Autoplay card): off = predictions use the moving blocks / spikes where they are now (to test with and without it).
- Death record (Log, every autoplay death): tick, x / y, x speed per tick and y speed, gamemode, gravity, practice, button held / up and the last input (press / release, how many ticks ago, where), the input queue, where the route had you (and how far off you were), what killed you - and what kind of death it was: physics mismatch (the route said you'd live), transition (a portal, orb, speed, gravity or size change in the 0.4 s before), pathfinding (no route through was found, or it hadn't planned that far), release (let go at the wrong moment / held too long) or timing (the right input on the wrong tick). Dev tab: "Death types", "Retry spots".
- The 100 ms prediction check is off while deaths are off (learning run / Noclip): its "you'd die here" couldn't come true, and counted as false deaths.
- Moving objects: their current motion is carried on for at most ~0.5 s now (was ~1 s) - further than that a straight line is a guess.
- Autoplay died somewhere before: a route search there looks three times as far back for the input that saves it (the fix usually comes earlier than the spot).
- Autoplay taps that change nothing are gone: a tap that lives but doesn't change your path in the next ~0.1 s (pressed under a ceiling, where GD doesn't jump) isn't taken - it only stays as a last resort before "stuck". Those made the row of cyan presses on a flat line.
- Windows build fix: a field named `near` clashed with a Windows header macro (`near` / `far`); renamed.
- Autoplay's label above you says what it's doing (learning run %, route N s ahead, searching a way past x, stuck at x - and how many moving objects it tracks) instead of Show Rays' leftover "looking ahead...". With Show Rays on it also marks where it died before (red X, bigger for more deaths) and outlines in orange where moving blocks / spikes will be when you get to them.

## v2.2.0
- New window: the tabs (Log, Stats, Stage, Modes, Tools) are a list in a sidebar on the left, under the title, version and author; the page you're on shows its name at the top. Dark glass look with a purple hue: near-black panels with soft violet edges, outlined cards, one violet accent.
- Switches instead of checkboxes: a pill that turns violet with a white knob that slides across (Stage, Modes and Tools).
- Animations: the window grows in with a small bounce when it opens and shrinks away when it closes, and each page slides in when you switch tabs.
- Console log (Windows): the "console" button on the Log tab opens the Log in its own command-prompt window instead of the Log tab (and the in-game pill). Colours by type, and with "Log: more detail" on it also shows every click's decision. Its close button is removed on purpose - closing a console window would close the game - so turn it off with the same button. It stays on next time until you turn it off.
- Stages 3 and 4 are gentler: 3 frames and 5 frames (were 4 and 8). The jump from Stage 2 was too big and clicks were held too long ("too harsh"); now it's an even climb, 1 / 2 / 3 / 5 frames, then Extreme. Wave: 3 and 4 frames; ship: 2.
- Ship, light touch: ship clicks are only ever held up to 2 frames (~33 ms), on every stage, and only for a crash in the next 100 ms; anything later counts as your next input's job. (A Custom ship value above 2 frames is held to 2 too.) Ship inputs used to be held much longer for crashes far ahead, which pulled you down off a straight fly when you were a little off the predicted path.
- The badge says V2.2. The system name ("Windows 10" etc.) is at the bottom of the sidebar.
- Cleanup: the switches' round ends drew a little spike on the right (GD's shape fill doesn't like two points in the same spot) - they're clean pills now, slightly wider, with a soft shadow under the knob. Labels, buttons, tab names and the footer use GD's clean font; GD's bold font is only for headings (title, page name, card titles). The system name is centred at the bottom of the sidebar under a thin line.
- One smooth bold font for the whole window: Poppins Bold, bundled with the mod (Open Font License, in resources/fonts). Text is bigger than GD-font sizes would make it. Titles (card titles, Stats section titles, the column heads on Modes, the footer) are bold UPPERCASE; the Stats section titles are lavender like the card titles, and the rows under them are white. Buttons and switch labels are in Title Case. If the font can't load, the window falls back to GD's fonts.
- Shooting stars: thin streaks drift down-left across the page behind the cards while the window is open (not in the small in-game pill).
- Buttons: text a bit bigger and centred in the box (this font sits higher than GD's), Forget Level / All Settings / Export Report are sized to their text, with bigger text; Forget Level and All Settings sit side by side at the right of the OPTIONS card.
- Tools: descriptions start with a capital; the scan hint and the scan status are in capitals. Modes: gamemode names and the NORMAL / MINI heads are bigger.
- Sidebar: a bit wider, with a bigger "Input Buffer" title, a bigger round V2.2 badge with its text centred, bigger "by AlQuerez23", the tab dots lined up with the names, and the system with its version at the bottom ("Windows 10 (22H2)").
- The stage pill at the top right has its text centred. Bigger: NORMAL / MINI on Modes, Cube / Ship / Wave and their numbers in Custom Frames, Forget Level and All Settings.
- The stage names say the new ship limit ("Stage 4: 5 frames (4 wave, 2 ship)").
- Sidebar sky: a spiral galaxy (glowing core, two arms) up behind the title, and a few faint stars. Your own icons, in your own colours, run across the sidebar like in GD: your cube runs and jumps (longer jumps, a bit faster than the others) (a half turn per jump, landing flat) kicking up little squares, your UFO (a bit bigger, with your cube inside) bobs around the middle with a streak and a puff of squares per flap, and your wave zigzags at 45 degrees with its solid trail - as thick as the arrow's back notch - running into the back of the arrow like in GD; the whole line stays all the way across, and when the wave leaves the side the line wipes away from its start to its end, then the next arrow starts (lined up from the wave sprite itself, so it fits any wave icon). Change your icon or colours in the garage and they change here too. Click one and it dies like in GD - a burst ring, squares flying out in your colours and the death sound - then comes back from the left. The page itself only has the shooting stars (bright, longer, about every quarter second), so the text stays easy to read. The V2.2 badge is bigger, and "by AlQuerez23" is white so it reads over the galaxy.
- The page background has round corners (it was a plain box behind every page).
- Click Guide removed (the level scan still feeds Snap To Scan). Tools: ASSISTS has Orb Helper and Snap To Scan; LEVEL SCAN has more room.
- Dev mode (hidden): click the V2.2 badge 5 times quickly to turn it on / off. It shows the Stats tab (now hidden otherwise, to keep the sidebar short) and the Dev tab: what's happening right now - your player (mode, position, speed, holding), the last input (decision, delay vs window, what the click as made would do, the search), the input queue, your ship / wave rhythm, one-tick prediction accuracy per mode and the scan's internals. "Copy All" copies it plus the newest trace lines to paste to Claude.
- The hints use the keys you set: the footer says your Window Key ("Left Alt to toggle", or e.g. "Ctrl+B to toggle"), and the Stage card says your Stage Cycle Key ("F6 cycles stages"); any key or key combo shows by name.
- New setting "Pause Menu Button" (Geode mod settings, on by default): turn it off to hide the green Input Buffer button in the pause menu. (On phones it is the way to open the window.)
- Fixed the window turning into big coloured blocks after switching between fullscreen and borderless / windowed (or any graphics change that makes GD reload): the window is rebuilt fresh when GD reloads its graphics. On Android it is also rebuilt when the game comes back from the background.
- The pill at the top right shows your stage ("STAGE 2", "EXTREME", "CUSTOM", "OFF") instead of just "ON".
- The page only slides in when you switch tabs - picking a stage, +/- or Apply no longer makes it jump.
- Custom frames are saved and used the moment you press +/- (the Apply button is gone). Your numbers only counted after Apply before: without it the old 6 / 4 / 4 frames (24 / 16 / 16 ticks) stayed on, which is where the 6t / 4t clicks came from.
- New Custom Min / Custom Max on the Stage tab (OPTIONS card), for the Custom stage only: Max is a hard limit - no click goes in later than it (held clicks, Orb Helper and Snap To Scan included); "Off" = no limit. Min is the smallest shift a click gets when it has to move. Ticks: 240 a second, 4 = 1 frame (the Log's "+6t"). The other stages are untouched.
- Show Paths and Small While Playing are removed, code and all. No more in-game pill: the window stays as it is while you play (the Window Key shows / hides it).
- New Show Rays (Tools, off by default): what the buffer sees and thinks, drawn in the level as lines while you play. A white outline is your hitbox. The cyan line is where you go if you press now, the green one if you let go / don't press, with a red X where one dies. The yellow line is a live pathfinder - a small search ~1 second ahead (up to 12 versions, a press / release choice every few ticks, like the level scan) for inputs that get through, with cyan / pink ticks where to press / let go. After each click: the click as made (red if it dies), the delays the buffer tested and rejected (faint red), the one it picked (white), and a line of text saying why ("PRESS held +4t: on time dies in 9t (hits spike) - fires on the first safe tick").
- New Export Scan button (Tools, LEVEL SCAN): saves this level's scan to a text file (and copies it) - every press / release with its % and position and gamemode, which spots it couldn't solve, and what killed every path there.
- Online users: the top of the window shows how many people are online (green dot) and offline (grey dot). Each game sends the Input Buffer server an anonymous random ID every 2 minutes, nothing else; the "Show Online Users" setting turns it off. Needs the server set up once (server/README.md) - until then it stays hidden.
- Releases work like presses. An early release now waits for its moment the same way an early click does: it gets the same window as a press (on Extreme wave / ship releases were capped at 3 frames against 12 for presses), and a release made while your press is still being held is checked too - it used to fire on schedule unchecked, so a slightly early release just died.
- Level scan: it stops at the end of the level (it used to "go through" spot after spot past the end - one scan logged 39 000 of them and never finished). The floor / ceiling of a gamemode the level starts in (no portal yet) sits on the ground, like GD (Denouement's mini wave: 90 .. 390). "Ground check" / "band check" lines have their own list now, so the scan's own lines can't push them out before an export.
- Nova: the window is called Nova now. The sidebar has the logo, NOVA in big letters (each letter glows violet and lifts when the mouse is on it), "Input Buffer" under it, then the version badge and "by AlQuerez23". A settings gear sits top left of every page (opens the mod settings).
- New layout like the reference: Stage - the stage on top, Options rows and Quick tiles (Forget Level, All Settings, Discord) on the left, Custom (frames, Custom Min / Max) on the right. Tools - Assists rows (Orb Helper, Snap To Scan, Show Rays, Show Scan) and Your Stats on the left, Level Scan on the right. Every setting is a rounded row with its name, a short grey description and the switch: click anywhere on the row to switch it; it glows under the mouse, and an "on" row is tinted violet. Sidebar tabs glow under the mouse too.
- Scan / A*: cubes can hold now. The scan only ever tapped in cube; holding is how a lot of the game is played - you re-jump the moment you land, and a held press carries into an orb. A cube version now tries keep / switch the button / a tap.
- Smooth window: GD draws shapes without anti-aliasing (jagged circles and corners), so buttons, switches (pill and knob), cards, the sidebar highlight and the online pill / dots are now drawn from small smooth textures the mod makes itself. Buttons have a gentle shade with a light top edge.
- Hover works: buttons glow violet (fading in / out) under the mouse - the old check never found the buttons.
- Scan / A* / pathfinder only accept real ways through: a version with no block, spike or slope of the level within 10 blocks counts as dead ("left the level's path"). A level's path always runs along its obstacles - walking along the ground under the level or flying off it isn't a set of inputs that gets you to the end, but it was what the scan found (Shardscapes: 1 input for the whole level). The portal floor / ceiling now also works where the level starts in that gamemode (no portal yet: GD's own portal y).
- Export Scan lists what you stood on while playing ("ground check": the block, or GD's ground / a portal floor, and whether the mod's list has it) and your real height range per gamemode part ("band check") - to find what the hidden player still misses.
- Window overhaul, first pass (like the reference): flat charcoal panels with a purple tint and one muted violet accent, near-white card titles, and settings rows with the name on the left, a short grey description under it and the switch on the right, with a thin line between rows (Stage options, Tools).
- Scan / A* / pathfinder: the hidden player now has the floor and ceiling GD puts at a ship / UFO / wave / swing / ball / spider portal (GD's own heights: 300, ball 240, spider 270, centred on the portal you came through, never below the ground). Without it, versions fell through that invisible floor to the ground and walked under the whole level (Shardscapes: y 99 from 2% to the end with 3 inputs), or bounced along the ground (Denouement after 20%), or flew out of the top. They slide along it now, like you do. The Log trace has a "band check" line per gamemode part (how far you really went vs. the band used) so the band can be tuned from a report.
- Show Rays: the pathfinder pauses while one of your inputs is waiting to go in.
- Window: a soft violet light runs around the window's edge; the online / offline pill is at the bottom right; the purples are calmer (selected buttons, titles, hover).
- Scan / pathfinder fix: versions could fly out of the level. The hidden player isn't held inside the floor / ceiling GD puts at a ship / wave / UFO portal, so a version could climb far above everything (one died at y = 45 000 in Denouement, 60 000 in Amethyst) and "survive" to the end with no inputs - scans that said "done" with 10 inputs for a whole level, or 80 spots it "couldn't solve". A version that leaves the level's height range (every object in it, plus 5 blocks) now counts as dead. Old scans made that way are wrong: Forget Scan, then scan again.
- Export Scan also lists the scan's path every ~1% (where it really went) and the level's height range.
- A* pathfinding: the live pathfinder (Show Rays) and the level scan's hard spots use an A* search now. A state is the hidden player after some ticks; from each one it tries keeping the button as it is or switching (a tap in cube-type modes), with real game physics - every tick in wave (so releases land on the exact tick), every 2 ticks in ship, 4 elsewhere. It always carries on from the most promising state (fewest ticks + inputs, away from spikes, closest to the goal), never revisits a state it has seen, and backs up to the next best the moment a line dies - instead of keeping a fixed set of versions. The scan runs it first wherever every path dies (up to 0.4 s per spot, from a few blocks back); the scan message says how many spots A* solved. The pathfinder's line turns orange when no way through was found (it shows how far it got).
- The online counter's address is in its own file now (src/OnlineURL.hpp), so a new main.cpp never wipes it.
- Predictions see invisible / hidden blocks: GD only gives a player the objects of the level sections it has loaded for collisions, and the hidden player that runs every prediction (and the scan and pathfinder) was missing some - it fell straight through invisible floors you were standing on, so whole paths were wrong. Every solid block, spike and slope right around it now also comes from the mod's own list of the level, once per tick (never twice). Stats shows how many it had to add.
- Snap To Scan is checked by the prediction now. It trusted the scan blindly: a click on a scanned spot went in raw even when it would die, and an early one was held until you reached the scanned x - up to your whole window, +32t in mini wave - wherever your height had drifted by then. Now an early click is only held if the prediction puts you on the scanned point (x and height) on that tick and pressing there survives; everything else is decided normally. Releases no longer snap (they keep your spacing).
- The Log says what a held click was waiting for: "reached the scanned input" / "touched the orb" - both used to say "spot that worked before", the learned-spot text.
- Orb Helper never takes over a good click: a press that survives as made goes in as made (except a cube / ball / spider press in the air, which does nothing until an orb anyway). On by default, it was holding normal jumps near orbs for the orb.
- Changing Custom Min / Max switches the stage to Custom.
- Online / offline: round dots with a soft glow on a small dark pill.
- Buttons light up purple when the mouse is over them (PC / Mac).
- Show Rays: the pathfinder's yellow route is only drawn ahead of you.
- Spam no longer shoots you up (wave and ship): a delayed release made that hold longer, and the next press then went in on time ("on time first"), so the extra hold was never paid back - every time, you went up a little. Now a stream's shift only ends on the same kind of input that started it, so your holds and gaps add up to what you made. Ship spam gets the same steady-shift handling as wave. A follow-up input (your release while the press is held) keeps your spacing first and only goes on time when keeping it dies.
- Orb Helper is on by default and now works on dash, spider, teleport and custom orbs too: the prediction can't play those (it stops right before one), so an early click on them went through raw and missed. If doing nothing gets you to the orb alive, the click waits and goes in the tick you touch it.
- Scan Level solves more: a spot where every path dies gets up to 3 tries, each backing up further (4 / 8 / 12 blocks) with more versions (256 / 512 / 1024) and finer heights, before it goes through the spot unsolved. (It tried once.)
- Fixed the game crashing during Scan Level on big levels (crash in GD's collision code, PlayerObject::collidedWithObject): where every path died, the scan carried on from one of your runs saved in an earlier session. Saved to disk, a run loses what it was touching (level objects only exist while the level is open) but still thinks it's on that ground / slope, and GD crashed using the missing object. Runs from earlier sessions aren't used any more - only runs from this session, which are complete. (The crash test that switched off the hidden player's collisions is undone - with it off the buffer couldn't see any obstacles.)
- New Forget Scan button (Tools, LEVEL SCAN): deletes this level's scanned route, its guide and your saved runs.
- Scan view: red dots only show around where the scan is working now (they piled up all over the level), and a death to a moving hazard puts its dot in the right place (it reused the last death's spot).
- Real Game (Practice) is switched off and hidden in Tools. It ran the whole level while paused and backed up with practice respawns, one input choice every 2 ticks - too fragile to trust (crashes, routes that didn't hold up). The code is kept for a proper rebuild.
- Wave rays: a wave only ever flies in two straight lines, so the buffer now casts both - the way a press sends you and the way a release does - against the level's hitboxes, like a wave bot's view, and lets them pick the delay to try. One real prediction confirms it (plus up to 3 to find the earliest that holds) instead of the full search's dozen-plus per deadly click, so spam stays under the CPU limit. If the prediction disagrees, the normal search runs as before. It only moves your own input inside your window; it never makes inputs. Stats shows how often the rays' pick held up.

## v2.1.0
- Fixed the buffer only working well after scanning the level (mini cube especially). Mini cube is back to how it predicted before: the extra player state predictions started copying in this version (jump / slope / boost values and what you're touching) is gone from normal predictions again. Only the level scan uses it.
- Click guide dots are drawn as filled circles the same way the window draws its panels.
- The badge next to the title now says V2.1.
- "by AlQuerez" and the system name at the bottom are now white and bold.
- Name and Discord updated: the title says "by AlQuerez23" and the Stage tab says "Discord: alquerez23".
- The bottom-left of the window now says how to show / hide it, like "Left Alt to toggle" (whatever key you set), in white bold, instead of "INPUT BUFFER  EXTREME". On phones it points to the Buffer button in the pause menu.
- Discord is now a purple button under the Stage tab cards (white, bold). Click it to copy alquerez23. The old "Left Alt: show / hide this window" line there is gone (the bottom of the window already says it).
- White text: "F6 cycles stages", "frames @60fps, 0.5 steps", the Modes tab hint, and the grey rows in Stats.
- "forget level" is purple like the V2.1 badge.
- The pause-menu button is now a green circle like GD's own pause buttons, using GD's own green circle base (same rings, outline and shading as the gear) with the gold arrow, target and timeline icon on top, and it's the same size as the buttons next to it. It's on every platform: Windows, Mac, iOS and Android.
- If the button image is missing from a build, the pause menu falls back to the old "Buffer" text button, so the window can always be opened. build.bat now refreshes the build setup every time, so new images get picked up.
- Phones: the window is 1.5x bigger on iOS and Android (Window Size still scales it on top).
- Phones: hints say to use the pause-menu button instead of a key.
- Fixed a crash on iOS and Apple Silicon Macs when touching an orb. The mod hooked a tiny orb function that's too small to hook on those devices, which broke the function right next to it. That hook is gone (what it did is already covered by the mod's other orb checks).
- New purple logo.
- Wave and ship, input checking: when you let go while a press is still being held (or the other way round), the mod used to move your second input by the same delay to keep your spacing. A +18t mini-wave press moved your release 18t too, and that's what killed you. Now it tests both: your second input on time vs. keeping the spacing, and uses on time when that's safe (less lag), otherwise whichever survives.
- Wave and ship, less harsh: an input is never held longer than about 3/4 of your own usual hold (for presses) or gap (for releases). Ship releases on Extreme are capped at 5 frames like wave releases.
- Fixed a false "one-tick check: prediction differs" right after respawning (most visible with a start position): a check from the end of the last attempt was compared with the new spawn.
- Fixed "the physics hook isn't running" showing up when nothing was wrong. It came from clicking while dead or respawning; now it only shows if the game keeps drawing frames without any physics steps while you're alive.
- The "Input Buffer - Stage ..." banner only shows when you press F6, not when you pick a stage in the window.
- Show paths: the hitboxes at both ends of the path are circles now.
- The Log no longer shows OK (safe click) and QUEUED lines. "Log: show safe clicks" is now called "Log: more detail".
- New Tools tab:
  - Orb helper (toggle): a click made a little early for an orb waits and goes in the tick you touch the orb (up to 5 frames early). Only if not pressing until then is safe. Meant for orb double-clicks and UFO / swing orbs.
  - Level scan (beta): pause at the start of the level (or a checkpoint) and press "scan level". The mod plays the level ahead on its hidden player and finds a set of inputs that gets through. It runs while you stay paused and saves the result for the level. A scan always starts from where you paused, so if it stops somewhere, pause past that point and scan again - the new part is added to what's saved. It can't run the level's triggers, so parts with moving objects may come out wrong, and it stops at dual / mirror / teleport portals for now (scan again after the portal).
  - Scan fix: it got stuck right away in tight parts (wave / ship / UFO), because it wanted every input to survive on its own for a while - there the next input is always needed soon. It now takes the input that gets furthest - even by a single tick - and lets the next one carry on. The scan also starts from your real player now (exactly what the normal predictions use). When it does get stuck, the message says the gamemode, how soon it would die and what kills it, how many inputs it tried and how far the best one got.
  - Scan, rebuilt: it follows up to 64 different versions of the run at the same time. Every 2 ticks (every tick in wave) each version tries both "keep going" and "switch" (press / let go); versions that crash are dropped, and the survivors are kept spread over the whole height range. The version that gets furthest with the fewest inputs, staying away from spikes, becomes the route.
  - Why it got stuck ("every path dies there"): it used to keep the versions with the fewest inputs, so they all ended up as near-copies of "don't press" a few px apart, flew into the same wall together, and switching at the last moment couldn't save any of them. Now the versions stay spread out, and wave versions can switch every tick (was every 2).
  - Click guide routes are cleaner: no extra inputs, and the route keeps a margin from spikes instead of turning right at their tips.
  - The scan no longer stops at triggers ("speed portal/trigger ... ahead"): it can't run triggers anyway, and speed portals are always applied. A version that runs into something it can't see past is dropped; the scan only stops there if no version gets around it.
  - The scan uses your own runs where it can't simulate the level: while you play, the mod saves your real player's state every block (only from parts you got at least 3 blocks past). When every version of the scan dies, or it reaches something it can't run (a trigger, a moving part), it carries on from your own run just past that spot instead of stopping. Right after a gamemode portal it also switches over to your real state in the new gamemode if you have one there (GD does more on a real portal entry than the scan's hidden player can copy - in Amethyst's UFO every version died right after the portal). So: play a level once as far as you can, then scan, and the scan reaches at least as far as you got. These states are kept until you leave the level.
  - When the scan stops, the message says what killed every version and where it is in the level.
  - The scan never stops before the end of the level now. When every version dies at a spot, it:
    1. backs up about 4 blocks and tries harder there (4x the versions, a switch every tick, finer heights),
    2. carries on from your own run just past the spot, if you've played past it,
    3. with "Real game (practice)" on and practice mode, tries the spot with the REAL level (see below),
    4. and as a last resort goes through the spot (deaths ignored for one block) and carries on - that spot gets no dots, everything after it does.
    The message at the end says how often it needed each one.
  - Portals in the scan now do what GD does first on a real portal: the player's own "switched to gamemode" step (speed / velocity changes on entry), then the switch. That was missing, and it's the likely reason every version died right after Amethyst's UFO portal.
  - Your run's states are saved now (per level), so the scan can use runs from earlier sessions too. Only plain values are saved; a GD update starts a fresh file.
  - Show scan (Tools, on by default): while the scan runs you can see what it's doing in the level behind the pause menu - the versions it's following (yellow lines), where they die (red dots), and spots it had to go through without a solution (orange). It stays up until your next attempt.
  - Real game (practice) (Tools, off by default, experimental): in practice mode, where the hidden player can't get through, the scan plays the real level from where you paused - triggers, moving parts and portals all run for real. It follows the route found so far, tries inputs every 2 ticks past it, and backs up to its own checkpoints when it dies, until it's 2 blocks past the spot. Then the level goes back to exactly where you paused (a practice respawn) and the normal scan carries on from the real state. While it runs your clicks, deaths and the level end are held off, nothing counts as progress, and the attempt counter goes up with each of its respawns. It's new and couldn't be tested on a real level yet - if anything looks wrong, turn it off and send a report.
  - The scan only runs when you press "scan level" (no automatic scans when you pause).
  - Export report now lists the scanned route (every scanned press / release with its spot and gamemode) and where gravity flips in the scan, so a wrong guide can be checked against your real clicks.
  - The pop-up when a scan ends is short now ("Level scan: 34% done"); the full message is on the Tools tab.
  - Scan goes through gamemode portals now (experimental): the hidden player switches to ship / ball / UFO / wave / robot / spider / swing / cube with its own switches, nothing in the level is touched. It still stops at dual, mirror and teleport portals.
  - Every version starts from your real player with its saved movement on top (copying the player into a spare hidden one lost something - in a mini wave the copy died on its first tick).
  - The scan copies what your player is standing on / touching (ground, slope, walls) too.
  - If every version dies at one spot, the message says what kills them there.
  - Scan inputs per gamemode: cube, ball, spider, UFO and swing get single clicks (press, let go a tick later) - one dot per click. Only ship, wave and robot use press + release (there it matters how long you hold).
  - Click guide (toggle): round dots where the scan's clicks go (cyan). In ship, wave and robot also where you let go (pink), joined to the press by a white line. No text.
  - The white line follows the path the scan took between the press and the release, so a robot jump draws its curve instead of a straight line.
  - Fixed the scan running from the wrong place on start-position levels (like Shardscapes StartPos): pausing before the attempt had started scanned from the level's normal spawn on the floor, before the start position moved you, so it scanned a path you never take (stuck at 90%, and the guide dots were off screen at the bottom). Scanning now waits until the attempt has started.
  - If your run is nowhere near the scanned path (10+ blocks away for about 1.5 seconds), that part of the scan is dropped, dots and all, so a scan saved from the wrong place clears itself. Pause there and press scan level to redo it.
  - The normal buffer never needs a scan: with no scan (or Snap to scan off) every click is predicted as usual.
  - Snap to scan: releases snap too. A release after a press that snapped to a cyan dot now waits for its own pink dot; before, it kept the press's delay (or went on time), so presses lined up with the guide and releases didn't.
  - Snap to scan (toggle, off by default): when your click matches a scanned input (same gamemode, same height on the path), the mod uses the scan instead of predicting: a little early (within your stage's window), it waits for the scanned spot. Less work at click time, and the input already knows where it goes.
  - Your stats: attempts, deaths, best %, completions and clicks buffered, for this level and all levels, saved between sessions.
  - Export report: saves the Log, Stats, settings, system info and a trace of every click to a file, copies it, and opens the folder (PC / Mac). Send that file instead of screenshots.
- Wave, lighter: each wave prediction now only looks as far ahead as matters - until your next input at your own rhythm plus a short grace (where you go after that is your next input's job, the same rule as before). It used to look 3-4x further every time, which was most of the work and the cause of frame drops while spamming. Same decisions, roughly half the work or less per test.
- Wave, held releases: a release that's being held now follows its plan like presses do, instead of running a full prediction every tick while it waits. Less work while you spam, and it fires on the planned tick.
- Wave releases on Extreme: a release is now held at most 5 frames instead of 12, so it can't come out way late or look ignored. And a release that's safe up to an orb or portal (where the prediction stops) now goes straight through instead of being held until the window ran out.
- New mod description: how the mod works, the stages, and a version table with the platforms each version works on.
- New system line: the bottom of the window shows what the game is running on: Windows 10 / 11, Wine / Proton (Linux, Steam Deck), macOS with Apple Silicon / Intel / Rosetta, iOS / iPadOS, or Android 32 / 64-bit.
- Stats has a new "System" section: the full OS version / build, the device (chip or phone model), and the Geometry Dash, Geode and Input Buffer versions. Handy when someone reports a bug.

## v2.0.0
- Input Buffer V2: everything since v1.17 in one release - exact predictions (one-tick check 100%), learned orb speeds, size portals predicted, held clicks that follow their plan, much lighter per frame, the new purple window with the in-game pill, the new Log and Stats, Android, iOS and macOS support. Details per step below.
- Build fixes for iOS: the keyboard hook (macOS only) is no longer compiled on phones, and the GitHub build works around a missing include in Geode's current iOS bindings.

## v1.26.2
- Fixed the "random orb": a circle could show up next to an orb. It was the orb effect being drawn by the mod's hidden prediction player. Predictions no longer trigger it, and the jump itself comes from the learned orb speeds as before.
- Android support: the mod is marked for Android, and there's a new "Buffer" button in the pause menu that shows / hides the window. That's the way to open it on a phone, since there's no keyboard. Mouse-wheel scrolling is PC-only; on Android you scroll the Log and Stats by dragging.
- A GitHub Actions build (.github/workflows/multi-platform.yml) builds Windows and Android together into one .geode.

## v1.26.1
- Held clicks follow their plan: when you click, the mod predicts your path once, and while the click is held it just checks you're still on that path, with no new prediction every tick. It fires on the same tick as before. If something unexpected moves you off the path, it goes back to checking every tick. Much less CPU while a click is held. (Mini cube keeps its full per-tick checks.)
- "Small while playing" (Stage tab, on by default): while a level is running you get a small pill with the stage and the latest Log line. The full window comes back when you pause or go to the menus.
- New Log look: time, a coloured tag (BUFFER, FIRED, DEATH, RAW, QUEUED, OK, NOTE) and a short description.
- Log lines are only built when they'll be shown.
- The window pops in when it opens, the tab highlight slides between tabs, and the window reopens on the last tab you used.
- New Window Opacity setting (in All settings) for the window's background. Text stays solid.
- "forget level" and "all settings" moved next to the OPTIONS title.
- A "V2" badge next to the title.

## v1.26.0
- Less work every frame, for less input lag:
  - Turned off moving-object tracking. It recorded every nearby spike and orb 240 times a second and never actually predicted anything.
  - The one-tick check and accuracy tracking (diagnostics) only run with "Log: show safe clicks" on.
  - The window only redraws text that changed, instead of rebuilding everything 4 times a second while you play.
- Cleaner log: the small "live: said no ..." detail after a fired click only shows with "Log: show safe clicks" on.

## v1.25.9
- Removed everything that held or moved your clicks for orbs: orb aim, the early-click orb snap, and aiming through portals. Also removed the gamemode-portal hold. All of these delayed clicks and made the game feel off. Orbs are still predicted correctly; nothing holds a click for one anymore.
- Wave: an input in a burst of spam goes in on time whenever that's safe. Before, one delayed input kept the same delay on every input after it until you paused, which felt like input lag.
- Learn from attempts is fully mini cube only: spots that older versions saved for UFO and other modes are deleted when a level loads.
- Stats: the first section is titled with the level's name, and every section title is bold and white. The Windows section shows what clicks really get. Extreme is 20 frames (12 for ship / wave); Stats was wrongly showing the base 8f and 5f, but Extreme itself was working.
- Scrolling with the mouse wheel over the window now scrolls only the window, not the level list behind it.

## v1.25.8
- Buttons and boxes are actually rounded in the game now. They're drawn as rounded shapes instead of stretched textures, which came out square on small buttons.
- "EXTREME" in the top-right, the stage name and the close X are white. The X is now a box like the other buttons.
- Stats cleaned up: short sections (This level, Prediction, Orbs, Your rhythm, Windows, Performance) with the label on the left and the number lined up on the right. The debugging numbers are under DETAILS, which only shows with "Log: show safe clicks" on.

## v1.25.7
- New colors: the window fades from purple at the top into midnight blue at the bottom, with a violet-to-pink line under the title, violet highlights for the selected tab and stage, and lavender section titles.
- The title is white instead of yellow.
- Every tab and button is now a rounded box, and the whole box is clickable. Before, tabs only reacted when you clicked the word itself. All buttons share this one style.

## v1.25.6
- New window look: the tabs are one even bar, the Stage tab is split into three panels (Stage, Custom frames, Options), the Modes tab has a panel per column, and Log / Stats have a real scrollbar. "clear" moved to the bottom of the window, and an empty Log explains what will show up there.
- "by AlQuerez" next to the title, and "Discord: AlQuerez#3900" plus your window key (Left Alt by default) on the Stage tab.
- Removed the Changes tab. This changelog is still kept up to date.
- Removed the "Early UFO clicks go to the next orb" toggle. That behavior is now always on.
- Shorter orb aim line in the Log: "PRESS aimed at the pink orb: +6t (good on +5..+7t)".

## v1.25.5
- Orb aim reworked after going through it properly:
  - It tests the whole time you overlap the orb, not just its first 10 ticks. At normal speed you're inside an orb for about 40-50 ticks, and the tick that clears the spikes is usually late in that. Your on-time clicks kept landing on the orb's last usable tick, so early clicks were only ever tested on ticks that hit the spikes.
  - In a chain of orbs, a tick counts as good if it gets you to the next orb with a few ticks to spare, because that orb is your next click's job. Before, the right tick still looked deadly, so nothing got aimed.
  - It only aims at a tick that actually gets you through. Before, it could aim at the "least bad" tick and override a better plan.
  - It fires in the middle of the longest run of good ticks, so being one tick off still works.
- The tick picking is unit tested: it finds a 1-tick window anywhere in a 50-tick orb, including at the orb's very edge. It's capped at 2.5ms of CPU per click.
- With "Log: show safe clicks" on, the orb aim line shows how many ticks were tested and what each run of ticks did.

## v1.25.4
- Orb aim uses much less CPU. In UFO it was running on every click and dropped the frame rate (124fps in the last log).
- "PRESS too late for the orb" now only shows when nothing later would keep you alive either.

## v1.25.3
- New toggle on the Stage tab: "Early UFO clicks go to the next orb" (on by default). A UFO or swing click made well before an orb now gets buffered onto that orb, like any other buffered click, as long as you'd reach the orb without pressing, the orb is within your window, and using it keeps you alive. Before, only a click that would kill you right away got aimed, so an early click far from the orb just flapped.
- If you need a flap to reach the orb, the click stays a flap. Turn the toggle off if it ever moves a flap you meant onto an orb.

## v1.25.2
- Cleaner log. The orb check and orb jump lines only show up when the orb prediction is off by more than 2px. "REL raw (no effect here)" and "orb aim: no orb ahead" are gone. Orb aim tests are grouped, e.g. "+0 orb, dies 11t | +1..+10 flap, dies 7..1t".
- A click on an orb's last usable tick that still kills you used to say "PRESS ok (safe 11t)". It now says "PRESS too late for the green orb: using it now dies in 11t, later is a flap - click a bit earlier".

## v1.25.1
- Size portals no longer stop the prediction. In Amethyst's UFO part the orbs sit right next to mini and normal size portals, so every orb click there went in raw ("size portal (mini) 6px ahead"), and none of the orb fixes ever ran. The prediction now switches your size when it passes a size portal. It does this on its own hidden player only and never touches the real portal, which is what broke portals back in v1.20.0.
- An orb that hasn't been learned at a given size or gravity yet uses the same orb's learned jump from the other size or gravity.
- Stats shows how many size portals predictions have gone through.

## v1.25.0
- Found the orb bug that's been there since v1.23.0: only the first prediction of each click could use an orb. When a prediction touched an orb, the game marked it as already used and the mod never cleared that, so every prediction after it (the search for the right tick, orb aim, the live re-checks) was told the orb was gone. A click on the orb worked, because that's the first test, but an early click never found the orb tick and said "no safe moment found" or "too late".
- Predictions now use any orb you haven't really used this attempt, no matter what the game's flags say, and orbs are always put back exactly as they were.
- With "Log: show safe clicks" on, orb aim lists what each tick it tested did, e.g. "+3:orb dies 14t  +4:orb ok".

## v1.24.9
- Orb aim kept saying "no orb ahead" even with your press on the orb. The game marks an orb as activated as soon as you touch it, not when you use it, so the mod skipped the orb you were in. The mod now keeps its own list of the orbs you've really used this attempt.

## v1.24.8
- Orb aim never ran ("held for an orb: 0"). It needs to know when you'd reach the orb if you don't press, but the game only reports touching an orb while the button is held. Now it uses the hitboxes for that; the game still decides which press ticks actually use the orb.
- A press held through a size or gamemode portal now gets aimed at the orb after the portal, as soon as the mod can see past the portal. Before, it fired at the portal hold's limit straight into the spikes.
- With "Log: show safe clicks" on, the Log says why a click wasn't aimed (no orb ahead, or no press tick uses it).

## v1.24.7
- Early UFO / swing clicks for an orb finally get aimed: the mod tests every tick you'd be overlapping the orb and fires your click on the one whose orb jump keeps you alive longest. Before, the normal search could never pick an orb: it wanted safe ticks on both sides of its pick and skipped ticks far from the click, and a frame-perfect orb is only 1-2 ticks wide. The v1.24.4 hold ran out of CPU time every click, so it never triggered.
- Log: "PRESS aimed at the pink orb: +Nt (you overlap it on +A..+Bt)", then "PRESS fired +Nt (on the orb)".
- The orb press prediction follows GD's own order by default (flap step, then the orb). The old orb check results are reset, since they were made while the prediction's orb did nothing.

## v1.24.6
- Found why the first orb never buffered: the prediction's orb did nothing. Pink and green orbs both came out as a normal UFO flap (y-speed 6.87), while the game gave 4.46 (pink) and -10.62 with a gravity flip (green). So every "after using an orb" prediction was wrong.
- Orbs are now learned from the game: every orb you really use records the speed it gives and whether it flips gravity (per orb type, gamemode, size and gravity), and predictions use exactly that. It's saved, so each orb type only needs to be hit once. You'll see "learned: pink orb (ufo) gives y-speed ..." in the Log and the full list in Stats.
- Removed the y-speed correction from v1.24.5 (it was learned from the broken orb).

## v1.24.5
- Orb jumps are measured against the game: after a UFO orb click that went in on time, the Log shows "orb jump [pink orb]: game used it on tick +N -> y-speed A | predicted tick +M -> y-speed B". If the tick matches but the speed doesn't, the prediction learns a correction for that orb type and size and uses it from then on.
- The prediction uses orbs exactly the way GD calls them (same settings as the game's own call).

## v1.24.4
- Early UFO / swing click for an orb: if pressing now would kill you and an unused orb is coming (you reach it without pressing, inside your window, before anything kills you), the click is held and fired on the tick you're touching that orb, exactly like a perfect click. It no longer depends on predicting the orb jump, which was 6-18px off and made the first orb say "no fix". The log shows "PRESS held for the pink orb", then "PRESS fired +Nt (on the orb)".
- Stats > ONE-TICK CHECK shows how many early UFO clicks were held for an orb and fired on it.

## v1.24.3
- UFO / swing orb presses: the prediction now tries three ways GD might handle a press on an orb (orb first with no flap, flap then orb, both together). Every time you click a UFO orb and it goes in on time, all three are compared with where you really end up 10 ticks later, and the closest one is used from then on. It's saved between sessions. You'll see "orb check" lines in the Log, and the result under Stats > ONE-TICK CHECK.
- A press only uses an orb you're really overlapping that hasn't been used yet.
- Death lines say what you hit (spike, saw, block, slope) instead of "object".

## v1.24.2
- Fixed presses near portals being super delayed (+17t, +35t). Only a press at most 4 ticks before a gamemode / size portal is held now (it was anything within 40px, about 30 ticks), and it fires at most 6 ticks after you reach the portal: on the first safe tick, or at that limit. Clicks queued behind it no longer get shifted by a huge amount.

## v1.24.1
- UFO / swing: pressing while touching an orb now uses the orb on that same tick in the prediction, with no flap first (like the game). This was making the orb click look deadly at every timing.
- Learn from attempts is mini cube only again (in UFO it was firing presses far too late at old spots).

## v1.24.0
- A press right before a gamemode or size portal is no longer passed through raw: it's held until you're through the portal, then fired on the first safe tick (the prediction can see again there). Not in ship / wave.

## v1.23.3
- With Click Between Frames, buffered clicks were firing up to a whole tick later than planned (a click lands mid-tick, held clicks fire on tick boundaries). Predictions now start from the exact point inside the tick and held clicks fire on the exact tick that was tested. Matters most for frame-perfect clicks.

## v1.23.2
- Predictions copy all of your player's jump / fall / slope / timer state, not just a few values. The leftover "press waiting" state was still making UFO predictions flap on their first tick.

## v1.23.1
- Fixed predictions starting with an extra UFO flap whenever you were holding (the cause of normal UFO being a few pixels off).
- Learn from attempts: a click is held for a learned spot only a few ticks ahead, and only if waiting is safe (long holds made the UFO fall and press below the orb).

## v1.23.0
- Exact orb contact: the prediction asks the game's own collision when you touch an orb (its real hitbox) instead of estimating it - for frame-perfect orb clicks.
- One-tick self-check in Stats: how often the prediction matches the game exactly after one tick, per gamemode, and by how much it differs. Diagnostics only.

## v1.22.2
- Removed the "no safe moment found" hold: clicks the buffer can't improve go straight through right away, like before v1.19.0.
- Those lines only show in the Log with "Log: show safe clicks" on.

## v1.22.1
- Moving objects that speed up / slow down (eased move triggers) are now predicted - before, only steady movement was, so most moving spikes were treated as standing still. They're also trusted faster.

## v1.22.0
- Moving spikes and orbs are predicted where they will be (not where they are now) in every gamemode except ship and wave. Windows that open when a spike moves out of the way can be buffered now.

## v1.21.1
- UFO gets full learn from attempts: held UFO clicks fire on spots that worked before, and clicks on spots that killed you before are held and re-planned.

## v1.21.0
- Learn from attempts now also works for UFO.
- An early click the prediction can't line up (a portal or orb ahead, or no safe moment found) is held for the spot where a press worked on an earlier attempt, even through a gamemode portal, and fires when you reach it.

## v1.20.2
- Diagnostics: Stats > PREDICTION ACCURACY shows which way predictions are off per gamemode (sideways vs up/down), and so does each "prediction off" log line.

## v1.20.1
- Reverted v1.20.0: switching gamemode inside the prediction broke real portals. Portals work exactly like v1.19.2 again.

## v1.20.0
- Gamemode and size portals no longer stop the prediction: it switches through them, so clicks just before a portal (like an orb right after a UFO portal) can be buffered.

## v1.19.2
- UFO / swing: clicks the buffer can't fix go through as made again, instead of being held (the prediction was wrong in some UFO parts and held clicks never fired).

## v1.19.1
- UFO / swing: holding the button no longer counts as clicking orbs in the prediction (in the game, only a fresh click uses an orb there). This made held UFO clicks never fire.
- A held click that's checked every tick now fires just before doing nothing would kill you, instead of waiting.

## v1.19.0
- Fixed early clicks being called "too late": the quick search stepped over narrow safe moments far from the click. Now (cube, UFO, robot, ball, spider, swing) such a click is held and checked every tick for the whole window, and fires on the first safe tick.

## v1.18.8
- Fixed every orb click saying "too late, no delay helps" (a v1.18.6 change made the prediction ignore the orb you were clicking).

## v1.18.7
- "too late" and "no fix" log lines say what the predicted death hits and whether the prediction used an orb.

## v1.18.6
- Fixed: every click on an orb went raw. After the prediction used the orb, the same orb stopped it on the next tick. Used orbs are now ignored for the rest of the prediction.

## v1.18.5
- Clicks on an orb you're touching are predicted through the orb instead of going raw ("raw: pink orb (touching)").

## v1.18.4
- The Log now says when inputs pass through because another mod stops the buffer's physics hook (it used to stay silent).
- Stats > CLICKS shows how many inputs reached the buffer, so "nothing in the Log" can be told apart from "the buffer never sees my clicks".

## v1.18.3
- A deadly click that runs out of time is finished with quick checks instead of going through raw (what made the old Predictive Buffer keep working on Grief / Slaughterhouse). Stats counts these clicks.

## v1.18.2
- Heavy levels (Grief, Slaughterhouse): far fewer "raw: CPU budget" clicks. The first check of a click always gets enough time, the search gets its own budget, cube checks stop right after landing, and wave / ship searches do less extra work.
- Stats > PERFORMANCE shows the cost per predicted step and whether the level is light / medium / heavy.

## v1.18.1
- Fixed presses being swallowed after pausing while holding (the release in the pause menu never reached the mod).
- The mod never presses on its own to "fix" the button state any more.
- Safety nets: if the game's physics hook isn't running (another mod, a hitch), inputs go straight through; a held input is always released within 600 ms.
- CPU budget checked more often, so object-heavy levels (Grief, Slaughterhouse) can't overrun it by much.

## v1.18.0
- Less chop: held clicks are re-checked once per tick (not on every Click Between Frames sub-step) with a smaller time budget.
- Removed a wasted extra prediction per buffered click; the "how early was it" log check is much cheaper.
- Moving-hazard tracking only runs in mini cube.
- Stats > PERFORMANCE shows re-check cost, frame time and the mod's worst cost per frame.

## v1.17.1
- Wave "randomly goes up": the hidden prediction player now copies your ground / portal / landing / sliding state, so good releases aren't held back.

## v1.17.0
- Changes tab in the window, and this changelog on the mod's page.

## v1.16.2
- Wave wobble: spam taps are judged against your own hold / gap rhythm again, and a burst of spam keeps one fixed delay until you pause.

## v1.16.1
- "forget level" is always in the Stage tab (outside a level it tells you to open one).

## v1.16.0
- Wave spam: taps in one burst share the same delay instead of each getting a different one.

## v1.15.1
- A release made while a press is held fires exactly on time after it (keeps your hold length).

## v1.15.0
- Two engines: mini cube keeps the new one; every other gamemode is back to the v1.10.2 behaviour.
- Every mode: a held click fires on its planned tick at the latest.

## v1.14.3
- Wave / ship: clicks that run out of CPU time go through raw again; held clicks with no plan give up after 1 frame.

## v1.14.2
- Wave / ship judged against your own rhythm (fewer normal taps treated as deadly).

## v1.14.1
- Learn from attempts and near-miss waits: presses only. Queued releases held at most 2 frames.

## v1.14.0
- Modes tab: buffer on / off per gamemode, normal and mini separately.

## v1.13.2
- Held clicks fire exactly on their plan (was 2 ticks late). Moving-hazard speeds must be proven before they're used.
- New window look.

## v1.13.1
- Learned spots are saved per level between sessions. "forget level" button.

## v1.13.0
- Fixed held clicks that never fired ("held click hadn't fired yet"): they now fire on their plan.

## v1.12.3
- Window Key is Left Alt (new setting, old saved keys don't stick). Window turns back on once.

## v1.12.2
- Window Key read straight from the keyboard (works with Click Between Frames).

## v1.12.1
- Out of CPU on a deadly click: re-planned live instead of raw. Log says when / why each held click fired.
- Window works in menus too.

## v1.12.0
- Learn from attempts: remembers where inputs worked or killed you on a level.

## v1.11.0
- Near-miss check, moving-hazard prediction, Custom stage with Apply.

## v1.10.2
- Cube live check uses your real hold length. Log shows the gamemode and "too late" clicks.

## v1.10.0
- Wider windows for every stage. Live path preview with hitboxes.

## v1.9.0
- Extreme: live re-planning for clicks and releases. Deaths counted once. Left Shift window, half size.

## v1.8.0
- One Stage setting (Off, 1-4, Extreme). Every jump key works. Dense check right after a click.

## v1.7.0
- Draggable window (Log / Stats / Stage). Timing coach removed.
