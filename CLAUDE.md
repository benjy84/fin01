# Project Sentinel

A 2D browser game for a parent and their 13 year old son to build together and learn from.

## Ground rules
- Everything lives in a single `index.html` file (HTML, CSS and JavaScript together). Use the HTML5 canvas, no libraries and no build step, so it deploys to Vercel as a plain static site.
- Keep the code simple and well commented so a teenager can read and change it.
- Controls are keyboard and mouse.
- Commit after each working change with a clear message.
- Work on a branch for each new feature, and keep `main` always playable.
- Build in small steps: get one thing working before adding the next.

## Game design (from the son's original prompt)
- Reverse-horror, pixel-art, side-scrolling action game with some platforming. The player is the thing the enemies should fear.
- Player: the Sentinel, a huge armoured super-soldier. Dirty greys and dark greens, helmet hides the face. Movement should feel heavy, not floaty.
- Attacks (planned): punch, shoot, stomp, tear.
- Enemies: crimson insectoid aliens with yellow eyes. Variants planned: standard, lurker, brute, ranged, elite.
- Setting: a research laboratory overrun by green alien growth. Muted, gritty colours.
- Human survivors can be rescued or killed; rescued and killed counts shown at the end of a level.
- Planned campaign: 15 levels. Levels 3, 7 and 15 are outdoors on the planet surface, with an environmental support meter and shelters. All the others are inside the laboratory.
- Only inventory is a weapon scroll. HUD stays minimal.
- Pixel grid: draw at 320x180 and scale up, so everything keeps a consistent pixel-art look.

## Build order
1. Basic page with the canvas (done).
2. Sentinel that walks, jumps and punches (done, first playable version).
3. One alien that chases the player and dies with a little gore (done).
4. One small room (done: kill 8 aliens to clear it).
5. Also done: crouch, shotgun with mouse-wheel weapon scroll, stomp, and sound (all made in code with Web Audio, no sound files; M mutes).
6. Rooms: each room is an entry in the `ROOMS` list in `index.html` (size, how much you can see, platforms, enemy mix). Room 2 is 3x wider with a scrolling camera, a bigger field of view (480x270) and large "brute" aliens. Add `#room2` to the web address to jump straight to it; Enter goes to the next room after clearing one.
7. Next: the tear attack; then more enemy types, survivors, outdoor levels and the full 15 levels, one branch at a time.

The original prompt asked for Godot; we chose plain JavaScript and canvas instead so the game stays a static site on Vercel.
