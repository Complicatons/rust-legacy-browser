<p align="center"><img src="assets/banner.svg" alt="Rust Legacy Browser — a browser port project by Complicatons" width="100%"></p>

<p align="center">
  <img alt="Overall progress: 93%" src="https://img.shields.io/badge/PROGRESS-93%25-e96938?style=for-the-badge">
  <img alt="Status: closed development" src="https://img.shields.io/badge/STATUS-CLOSED_DEVELOPMENT-242a30?style=for-the-badge">
  <a href="https://rustlegacy.co.uk"><img alt="Website: rustlegacy.co.uk" src="https://img.shields.io/badge/WEBSITE-RUSTLEGACY.CO.UK-e96938?style=for-the-badge"></a>
  <img alt="Creator: Complicatons" src="https://img.shields.io/badge/CREATOR-Complicatons-242a30?style=for-the-badge">
</p>

<p align="center"><strong>The original island. The familiar survival experience. Nothing to download — or, if you prefer, a small installer that plays the original game too.</strong></p>

**Rust Legacy, running in a modern browser.** This project brings back the original Rust Legacy world and gameplay rather than designing a new survival game. You open a web page and play. You don't need a launcher, a loader or an executable. Created and led by **[Complicatons](https://github.com/Complicatons)**, with AI-assisted development.

This repository is the public development journal: real screenshots, progress and the roadmap. The game's code is kept private.

