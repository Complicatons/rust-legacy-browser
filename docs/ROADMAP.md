# Roadmap

Updated 20 October 2026. Rust Legacy as a desktop browser game. Keeping the original appearance and behaviour is the priority.

```text
Overall   ███████████████░░░░░  76%
```

The [project overview](../README.md#progress--20-october-2026) has the area-by-area breakdown.

## Done

| Area | What works |
| :--- | :--- |
| Entry flow | Original main menu over the original menu scene, Options (quality, FOV, key rebinding, FPS counter), server browser, loading screen, in-game Escape menu and death screen |
| World | The original island and buildings, terrain trees with distance detail, time-of-day sky, stars and moon phases, the original sea, original lighting and shaders, grass, sun shadows, six original quality presets and post-processing |
| Survival | Gathering, metabolism, bleeding, radiation, cold, cooking, medical items, research kits and blueprints, loot crates, dropped items and death bags |
| Wildlife | Chickens, rabbits, boar, stags, wolves, bears, mutant wolves and mutant bears with their original AI, sounds and animations |
| Building and raiding | Structures, deployables, doors, code locks, decay, and raiding with the original explosive and damage rules |
| Combat | Firearms, bows, hand cannon, grenades, C4, attachments, flashlight and laser, recoil, muzzle flash, tracers, impacts, ragdolls, hit markers and directional damage |
| Social | Chat, push-to-talk voice, name tags, F1 console with server commands |
| Airdrops | C130 plane, parachute crate, smoke and loot |
| Online client | Inventory, crafting, building, combat, vitals, wildlife and airdrops controlled by the server, tested against the project's own test server |
| Anti-cheat and admin | Server-side checks for shooting or using through walls, noclip, aim snapping and command spam; admin roles, bans and audit log |

**614 automated tests pass**, plus GPU checks of every major system on an RTX 4090.

## Next — in order

### 1. First real-server test

All online play so far runs against the project's own test server. Next, connect browser players to a real Legacy server through the bridge and check joining, movement, combat, inventory, crafting, building, death and reconnects end to end.

### 2. First community servers

- Open a **PvP server** first.
- Then open an **EU server** in the following week.
- The community decides on **wipe schedule** (for example monthly), **group limits** and server rules.

### 3. New website

Sign in (email, Steam or Discord), server list with one-click join, island maps and a wiki. The design is finished and the build is under way.

### 4. Polish

- Texture compression for faster loading.
- Testing on more desktop hardware and browsers.
- Remaining small fidelity items: ragdoll joint limits, code-lock dialog styling, animation polish.
- Bugs reported by players.

### 5. Server owners

Documentation and an install package for server owners who want browser players on their own Legacy servers. See the [guide for players and server owners](PLAYERS-AND-SERVER-OWNERS.md).

[Screenshots](SCREENSHOTS.md) · [Development journal](DEVLOG.md) · [Project overview](../README.md)
