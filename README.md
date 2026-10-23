<p align="center"><img src="assets/banner.svg" alt="Rust Legacy Browser — a browser port project by Complicatons" width="100%"></p>

<p align="center">
  <img alt="Overall progress: 93%" src="https://img.shields.io/badge/PROGRESS-93%25-e96938?style=for-the-badge">
  <img alt="Status: closed development" src="https://img.shields.io/badge/STATUS-CLOSED_DEVELOPMENT-242a30?style=for-the-badge">
  <a href="https://rustlegacy.co.uk"><img alt="Website: rustlegacy.co.uk" src="https://img.shields.io/badge/WEBSITE-RUSTLEGACY.CO.UK-e96938?style=for-the-badge"></a>
  <img alt="Creator: Complicatons" src="https://img.shields.io/badge/CREATOR-Complicatons-242a30?style=for-the-badge">
</p>

<p align="center"><strong>The original island. The familiar survival experience. Nothing to download.</strong></p>

**Rust Legacy, running in a modern browser.** This project brings back the original Rust Legacy world and gameplay rather than designing a new survival game. You open a web page and play. You don't need a launcher, a loader or an executable. Created and led by **[Complicatons](https://github.com/Complicatons)**, with AI-assisted development.

This repository is the public development journal: real screenshots, progress and the roadmap. The game's code is kept private.

