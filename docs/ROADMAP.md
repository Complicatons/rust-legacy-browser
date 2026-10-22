# Roadmap

Updated 22 October 2026. Rust Legacy as a desktop browser game. Keeping the original appearance and behaviour is the priority.

```text
Overall   █████████████████░░░  83%
```

The [project overview](../README.md#progress--22-october-2026) has the area-by-area breakdown. The website has the **[full dated update history](https://rustlegacy.co.uk/roadmap)**, with pictures and clips for every finished piece.

## Done

| Area | What works |
| :--- | :--- |
| Entry flow | Original main menu over the original menu scene, Options (quality, FOV, key rebinding, FPS counter), server browser, loading screen, in-game Escape menu and death screen |
| World | The original island and buildings, solid rocks and cliffs, terrain trees with distance detail, time-of-day sky, stars and moon phases, the original sea, original lighting and shaders, grass, sun shadows, six original quality presets and post-processing |
| Movement | The original character movement: sliding along rocks and walls, never pushed through them |
| Survival | Gathering, metabolism, bleeding, radiation, cold, cooking, medical items, research kits and blueprints, loot crates, dropped items and death bags |
| Wildlife | Chickens, rabbits, boar, stags, wolves, bears, mutant wolves and mutant bears with their original AI, sounds and animations |
| Building and raiding | Structures, deployables, doors, code locks, decay, the original placement preview, and raiding with the original explosive and damage rules |
| Combat | Firearms, bows, hand cannon, grenades that bounce and roll, C4, attachments, flashlight and laser, recoil, aim drift, draw sounds, muzzle flash, tracers, impacts, metal sparks, explosion flashes, melee hitting the ground, ragdolls, hit markers and directional damage |
| Inventory | Original windows, list scrolling, button colours, close buttons and sounds |
| Social | Chat, push-to-talk voice, name tags, F1 console with server commands |
| Airdrops | C130 plane, parachute crate, smoke and loot |
| Online client | Inventory, crafting, building, combat, vitals, wildlife and airdrops controlled by the server, tested against the project's own test server |
| **The original server** | Browser players join the original 2014 server on a sealed-off cloud test machine, see its resource nodes and gather, and get its starting items. 4 test bots played 22 minutes with no kicks or disconnects |
| Anti-cheat and admin | Server-side checks for shooting or using through walls, noclip, aim snapping and command spam; admin roles, bans, reports and audit log, every admin action tested end to end |
| Loading | First join in 25 s (was 83 s), return visits in about 3 s, 167 MB download (was 210 MB); tested in Edge, Firefox and Chrome; fullscreen play so Ctrl+W can't close the tab |
| Website | Live at [rustlegacy.co.uk](https://rustlegacy.co.uk): accounts (username/password or Steam), server list, wiki with 39 guides and a resource calculator, detailed island map, dated roadmap, opening-day sign-ups |
| Server owner tools | A host app that runs the server, gateway and website together, restarts a frozen server and keeps the last good save; or run everything with scripts |

**917 automated tests pass**, plus GPU checks of every major system on an RTX 4090.

## Next — in order

### 1. Finish testing on the original server

Joining, gathering and a 22-minute multi-player run already pass. Still to check on the original server: crafting, building, combat, death and respawn, reconnects, and hours-long runs with several players.

### 2. Install on the public game server

The game server machine is ordered and running. The original server and our bridge go on it next, then it appears in the website's server list.

### 3. First community servers

- Open a **PvP server** first.
- Then open an **EU server** in the following week.
- The community decides on the **wipe schedule** (for example monthly), **group limits** and server rules on [Discord](https://discord.gg/4NjPbkFnpf).

### 4. Website extras

Discord sign-in and account emails (password reset, email checks) are switched off until they are set up.

### 5. Desktop players

A small launcher so the same website account can join from the original desktop game as well as the browser. The website side (signing a launcher in with a code) is built.

### 6. Polish

Lower-end hardware, ragdoll joint limits, the code-lock dialog styling, and bugs reported by players.

[Screenshots](SCREENSHOTS.md) · [Development journal](DEVLOG.md) · [Project overview](../README.md)
