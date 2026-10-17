# Playing in the browser: a guide for players and server owners

**Planned experience — browser multiplayer is not available yet.** This guide explains the first release we intend to build. Installation packages, linking commands and compatibility are still being developed and tested.

## For players

### How will I play?

Visit the project website, sign in, choose a server marked **Browser ready**, and join. You will not need to install our desktop client or gateway. Your browser runs the game graphics; the selected server runs the shared world.

### Can I join the server I already play on?

For the first release, its owner will need to install our supported browser connection package. We call this the **bridge**. It lets browser players connect and lets the server recognise their accounts.

A server being online for desktop players does not automatically make it browser ready. If your favourite server has not enabled support, you can keep joining it through your desktop client. Browser access to unchanged servers is being investigated separately and is not promised.

### Can I keep my existing character and items?

That is the goal on supported servers. You will need to link your website account to your existing character **on that server**:

1. Sign into the project website.
2. Join your usual server using your desktop client and existing character.
3. Use the server's account-linking command to receive a private, temporary code.
4. Enter that code in the website's **Link existing character** screen.
5. Once linking is confirmed, disconnect from desktop and join the same server through the browser.

The command and screen names are not final. The code proves you can access the existing character. **Typing the same username does not prove it is yours.** Never share a linking code with another person.

The server would use the same saved identity for your linked character, including its inventory and building ownership where supported. We must verify this against each supported server setup before offering it. Normal server wipes and rules still apply.

### What if I am a new player?

On servers that support new browser accounts, you will sign in and join to create a new character. You will not need a desktop character first. Support for using that newly created character in a desktop client is a separate compatibility feature; we will state where it is available.

### Will I need to link every time?

No. The intended link is permanent until deliberately changed. Signing into the same website account lets the same server recognise you again, even if your IP address, computer or display name changes. You will need a separate link for an existing character on another server.

### Are my items stored in my website account?

Your website account proves who you are. Each game server keeps its own characters, items and world. Your inventory on Server A does not travel to Server B. Linking does not copy saves to the website or protect them from that server's wipes.

### Can I use desktop and browser at the same time?

The planned rule is one active connection per character. Disconnect from one before joining with the other. Linking does not create a second copy of your items or let two players control the same character.

### What if I cannot access my old desktop character?

Do not create a link by guessing its name or number. Recovery will need the server owner's supported process and enough evidence of ownership. We cannot promise recovery for every community client or server setup.

## For server owners

### What would I install?

Our planned **browser connection package**, or bridge, has two parts:

| Part | What it does |
| --- | --- |
| Gateway | Receives browser connections and translates game network traffic |
| Server adapter | Checks browser admission and connects each verified website account to the correct saved player identity |

The first supported setup will run the gateway alongside your game server. The adapter may be a plugin or a server extension, depending on the exact Legacy build and available hooks. We will list supported combinations; we are not promising one plugin that works with every server.

### Do I replace my game server or move my world?

The intended design keeps your original Legacy server and its saves. You continue to run the world, control its rules and manage its players. Your game server does not have to be hosted by us. Our website supplies the browser client, accounts and server list.

Keep backups and test on a copy before enabling support on a live world. We will not advertise an installation as preserving saves until that combination has passed reconnect, restart and restore tests.

### Can desktop players stay?

Yes, supporting desktop and browser players in the same world is a release requirement. The bridge adds a browser entry point while desktop players retain their existing connection method. That behaviour must be tested on each supported server setup.

### How would I enable browser support?

The intended process is:

1. Check that your server build and hosting provider support the package.
2. Back up your world, player saves and configuration, then prepare a test copy.
3. Install the matching gateway and adapter; configure the secure browser address.
4. Register the server with the project and prove that you control it.
5. Run the connection, account-linking, desktop-player and save checks.
6. Enable the listing once it passes, so players can see it as **Browser ready**.

Some hosting providers may need to allow an additional service and network port. Exact requirements and installation instructions will accompany a tested package. No install command or downloadable bridge is available yet.

### What stays under my control?

Your world, server rules, local bans, player progress and wipe schedule remain your responsibility. Players' website passwords are not shared with you; the adapter receives verified account information needed to admit and recognise players.

### How will the server list work?

Only supported, registered servers that pass the required checks will be offered as browser-playable. A familiar server name or an open game port is not enough. Listings should state compatibility and availability clearly; offline or incompatible servers should not appear ready to join.

## The first release in one sentence

**Players sign into the website; participating server owners install the bridge; existing players link their character once so the server knows who they are.**

For the research and implementation milestones, see [the server integration plan](SERVER-INTEGRATION.md). This guide describes the intended experience, not a released service or a guarantee of compatibility with existing online servers.
