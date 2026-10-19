# Roadmap

Updated 19 October 2026. This is a desktop browser game. Preserving the original Rust Legacy appearance and behaviour is the priority. No launch date or completion percentage has been announced.

## Working prototype foundation

| Area | Current evidence |
| :--- | :--- |
| Original world and survival | Local browser world, collision, doors, gathering, wildlife, survival, cooking and respawn |
| Building and combat | Local structures/deployables, placement, firearms, bows, explosives, armour and attachments; online requests/state exercised against the project mock |
| Inventory and crafting | Rebuilt separate desktop windows, drag/move, item details, armour effects, original container cell arrangements, batch crafting and server-confirmed inventory changes |
| Dropped items and death | Local physical bags/pickup, server pickup presentation routes, clothed ragdolls and death-camera presentation; exact original physics remains unproven |
| Effects and controls | Surface-specific impacts, original tracer/decal presentation, FOV slider/F1 synchronization, mouse capture/release and fullscreen |
| Accounts and connections | Website/account/directory and browser-to-bridge join flows tested locally with a project mock server |

The latest recorded checkpoint has 306 passing automated tests, focused hardware-GPU browser checks, and passing full offline/online mock-stack regressions. Passing these checks does not establish native-server compatibility or exact original-engine fidelity.

## Remaining implementation — in priority order

### 1. Original desktop entry flow

- Reconstruct the original main-menu scene and layout, Play button, server chooser and loading screen.
- Connect that flow to website sign-in and real participating-server listings without losing the account/join handling already built.
- Replace the developer explorer panel in the player experience. Keep developer tools separate from normal play.
- Ensure menus, mouse capture, fullscreen, loading failures and disconnects work together cleanly.

### 2. Original appearance and presentation

- Compare inventory, crafting, container windows, tooltips and HUD against original references; complete spacing, text and interaction polish.
- Complete remaining player animation events/transitions and compare first-person and remote-player poses.
- Improve lighting, sky, water, particles and shaders; current rendering is still an approximation in several areas.
- Compare ragdoll motion, contacts, movement and death-camera details with the original in the final runtime phase.

### 3. Remaining gameplay and browser work

- Complete remaining original item actions, including the unfinished research/blueprint, split and unload interactions.
- Resolve remaining melee/collision and other source-behaviour differences.
- Extend online pickup checks through the complete mock stack; existing presentation/unit checks are not a substitute for that coverage.
- Improve startup/loading, frame rate, memory use and long-session stability on a documented range of desktop hardware and browsers.
- Continue fixing demonstrated bugs, including issues reported while trying the local demo.

### 4. Final isolated native-server validation

Do this after the implementation work above. Real Legacy server compatibility has **not** been demonstrated.

- Join a controlled real server and verify authentication, spawn, movement, combat, inventory, crafting and building.
- Verify browser and desktop players can share the same server/world and see consistent actions.
- Test stable account identity, optional desktop-character linking, death/respawn, reconnects, saves and server wipes.
- Check supported server versions and mods explicitly; do not label arbitrary servers as compatible.
- Perform original-engine visual/behaviour comparisons in the isolated test environment.

### 5. Hosting pilot and release preparation

- Configure production identity providers and hosting; verify sessions, ticket expiry, server-authoritative actions and abuse controls.
- Validate operator installation/update, backups, restore and monitoring on one controlled participating server.
- Publish the supported browser/hardware/server requirements, known limitations and operator documentation.
- Resolve distribution requirements before announcing public availability.

## Intended player experience

Browser players visit a website, sign in and join a verified participating server without installing a game client. Server owners install and operate the bridge. Linking an existing desktop character is optional. Each server retains its own world, inventory, progression and wipe policy.

[Latest screenshots](SCREENSHOTS.md) · [Development journal](DEVLOG.md) · [Project overview](../README.md)
