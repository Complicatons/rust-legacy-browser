<p align="center"><img src="assets/banner.svg" alt="Rust Legacy Browser — a browser port project by Complicatons" width="100%"></p>

<p align="center">
  <img alt="Status: local prototype" src="https://img.shields.io/badge/STATUS-LOCAL_PROTOTYPE-e96938?style=for-the-badge">
  <img alt="Creator: Complicatons" src="https://img.shields.io/badge/CREATOR-Complicatons-242a30?style=for-the-badge">
  <img alt="Documented development: October 2026" src="https://img.shields.io/badge/DEVELOPMENT-OCT_2026-242a30?style=for-the-badge">
</p>

<p align="center"><strong>The original island. The familiar survival experience. A browser as the destination.</strong></p>

This project aims to bring **Rust Legacy into a modern browser**, preserving its original world and gameplay rather than designing a different survival game. Created and led by **[Complicatons](https://github.com/Complicatons)**, with AI-assisted development.

This repository is the project's public development journal: real prototype screenshots, dated milestones, architectural plans and a roadmap. The implementation is maintained privately. **There is no public playable release yet**, and compatibility with existing Legacy servers has not been demonstrated.

<p align="center"><a href="docs/DEVLOG.md">Development journal</a> · <a href="docs/SCREENSHOTS.md">Screenshots</a> · <a href="docs/ROADMAP.md">Roadmap</a> · <a href="docs/ARCHITECTURE.md">Accounts & servers</a> · <a href="docs/PROJECT-ORIGIN.md">Project origin</a></p>

## Current build — 19 October 2026

![Original island compound in the current desktop browser prototype](assets/screenshots/2026-10-19/island-compound.png)

*Actual desktop browser capture. Development controls remain visible; the final menu and visual presentation are unfinished.*

The core survival prototype now runs locally in a desktop browser. Recent work rebuilt the inventory around the original separate windows, added item dragging and details, physical dropped-item bags, clothed ragdolls, surface-specific bullet effects, and saved FOV and fullscreen controls.

| Area | Implemented in the prototype | Still to complete or prove |
| :--- | :--- | :--- |
| Original island | Recovered terrain, buildings, trees, rocks, collision and doors | Lighting, sky, water, shader and overall visual parity |
| Survival and camp life | Gathering, wildlife, hunger, bleeding, medical items, radiation, warmth, cooking, storage and respawn | Remaining behaviour differences and final gameplay comparison |
| Inventory and crafting | Separate desktop windows, armour effects, item details/dragging, original container layouts, batch crafting and dropped-item pickup | Remaining item actions and exact interface polish |
| Building and combat | Structures, placement, deployables, firearms, bows, grenades, explosives and weapon attachments | Remaining physics, animation and effect fidelity |
| Player presentation | Original first-person models/clips, remote clothing/aiming, ragdolls and death camera | Original-engine motion and transition comparison |
| Desktop controls | Mouse capture/release, optional fullscreen, saved 60–120 FOV slider and synchronized F1 console command | Complete original menu, Play → server chooser → loading → game flow |
| Multiplayer | Website-to-game join and server-owned state exercised through the project mock stack | Real Legacy server compatibility and browser/desktop shared-world testing |
| Accounts and directory | Local sign-in/account flows, stable identity, server registration and one-use join tickets | Production provider configuration, hosting and operator pilot |

**Verified development checkpoint:** 306 automated tests pass, along with focused RTX 4090 checks for inventory, crafting, FOV, weapon zoom, mouse capture and fullscreen. Full offline gameplay and online mock-stack browser regressions also pass. This is development evidence, not a completed port or a public release.

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-19/desktop-inventory.png" alt="Rebuilt separate desktop inventory, armor and crafting windows"></td>
<td width="50%"><img src="assets/screenshots/2026-10-19/grenade-explosion.png" alt="Grenade explosion during a browser mock-server test"></td>
</tr>
<tr><td align="center">Rebuilt original-style desktop inventory</td><td align="center">Combat effects in the online mock test</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-19/dropped-item.png" alt="Dropped item bag with a pickup prompt"></td>
<td><img src="assets/screenshots/2026-10-19/options.png" alt="Options with saved field of view, fullscreen and mouse release settings"></td>
</tr>
<tr><td align="center">Dropped items and pickup</td><td align="center">FOV, fullscreen and mouse controls</td></tr>
</table>

**[View the complete latest gallery: 22 reviewed screenshots →](docs/SCREENSHOTS.md)**

## What we are building next

1. Reconstruct the original opening screen, Play button, server chooser and loading flow; replace the developer explorer interface in the player experience.
2. Finish desktop visual fidelity across inventory, HUD, weapons, animations, effects, lighting, sky and water.
3. Complete remaining item interactions and gameplay/physics differences, then address performance and browser bugs.
4. Run the final isolated real-server tests, including browser and desktop players sharing a server, persistent identity, reconnects and saves.
5. Configure the hosting/operator pilot and release only a documented, tested supported experience.

There is no announced release date. See the [detailed roadmap](docs/ROADMAP.md) for the remaining work and validation boundaries.

## Where this is going

The intended experience is straightforward: visit the website, sign in, browse community servers and join from the browser. Your stable account identity would let each server recognise you across sessions and IP changes. Each server would retain its own world, inventory and progression, subject to that server's wipe policy.

**For the first release, server owners will need to install our browser connection package.** Browser players need a website account and no installed client; existing desktop players may optionally link their character to use that same server identity in the browser. Read [the guide for players and server owners](docs/PLAYERS-AND-SERVER-OWNERS.md) for the planned steps and requirements.

The planned system combines a browser client, website accounts, a server directory and a bridge operated alongside each participating game server. Existing Legacy servers would need a compatible bridge and verified protocol support before browser players could join. [Read the proposed hosting design →](docs/ARCHITECTURE.md)

## Follow the work

- **Watch** this repository for documentation and progress updates.
- Read the [dated journal](docs/DEVLOG.md) and [delivery roadmap](docs/ROADMAP.md).
- Use [issues](https://github.com/Complicatons/rust-legacy-browser/issues) for feedback and well-documented suggestions. Please read [the contribution guide](CONTRIBUTING.md) first.

The first recorded development commits are dated **16 October 2026**. This public journal begins **17 October 2026**. [The origin record](docs/PROJECT-ORIGIN.md) identifies the private source snapshot behind this first publication without exposing its contents.

---

**Unofficial community project.** Rust Legacy and its original content belong to their respective rights holders. This project is not affiliated with or endorsed by Facepunch. No original game files, recovered assets or server binaries are distributed here. See [rights and attribution](RIGHTS.md) and [publication policy](docs/PUBLICATION-POLICY.md).
