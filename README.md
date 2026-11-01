# Signal Spire — Roblox prototype

An original, playable horror-obby slice inspired only by the broad “climb a tower while a monster threatens you” genre. It does **not** reuse another game's scripts, models, branding, map, or assets.

## Open and play in Roblox Studio

1. Open Roblox Studio.
2. Choose **File → Open from File…** and select [`SignalSpire.rbxlx`](SignalSpire.rbxlx) in this folder.
3. The saved place now contains the tower, ledges, scenery, and lighting in **edit mode**. If the viewport looks empty, select Workspace in Explorer and press **F** (Focus) to frame the scene.
4. Press **Play** (or **F5**) to test. The server script intentionally removes the static preview model and rebuilds the same world with touch handlers, HUD, checkpoints, collectibles, and the Echo hazard. This avoids duplicate geometry while making the place easy to inspect before Play.
5. Use WASD or the mobile movement joystick and Space or the mobile jump button to climb. Follow the section-colored ledges, touch the broad checkpoint platforms, collect optional gold shards, and reach the beacon.
6. Let the warning appear and watch the Echo rise. Stop the test and inspect **View → Output** if anything errors. Test jump reachability and mobile readability before publishing.
7. Stop the test and use **File → Save to File As…** to save your own working copy before editing.

If Studio does not open the place file on your computer, create a Baseplate, insert a normal **Script** under **ServerScriptService**, paste the contents of [`src/SignalSpire.server.lua`](src/SignalSpire.server.lua) into it, and press Play. Do not place this server script in Workspace or ReplicatedStorage.

## Prototype features

- Four ascending spiral sections with an edit-mode-visible course, colored section landmarks, tower ribs, floating ruins, and a beacon.
- Neon edge signals, checkpoint lighting, a night atmosphere, and restrained bloom for contrast and navigation.
- Teal shared checkpoints grant the current server a progress-preserving respawn point.
- The rising Echo has an advance warning and a simple original Warden silhouette built from basic Parts; checkpoint landings are safe.
- Optional Echo Shards are collectibles, not requirements to finish or paid power.
- Session-only leaderboard values: Stage, Shards, Escapes. No cross-session saving yet.
- The default Roblox avatar controls work on desktop and mobile; no plugins, packages, external assets, or purchases are needed.
- [`tools/build_place.py`](tools/build_place.py) regenerates the static edit-mode scene and embeds the current server source into the XML place.

## Current limits

This is an improved prototype, not a finished or revenue-ready game. The Echo Warden is a simple built-in-part silhouette rather than an animated character; no custom audio, permanent data saving, robust replay loop, or monetization is included. It has not been tested in Roblox Studio from this workspace. Playtest on PC and phone, inspect Output, and adjust jumps, warning timing, visibility, and hazard safety based on real experience before publishing.

## Files

- [`SignalSpire.rbxlx`](SignalSpire.rbxlx) — human-readable Roblox place file; open it in Studio.
- [`src/SignalSpire.server.lua`](src/SignalSpire.server.lua) — editable source for the server-generated game.
- [`docs/competitor-notes.md`](docs/competitor-notes.md) — reference facts, hypotheses, and playtest checklist.
- [`tools/build_place.py`](tools/build_place.py) — deterministic static-world builder and source synchronizer.

## Next milestones

1. Test the place alone on desktop and phone. Check that every jump is reachable, warning text is understandable, and respawns work.
2. Run a small friend playtest. Ask where they got confused, what felt fair, and whether they wanted another round—do not assume more time played always means more fun.
3. Replace placeholder geometry, monster visuals, and sounds with original assets.
4. Add server-side DataStore saving only after the session loop behaves correctly; use a separate test experience, not production player data.
5. Review Roblox Creator Dashboard analytics after a small release and improve based on retention, completion, device performance, and player feedback.
6. Consider optional, clearly priced cosmetics only once the free core game is enjoyable. Do not sell power or required progress in the first prototype.

Publishing requires your account and Creator Hub actions; this project will not publish itself. Roblox eligibility and policies can change. Check current official guidance in the research notes before release. Income is never guaranteed.
