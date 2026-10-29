# Roadmap

Updated 29 October 2026. Rust Legacy as a desktop browser game. Keeping the original appearance and behaviour is the priority.

```text
Overall   ███████████████████░  93%
```

The [project overview](../README.md#progress--29-october-2026) has the area-by-area breakdown. The website has the **[full dated update history](https://rustlegacy.co.uk/roadmap)**, with pictures and clips for every finished piece.

**[Play the island right now, in your browser →](https://rustlegacy.co.uk/play)** No account or download needed to look around. Joining a real community server still needs the first public game server (see below).

## Done

| Area | What works |
| :--- | :--- |
| Entry flow | Original main menu over the original menu scene, Options (quality, FOV, key rebinding, FPS counter), server browser, loading screen, in-game Escape menu and death screen |
| World | The original island and buildings, solid rocks and cliffs, terrain trees with distance detail, terrain detail chosen by the original rule, time-of-day sky, stars and moon phases, the original sea, original lighting and shaders, grass, sun shadows, six original quality presets and post-processing |
| Movement | The original character movement rules exactly: acceleration, hills, jumping, and sliding along rocks and walls without being pushed through them |
| Survival | Gathering, 61 blueprints, metabolism, bleeding, radiation, cold, cooking, research kits, loot crates, dropped items and death bags |
| Wildlife | Chickens, rabbits, boar, stags, wolves, bears, mutant wolves and mutant bears with their original AI, coats, sounds and attacks |
| Building and raiding | Structures, deployables, doors, code locks, decay, spike walls, fires, the repair bench, the original placement preview, and raiding with the original explosive and damage rules |
| Combat | Firearms, bows, hand cannon, grenades that bounce and roll, C4, attachments, flashlight and laser, recoil, aim drift, draw sounds, muzzle flash, tracers, impacts, metal sparks, explosion flashes, melee hitting the ground, ragdolls, hit markers and directional damage |
| Inventory | Original windows, drag-and-drop, list scrolling, button colours, close buttons and sounds |
| Social | Chat (works with the inventory open), push-to-talk voice, name tags, F1 console from the main menu with server commands |
| Airdrops | C130 plane, parachute crate, smoke and loot |
| Online client | Inventory, crafting, building, combat, vitals, wildlife and airdrops controlled by the server; two browser players meet, see each other and fight on the original server |
| **The original server** | Browser players join the original 2014 server on a sealed-off cloud test machine: 100 players at once, a 3-hour run without a drop, a restart mid-game, half a second of added lag with no kicks, and automated crafting, building, door, combat and wildlife checks |
| Anti-cheat and admin | Server-side checks for shooting or using through walls, noclip, hovering, speed, teleports, fire rate, melee and arrow line of sight; admin roles, bans, reports and audit log, every admin action tested end to end; bans follow the person, not just the account |
| Loading | First join in about 20 s, return visits in about 3 s, a clear message when a browser can't run the game, tested in Edge, Firefox and Chrome |
| Website | Live at [rustlegacy.co.uk](https://rustlegacy.co.uk): the island [playable at /play](https://rustlegacy.co.uk/play), accounts (username/password or Steam), server list, wiki with 39 guides and a resource calculator, detailed island map, forum, leaderboards, dated roadmap, opening-day sign-ups |
| Server owner tools | **Rust Legacy Host**, a full Windows app: one-download install, attaches an existing server as it is, a setup wizard, health graphs, Discord alerts, scheduled restarts and wipes, a settings and plugin editor, off-site backups and signed updates. Installed and ran the original server on a real test machine for five days |
| Desktop players | A launcher that signs in with the same website account, including creating the account from inside the launcher |

**1,116+ automated tests pass**, plus GPU checks of every major system on an RTX 4090, and tests run automatically on every change (GitHub Actions).

## Next — in order

### 1. Finish testing on the original server

Joining, gathering, crafting, building, combat, death and respawn, and a 100-player 3-hour run already pass. Still to check: the last admin and anti-cheat tests on the original server.

### 2. Switch on the public game server

The machine is prepared and the server-owner app is ready to run on it. This is the remaining step before the first server can open and appear in the website's server list.

### 3. First community servers

- Open a **PvP server** first.
- Then open an **EU server** in the following week.
- The community decides on the **wipe schedule** (for example monthly), **group limits** and server rules on [Discord](https://discord.gg/4NjPbkFnpf).

### 4. Website extras

Discord sign-in and account emails (password reset, email checks) are switched off until they are set up.

### 5. Desktop players

The launcher and its sign-up are built. It's being finished and tested for release alongside the first server.

### 6. Polish

Lower-end hardware, ragdoll joint limits, the code-lock dialog styling, and bugs reported by players.

[Screenshots](SCREENSHOTS.md) · [Development journal](DEVLOG.md) · [Project overview](../README.md)
