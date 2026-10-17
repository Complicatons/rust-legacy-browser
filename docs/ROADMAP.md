# Roadmap

This is a direction of travel, not a release schedule. No launch date has been announced.

| Stage | Status | Scope |
| :--- | :--- | :--- |
| World and survival foundation | Local prototype | Original environment, collision, doors, gathering, wildlife and survival systems |
| Building and player interactions | Local prototype | Structures, deployables, items, camp life and respawn; continued fidelity testing |
| Combat and environment | Local prototype | Firearms, bows, explosives, armour, day/night cycle, night cold and original radiation zones; visual and animation fidelity still incomplete |
| Browser polish and validation | In progress / remaining | Interface, audio, visual parity, loading, performance and broader browser testing |
| Multiplayer compatibility | Planned / unverified | Protocol investigation, bridge implementation and controlled end-to-end testing |
| Accounts and server directory | Planned | Website sign-in, stable player identity, server enrolment and server-scoped join tickets |
| Hosting pilot | Planned | One controlled server, persistence, reconnects, backups and operational monitoring |
| Community server support | Planned | Versioned bridge packages, operator documentation, registration and compatibility checks |
| Public availability | Future milestone | Distribution arrangements, reliable hosting and a clearly documented supported experience |

## What must be demonstrated before a multiplayer release

- Browser clients can join, interact and reconnect reliably.
- The server validates player actions and persists player/world state.
- The same account maps to the same player when the browser or IP changes.
- Join credentials cannot be reused on a different server or impersonate another player.
- Server operators can install, update, back up and restore the supported stack.
- The release clearly states supported browsers, server versions and known limitations.

Original Legacy server compatibility remains a research and validation task. A bridge is part of the proposed design; its existence alone would not establish compatibility with arbitrary online servers.
