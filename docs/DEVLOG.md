# Development journal

Maintained by [Complicatons](https://github.com/Complicatons). Entries below summarise the existing private Git history; they are not backdated public announcements. The public journal was first prepared on 17 October 2026.

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
