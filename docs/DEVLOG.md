# Development journal

Maintained by [Complicatons](https://github.com/Complicatons). Entries below summarise the existing private Git history; they are not backdated public announcements. The public journal was first prepared on 17 October 2026.

## 17 October 2026 — Online firearms and animated hit regions

- Connected browser firearm shots and reload requests to the online connection stack. Recoil, aiming and original first-person animations run in the browser; inventory counts and damage remain server-owned.
- Added the original player's 23 animated hit regions, following the head, torso and limbs through standing, walking and crouching poses.
- Added server wildlife collision for targeting and checked player, animal and world-object shot reports through the project's own server mock.
- Verified online combat, offline gameplay and original viewmodels on the RTX 4090. All 187 automated checks pass.

Real Legacy server interoperability remains unverified. Melee, bows, throwables and placement still need online integration; animation, effects and interface fidelity also remain unfinished. There is no public playable release yet.

![Original M4 sights during the online mock-server check](../assets/screenshots/online-gun-aim.png)

Actual local prototype capture, 17 October 2026. Development controls remain visible. Implementation, detailed protocol notes and recovered assets stay private.

## 17 October 2026 — Online inventory, equipment and respawn

- Connected the inventory and crafting windows to server updates. Moving items, taking loot and crafting send requests; item counts change when the server confirms them.
- Added original clothing changes for remote players, original loot sacks and clothed sleeping-player models with collision.
- Connected server health, bleeding and metabolism, plus death and respawn. Clicking Respawn waits for the server to create and place a new character.
- Verified the online flows and narrow inventory layout on the RTX 4090. All 182 automated checks pass; the offline gameplay/save/repair regressions also pass.

These are prototype checks through our own server mock. Real Legacy server interoperability, combat/placement routing, full animation/HUD fidelity and production hosting still need work. There is no public playable release yet.

| Server inventory | Original sleeper and loot models |
| --- | --- |
| ![Server inventory window in the prototype](../assets/screenshots/server-inventory.png) | ![Clothed sleeping player and loot sacks](../assets/screenshots/sleeper-loot.png) |

Actual local prototype captures from 17 October 2026. Implementation, detailed engineering notes and recovered game assets remain private.

## 17 October 2026 — GPU validation and online presentation

- Verified full gameplay, save/reload, repair and first-person held models on an NVIDIA RTX 4090 in Microsoft Edge/WebGL2.
- Added original remote-player models and unarmed movement animations, plus server-driven wildlife movement, attack and death presentation.
- Added original online campfire flames, smoke, sparks and light, controlled by server state.
- Checked the website-to-game join through the account service, gateway and server adapter using the project's own UDP server mock. Website and two-client transport checks also pass.
- Kept engineering checkpoints and AI handoff notes current in the private implementation repository.

The connection stack is implemented and mock-tested. **No real Legacy server interoperability has been demonstrated yet.** Online inventory, equipment and several gameplay actions remain unfinished. Remote clothing/held items, full animation blending and the original HUD still need work; this is not a public playable release.

| Original M4 sights | Online campfire effects |
| --- | --- |
| ![Original M4 sights rendered in Edge](../assets/screenshots/m4-aim.png) | ![Server-controlled campfire rendered in the browser](../assets/screenshots/online-fire.png) |

Actual local prototype captures from 17 October 2026, with unfinished development controls visible. The campfire capture uses our mock server through the full connection stack.

## 17 October 2026 — Combat and environmental survival

- Added local firearm, bow, grenade and explosive-charge behaviour, with wearable armour. Weapon viewmodels, hitboxes and several effects remain unfinished.
- Connected the recovered day/night clock to changing light and survival. Night cold consumes extra calories; clothing and lit fires offer protection.
- Connected the original radiation zones, wearable radiation protection and existing radiation metabolism/anti-rad items.
- Continued browser interaction checks and recorded clear handoff checkpoints so development can move between assistants.

This remains a local prototype. Sky and material rendering approximate the original presentation. These changes do not establish original-server compatibility or a public playable release. The selected gateway/server-adapter route remains the planned path to shared browser/desktop servers.

Validation: 78 automated logic/data checks pass. The installed Edge gameplay and narrow-layout check passes, including night cold, fire warmth and radiation protection, with no page/console errors or external requests. A separate two-client check passes for our local movement transport; it does not use an original Legacy server.

| Day | Night |
| --- | --- |
| ![Local prototype in daylight](../assets/screenshots/day.png) | ![The same prototype view at night](../assets/screenshots/night.png) |

Actual local prototype captures from 17 October 2026. The damaged hut follows the building/combat test; development controls and unfinished visuals are visible.

## 17 October 2026 — Building and camp life

Networking planning update: investigated existing-server gateway options and historical Legacy approval hooks. Added [the server integration plan](SERVER-INTEGRATION.md), distinguishing unchanged-server access from operator-installed identity adapters. No native server connection has yet been demonstrated.

- Work on deployables, cooking and camp respawn.
- Building work covering structures, hardpoints and placed doors.
- Public project journal prepared with screenshots, roadmap and an origin record.

Private history references: `0998755` and `bb26ba1`. The three screenshots in the main README show this day's local prototype. These are development snapshots, not a published multiplayer release.

## 16 October 2026 — Establishing the browser port

- Initial project committed.
- Imported world exploration, doors and loot.
- Resource gathering and item export corrections.
- Rebuilt the visible world from the client scene, corrected sea level and worked on wildlife.
- Metabolism, bleeding, eating and medical item work.

Private history references: `645c5e5`, `b77a132`, `d7673c3`, `c759f55` and `c579f99`.

## Next journal entries

Future entries should include a date, a concrete change, a screenshot or other evidence where useful, and known limitations. Performance and compatibility claims should identify how they were measured. Releases will be announced explicitly when a public playable build exists.