**The website is live at [rustlegacy.co.uk](https://rustlegacy.co.uk)**, with the wiki, the island map, the full dated roadmap and [opening-day sign-ups](https://rustlegacy.co.uk/launch). Join the [Discord](https://discord.gg/4NjPbkFnpf) to follow along.

<p align="center"><a href="docs/SCREENSHOTS.md"><b>Screenshots</b></a> · <a href="docs/ROADMAP.md"><b>Roadmap</b></a> · <a href="docs/DEVLOG.md"><b>Development journal</b></a> · <a href="docs/PLAYERS-AND-SERVER-OWNERS.md"><b>Players & server owners</b></a> · <a href="docs/SERVER-FILE-SCANS.md"><b>Server file scans</b></a></p>

![The warehouse compound from the air, in the browser](assets/screenshots/2026-10-20/town-aerial.jpg)

*The original warehouse compound, rendered in the browser (20 October 2026 build).*

<p align="center"><a href="assets/video/gameplay-tour-2026-10-20-v4.mp4"><img src="assets/video/tour-preview.gif" alt="Flying over the island in the browser (preview of the gameplay video)" width="560"></a></p>

<p align="center"><a href="assets/video/gameplay-tour-2026-10-20-v4.mp4"><b>▶ Download the 3½-minute gameplay video (MP4, 53 MB)</b></a>: the original menus, gathering, crafting, building a full base, guns, hunting, wildlife, raiding, multiplayer, night time and airdrops, with in-game sound.</p>

<table>
<tr>
<td align="center" width="25%"><h2>93%</h2><sub>overall progress</sub></td>
<td align="center" width="25%"><h2>1,116</h2><sub>automated tests passing</sub></td>
<td align="center" width="25%"><h2>100</h2><sub>browser players at once on the original server</sub></td>
<td align="center" width="25%"><h2>3 s</h2><sub>to rejoin the island</sub></td>
</tr>
</table>

## Latest updates — 22 & 23 October

### 100 players on the original server

We filled the **original 2014 Rust Legacy server** on our sealed-off cloud test machine with **100 browser players** at once (ping 101 ms). It ran for **3 hours 17 minutes without a drop**, was stopped mid-game and started again, and survived half a second of added lag with no kicks. Two test bots now play the whole game against the server: they craft, build a base, lock a door, cook, raid, hunt, fight and loot each other.

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-23/matrix-base.jpg" alt="A base built by a test bot"></td>
<td width="50%"><img src="assets/screenshots/2026-10-23/matrix-door-code.jpg" alt="A test bot opening a locked door with the code"></td>
</tr>
<tr><td>Test run: a bot built this base itself, from foundation to ceiling</td><td>Test run: the second bot was refused at the locked door, then typed the owner's code and got in</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-23/matrix-loot.jpg" alt="Looting the loser's sack after a fight"></td>
<td><img src="assets/screenshots/2026-10-23/bad-network-500ms.jpg" alt="A test player on the original server with added lag"></td>
</tr>
<tr><td>Test run: after the fight, the winner opens the loser's loot sack, armour and all</td><td>Test run on the original server with half a second of added lag and 5% packet loss</td></tr>
</table>

### We played the whole game

We played the browser game start to finish, alone and online, from the menu to raiding a base, and fixed everything that behaved differently from the original. Movement, jumping, gunfire, grenades, ragdolls, animals, building rules, blueprints, crafting, menus, chat and the console were all checked against the original game's code again. Repairing with wood works, mutants drop their loot sacks, and you keep your blueprints when you die.

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-23/playtest-raid.jpg" alt="A door blown off by an explosive charge"></td>
<td width="50%"><img src="assets/screenshots/2026-10-23/playtest-repair.jpg" alt="Repairing a damaged doorway with wood"></td>
</tr>
<tr><td>An explosive charge took the door; the doorway behind is at half health</td><td>…and repairing it with wood: "Healed 100 (802/1000)"</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-23/mutant-sack.jpg" alt="A mutant wolf's loot sack"></td>
<td><img src="assets/screenshots/2026-10-23/rpos-repair-bench.jpg" alt="The repair bench window"></td>
</tr>
<tr><td>A mutant wolf's loot sack beside its body</td><td>The repair bench shows what a repair costs</td></tr>
</table>

### Tools for server owners

The **host app** that runs a Legacy server, our gateway and the website together now installs from **one download** as its own Windows service. It has pages for players, cheat evidence, world saves, linked accounts and updates with one-click roll back.

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-23/host-anticheat.jpg" alt="Cheat evidence in the host app"></td>
<td width="50%"><img src="assets/screenshots/2026-10-23/host-backups.jpg" alt="World saves in the host app"></td>
</tr>
<tr><td>Cheat evidence on the demo server: every flag with its measurements and the player's path</td><td>World saves kept by the freeze watchdog and by hand</td></tr>
</table>

**[All the new screenshots →](docs/SCREENSHOTS.md)** · **[Every update, day by day →](https://rustlegacy.co.uk/roadmap)**

## Progress — 23 October 2026

```text
Overall   ███████████████████░  93%
```

| Area | Progress | Working now | Left to do |
| :--- | :--- | :--- | :--- |
| **Original world and graphics** | `██████████` 95% | The original island with all its buildings, rocks and trees, the ground now shaped exactly like the original's terrain. Day/night sky, stars and moon, the original sea with reflections, original lighting and shaders, grass, shadows, terrain detail by the original rule and six quality presets | Final side-by-side comparison with the original (lighting, tall grass) |
| **Survival, gathering and wildlife** | `██████████` 97% | Gathering, 61 blueprints, crafting, hunger, bleeding, radiation, cold, cooking, research kits, loot crates. Chickens, rabbits, boar, stags, wolves, bears and mutants with the original AI, coats, sounds and attacks; hunting checked on the original server | Small behaviour differences |
| **Building and raiding** | `██████████` 96% | Foundations to roofs, doors, code locks, storage, sleeping bags, decay, spike walls, fires, the repair bench window, the original placement preview, and raiding with grenades and C4 using the original damage rules; building, doors and fires checked on the original server | Last raid checks on the original server |
| **Weapons and combat** | `██████████` 96% | Rifles, pistols, shotguns, bows, hand cannon, grenades and C4. Sights, silencer, flashlight and laser. Recoil, aim drift, original melee impacts, explosion sounds, tracers, ragdolls, the death camera and hit markers; melee fights between two players checked on the original server | Last combat checks on the original server |
| **Menus, HUD and social** | `██████████` 99% | Original main menu, options, key rebinding, server browser and loading screen. Inventory windows with the original drag-and-drop, scrolling, colours and sounds; F1 console from the main menu, chat over the inventory, push-to-talk voice and name tags | Small UI polish |
| **Online play** | `██████████` 95% | The server controls inventory, crafting, building, combat, vitals, airdrops and wildlife. Two browser players meet, see each other and fight on the original server; movement now matches the original's rules exactly | Last gameplay checks on the original server |
| **First real server** | `███████▌░░` 75% | Browser players join the original server on a sealed-off cloud test machine. 100 browser players at once, a 3-hour run without a drop, a restart mid-game, +500 ms lag with no kicks, two-player meets and fights, and automated crafting, building, door, combat and wildlife checks. The public game server is prepared | Admin and cheat tests on the original server, then switching on the public game server |
| **Website, accounts and server list** | `█████████░` 90% | Live at rustlegacy.co.uk: accounts (username/password or Steam), server list, wiki with 39 guides and a calculator, island map, roadmap with pictures for every entry, forum, leaderboards, opening-day sign-ups, search-engine and security polish | Discord sign-in and account emails |
| **Anti-cheat and admin tools** | `████████▌░` 85% | Server-side checks for wall shots, noclip, hovering, speed, teleports, fire rate, melee and arrow line of sight, doors and aim snapping, plus item-transfer evidence and desktop-player combat checks. Admin roles, bans, reports and an audit log; every cheat test flagged and normal play clean | Tuning with real players |
| **Performance and release polish** | `████████▌░` 88% | First join in 20 s, return visits in about 3 s, a clear message when a browser can't run the game, recovery after a graphics reset, tested in Edge, Firefox and Chrome, stable memory over long play | Lower-end hardware |

*The percentages are the project's own estimates, weighted by how much each area matters for a playable public server.*

## Screenshots

**[See all screenshots, with labels →](docs/SCREENSHOTS.md)**

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-20/main-menu.jpg" alt="The original main menu"></td>
<td width="50%"><img src="assets/screenshots/2026-10-20/server-browser.jpg" alt="The original server browser"></td>
</tr>
<tr><td align="center">The original main menu, in the browser</td><td align="center">Server browser</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-20/m4-holo-aim.jpg" alt="Aiming an M4 with a holo sight"></td>
<td><img src="assets/screenshots/2026-10-20/bear.jpg" alt="A bear in the warehouse yard"></td>
</tr>
<tr><td align="center">M4 with holo sight</td><td align="center">Bear in the warehouse yard</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-20/coast-sunset.jpg" alt="Sunset over the original sea"></td>
<td><img src="assets/screenshots/2026-10-20/airdrop-plane.jpg" alt="Airdrop plane overhead"></td>
</tr>
<tr><td align="center">Sunset over the original sea</td><td align="center">Airdrop plane</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-20/raid-grenade-doorway.jpg" alt="A doorway destroyed by a grenade"></td>
<td><img src="assets/screenshots/2026-10-20/inventory-crafting.jpg" alt="Inventory, armor and crafting windows"></td>
</tr>
<tr><td align="center">Raiding</td><td align="center">Inventory, armor and crafting</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-20/options-fov-fps.jpg" alt="Options with the Field of View slider and FPS counter"></td>
<td><img src="assets/screenshots/2026-10-20/in-game-fps-counter.jpg" alt="In game with the FPS counter on"></td>
</tr>
<tr><td align="center">Field of View slider (60–120) and FPS counter option</td><td align="center">FPS counter in game (top right)</td></tr>
</table>

## What happens next

1. **Finish testing on the original server.** Crafting, building, combat and long runs with several players. Joining and gathering already work.
2. **Install on the public game server.** The machine is ordered and running; the original server and our bridge go on it next.
3. **First PvP server.** Open a PvP server for the community, followed by an EU server.
4. **Community decisions.** Wipe schedule, group limits and server rules are being decided with the players on [Discord](https://discord.gg/4NjPbkFnpf).
5. **Desktop players.** A launcher so the same website account can join from the original desktop game too.

See the [roadmap](docs/ROADMAP.md) for detail.

## How it will work for players

Visit the website, sign in, choose a server, play. Your account keeps your identity across sessions, so servers recognise you even when your IP changes. Each server keeps its own world, inventory and wipe schedule.

Because the game runs in the browser, there is nothing to install. You don't need a third-party launcher or a modified client to join. [Guide for players and server owners →](docs/PLAYERS-AND-SERVER-OWNERS.md)

## Follow the project

- **Sign up** at [rustlegacy.co.uk/launch](https://rustlegacy.co.uk/launch) to hear when the servers open.
- **Join** the [Discord](https://discord.gg/4NjPbkFnpf).
- **Watch** this repository for updates.
- Read the [development journal](docs/DEVLOG.md).
- Use [issues](https://github.com/Complicatons/rust-legacy-browser/issues) for feedback and suggestions. Please read [the contribution guide](CONTRIBUTING.md) first.

The first development commits are dated **16 October 2026**. This public journal started on **17 October 2026**. [Project origin →](docs/PROJECT-ORIGIN.md)

---

**Unofficial community project.** Rust Legacy and its original content belong to their respective rights holders. This project is not affiliated with or endorsed by Facepunch. No original game files, recovered assets or server binaries are distributed here. The original server files used for testing were security-checked: [server file scans](docs/SERVER-FILE-SCANS.md). See [rights and attribution](RIGHTS.md) and the [publication policy](docs/PUBLICATION-POLICY.md).