**The website is live at [rustlegacy.co.uk](https://rustlegacy.co.uk)**, with the wiki, the island map, the full dated roadmap and [opening-day sign-ups](https://rustlegacy.co.uk/launch). **[Play the island right now, in your browser →](https://rustlegacy.co.uk/play)** Join the [Discord](https://discord.gg/4NjPbkFnpf) to follow along.

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
<td align="center" width="25%"><h2>5</h2><sub>days the server-owner app ran unattended on a real server</sub></td>
</tr>
</table>

## Latest updates — 24–29 October

### Play it right now

**[rustlegacy.co.uk/play](https://rustlegacy.co.uk/play)** is live: the recovered island, open in your browser, no account or download needed to look around. This is the single-player island explorer the whole port has been verified against — joining a real community server still needs the first public game server, which is prepared and waiting to switch on.

### A real app for server owners

**Rust Legacy Host** stopped being a folder of scripts and became an actual Windows program: its own window, a tray icon, a boot screen that checks and starts each part in order, and a terminal docked at the side for quick commands. It now installs from **one download**, and an owner with a server already running can **point the installer at it and attach it as it is** — no reinstall, one code to link it to the website.

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-29/host-boot.jpg" alt="Rust Legacy Host starting up"></td>
<td width="50%"><img src="assets/screenshots/2026-10-29/host-installer-server.jpg" alt="The installer checking an existing server folder"></td>
</tr>
<tr><td>Starting up: each part checked and started in order (demo server)</td><td>The installer checks an existing server's SHA-256 and works out if it can be made browser-ready</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-29/host-attach.jpg" alt="Attaching an existing server as it is"></td>
<td><img src="assets/screenshots/2026-10-29/host-terminal.jpg" alt="The host app dashboard with a docked terminal"></td>
</tr>
<tr><td>"An existing server, as it is" — the owner's own copy, untouched</td><td>The dashboard with a terminal docked at the side, restarting the gateway (demo server)</td></tr>
</table>

It now also has a setup wizard instead of sixteen separate scripts, health graphs and Discord alerts, scheduled restarts and wipes with countdown warnings in chat, a settings and plugin editor, a one-button health check, off-site backups, and signed updates it checks before installing.

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-29/host-setup.jpg" alt="The host app setup wizard"></td>
<td width="50%"><img src="assets/screenshots/2026-10-29/host-health.jpg" alt="Player and server health graphs"></td>
</tr>
<tr><td>Setup as a guided list of steps, with its own plan and live output</td><td>Players, response time and resource use over the last day and week (demo data)</td></tr>
<tr>
<td><img src="assets/screenshots/2026-10-29/host-schedule.jpg" alt="A restart counting down with warnings"></td>
<td><img src="assets/screenshots/2026-10-29/host-settings.jpg" alt="Server settings explained in plain English"></td>
</tr>
<tr><td>A scheduled restart counting down, players already warned (demo server)</td><td>Every server setting with a short explanation of what it does</td></tr>
</table>

We installed it on a real Windows test server for the first time. It ran the **original Rust Legacy server** there: saving and quitting cleanly, restarting on schedule, wiping the map, and greeting players — then kept running **unattended for five days**, which is how we found and fixed a crashed game server that was never being started again.

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-29/vm-host-overview.jpg" alt="Rust Legacy Host running the original server on a real machine"></td>
<td width="50%"><img src="assets/screenshots/2026-10-29/host-offsite.jpg" alt="Off-site backups"></td>
</tr>
<tr><td>Rust Legacy Host running the original game server on the test machine</td><td>World saves copied off-site on a schedule, encrypted if the owner likes (demo server)</td></tr>
</table>

### Sign up without leaving the desktop launcher

Players who want the original desktop game as well as the browser can now make their website account **inside the launcher itself**, with ticks to remember their name and stay signed in. One account works in both.

<table>
<tr>
<td width="50%"><img src="assets/screenshots/2026-10-29/launcher-signup.jpg" alt="Creating a website account inside the desktop launcher"></td>
<td width="50%"><img src="assets/screenshots/2026-10-29/remote-torch-night.jpg" alt="Another player's lit torch at night"></td>
</tr>
<tr><td>The launcher's Create account screen (demo data)</td><td>We checked every message the original server sends the game, and back: another player's torch now lights up the way the original server really tells it to</td></tr>
</table>

**[All the new screenshots →](docs/SCREENSHOTS.md)** · **[Every update, day by day →](https://rustlegacy.co.uk/roadmap)**

## Progress — 29 October 2026

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
| **Website, accounts and server list** | `█████████░` 92% | Live at rustlegacy.co.uk, with the island playable at **[/play](https://rustlegacy.co.uk/play)**: accounts (username/password or Steam), server list, wiki with 39 guides and a calculator, island map, roadmap with pictures for every entry, forum, leaderboards, opening-day sign-ups, search-engine and security polish | Discord sign-in and account emails |
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

1. **Finish testing on the original server.** The last admin and cheat checks; everything else already passes, including a 100-player, 3-hour run.
2. **Switch on the public game server.** The machine and the server-owner app are both ready; this is the step left before the first server can open.
3. **First PvP server.** Open a PvP server for the community, followed by an EU server.
4. **Community decisions.** Wipe schedule, group limits and server rules are being decided with the players on [Discord](https://discord.gg/4NjPbkFnpf).
5. **Desktop players.** The launcher that lets the same website account play the original desktop game is built and sign-up works inside it; it's being finished for release alongside the first server.

See the [roadmap](docs/ROADMAP.md) for detail.

## How it will work for players

Visit the website, sign in, choose a server, play. Your account keeps your identity across sessions, so servers recognise you even when your IP changes. Each server keeps its own world, inventory and wipe schedule.

Because the game runs in the browser, there is nothing to install. You don't need a third-party launcher or a modified client to join — **[try it now at /play](https://rustlegacy.co.uk/play)**. If you'd rather play the original desktop game, a small official launcher signs in with the same account. [Guide for players and server owners →](docs/PLAYERS-AND-SERVER-OWNERS.md)

## Follow the project

- **Sign up** at [rustlegacy.co.uk/launch](https://rustlegacy.co.uk/launch) to hear when the servers open.
- **Join** the [Discord](https://discord.gg/4NjPbkFnpf).
- **Watch** this repository for updates.
- Read the [development journal](docs/DEVLOG.md).
- Use [issues](https://github.com/Complicatons/rust-legacy-browser/issues) for feedback and suggestions. Please read [the contribution guide](CONTRIBUTING.md) first.

The first development commits are dated **16 October 2026**. This public journal started on **17 October 2026**. [Project origin →](docs/PROJECT-ORIGIN.md)

---

**Unofficial community project.** Rust Legacy and its original content belong to their respective rights holders. This project is not affiliated with or endorsed by Facepunch. No original game files, recovered assets or server binaries are distributed here. The original server files used for testing were security-checked: [server file scans](docs/SERVER-FILE-SCANS.md). See [rights and attribution](RIGHTS.md) and the [publication policy](docs/PUBLICATION-POLICY.md).
