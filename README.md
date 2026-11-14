# Awesome Chatto

This is an *Awesome Chatto* list curated for the Chatto Community by nickk @ [Chatto HQ](https://chat.chatto.run) Server.

Chatto is a *A fully-featured team and group chat application that you can easily selfhost*. It is free to use, lightweight, easy to spin up and manage, and respects your privacy. Its international community is very friendly.

---

![Awesome](https://awesome.re/badge-flat2.svg)

NB: Chatto currently is pre-1.0 software. Consequently, some breakage *will* occur. Most authors are on Chatto HQ, so stop by and share your experiences.  

Chatto hit 0.5.0 on Nov 9th. Thus, most entries here assume 0.5 servers. Do **not** install 0.4 at this point.  

NB: For those operators that followed 0.5.0 release candidate cycle -- if you use Docker, just make sure you switch from *chatto:next* to *chatto:latest* now.  

## Table of Contents

* [Deployment](#deployment)
* [Frontend](#frontend)
* [Bots](#bots)
* [Agents](#agents)
* [Bridges](#bridges)
* [Libraries](#libraries)
* [Migration Hints](#migration-hints)
* [Further Reading and Listening](#further-reading-and-listening)

## Deployment 

### Proxmox Virtual Environment/LXC, and Incus
- MickLesk's Community Script: https://community-scripts.org/scripts/chatto, MIT  
  This closely follows Chatto's release cycle.

### AWS Lightsail 
- jessedc's **chatto-on-lightsail**: https://github.com/jessedc/chatto-on-lightsail, MIT  
  [0.4] Lightsail is AWS's Virtual Private Server (VPS) offering. This repository guides you through installing Chatto 0.4 on Lightsail.

### Nix
- abl's **nix-chatto**: https://github.com/abl/nix-chatto, *Nix flake for the Chatto release binary*, MIT  
  [0.4] Nix is a package manager, and NixOS is a Linux distribution based on Nix. It allows for reproducible builds and deployments, think "OS as code" - a declarative system configuration. A *Flake* can be imagined as part of a pipeline that builds these declarations, so nix-chatto is a quasi-installer for Chatto on NixOS.  
  NB: Deliberately on Chatto's stable cycle.

### Installation Variants

- lizzard77's **chatto-ttrpg-patches**: https://github.com/lizzard77/chatto-ttrpg-patches, AGPL-3.0  
  A collection of patches for Chatto's upstream source that provide an improved tabletop / pen & paper role-playing game experience. Example functionality added: Dice support, and an image annotation functionality (i.e. for shared world maps and the like).
- poga's **Emergency Box** for Civil Protection scenarios: https://github.com/poga/emergency-box, *A chat room that lives on your wifi and keeps working when the Internet dies*, AGPL-3.0  
  [0.4] "It's a 1 shot script for setting up a Chatto Server on a MacBook which allows anyone on the same LAN to join. Includes some built-in bots for fetching news if there's still intermittent internet connection."

### Operations Helpers 

- SeanGSR's **chatto-admin** as alternative to Chatto's *Operator CLI*: https://github.com/SeanGSR/chatto-admin, *A community made Admin Panel for Chatto*, MIT  
  [0.4] Chatto 0.4 has made a deliberate security/AX choice of having certain administration functionality exposed only at its *Operator CLI* for the time being. If you need or want to have a web interface nevertheless - including all the potential drawbacks that might bring - this project is for you. Make sure you and your agent read its SECURITY.md before deploying. 
	
## Frontend

### App Wrappers
These applications are native wrappers around Chatto's web frontend. This results in a standalone experience that includes native OS notifications, and badges.  
  
*Since 0.5, there are official ChattoCorp desktop apps (Linux, macOS, Windows) with the PWA remaining an excellent choice.*  

NB: If compatibility between your App wrapper and a server breaks due to different upgrade policies, you can always use that server's native web interface.  
  
- Kaihanga's **Solander**, a Tauri shell: https://github.com/jrimmer/solander-desktop, *Chatto desktop client*, Apache-2.0  
  [0.4] As of 2026-08-09, this was tested with Chatto Server 0.4.8 only - but likely works with later 0.4 releases. It just shows 0.4.8 on its User Interface because that was the PWA's version that got "app wrapped".  
- Teal's Tauri shell: https://github.com/teal-bauer/chatto-tauri, AGPL-3.0+  
  The very first community-made shell, follows Chatto's (beta/RC) release cycle. 

### Browser extensions
These enrich Chatto's standard web client experience. 
- SeanGSR's Chromium extension: https://github.com/SeanGSR/chatto-enhancer, *Chatto Enhancer*, MIT  
  [0.4] Currently aimed at Chatto 0.4. The extension provides enhancements for voice/video chat UI and chat bar (namely: Emoji picker, Giphy integration, local nicknames, enhanced theming, and Markdown controls).  
  NB: It's likely that SeanGSR will update the extension as soon as the feature set for Chatto 0.5 stabilises.  
        
### Alternative clients
These are alternative Chatto client implementations, usually focussing on text (chat) experience - leaving out audio and video calls.  
  - Beardicus' **chatline**: https://tangled.org/beardic.us/chatline, *A command-line bot client for Chatto.*, Apache-2.0  
    Spiritual sibling to "slackline". Includes a SKILL.md, has an agent-friendly ``chatline serve``, and works with Claude Code's *channels*. Implemented in Golang.  
  - Teal's **chatto-cli**: https://github.com/teal-bauer/chatto-cli, *Command-line client for Chatto (chatto.run)*, AGPL-3.0+  
    Probably the very first alternative client for Chatto. Text mode, implemented in Golang. Less of a classic client UI, more of a command-line interface to participating on a Server.
  - Felix's **chatto-native**, i.e. Python/Tk and Tcl/Tk clients: https://github.com/TheCodemancerLtd/chatto-native, MIT  
    [0.4] Initially a Proof of Concept that even older stacks are able to connect to Chatto. 
  
To keep on using your Matrix client, see also *Bridges* below.

## Bots

### Golang
- PaulK's **Cheapo**: https://forgejo.netdome.biz/paul/cheapo, *A CLI that finds all those free games from all those game stores. And, if you want, posts them to a Chatto channel.*, AGPL-3.0+  
  Inspired by ``free-games-claimer`` and ``free-games-notifier``. No browser/Playwright or login needed. Detects and reports free game offers on Epic, GoG, Steam. MCP server included.

### Python
- Teal's **chatto-bot**: https://github.com/teal-bauer/chatto-bot, *Python bot framework for Chatto — decorator-based commands, cog system, WebSocket subscriptions*, AGPL-3.0+  
  This is probably the first ever bot for Chatto.
- Felix's **robochatto**: https://github.com/TheCodemancerLtd/robochatto, *A bot demonstrator based on chattolib*, MIT  
- Isotopp's **chatto-rss-bridge**: https://github.com/isotopp/chatto-rss-bridge, *Read messages from RSS and post them into a chatto.run channel*, Unlicense  
  The bot and its feeds can be managed by @mention-ing. 

### Rust
- Jacklak's **TOGPCB**: https://github.com/jacklak-redstone/TOGPCB, *That One General Purpose Chatto Bot*, Apache-2.0  
  Some Discord servers employ YAGPDB, a multi-purpose bot. Jacklak's project aims at being Chatto's YAGPDB one day. It's in its early stages, but might be an interesting scaffold for your own extensions.
- TimesZ's **Chatto Tidal Bot**: https://github.com/Times-Z/tidal-bot-chatto, *A music bot for Chatto that plays Tidal HiFi streams in voice channels via LiveKit*, GPL-3.0  
  NB: This was the very first 0.5+ entry we had on *Awesome Chatto!*

### TypeScript
- Griffo's **Airhornchatto**: https://tangled.org/griffo.tngl.sh/airhornchatto *The infamous Airhorn Discord Bot, reimagined for Chatto*, Apache-2.0  
  Inspired by [/airhorn](https://airhorn.solutions/). Has a `docker-compose.yml` on board for easy deployment.

## Agents

  - [0.4] Kaihanga's **Hermes Chatto Plugin**: https://github.com/jrimmer/hermes-chatto-plugin/, *Chatto platform adapter plugin for Hermes Agent — WebSocket realtime, ConnectRPC API, thread support, dynamic room discovery*, MIT
  - PaulK's **Hermes Chatto Plugin**: https://forgejo.netdome.biz/paul/hermes-chatto-plugin, *Full-featured Hermes Chatto Plugin. So you can use Chatto to talk to your Hermes Agent*, MIT  
  This first started out as a fork of Kaihanga's work, and vendored in Felix' *chattolib*. 
  - ncmro's **channels** for Pi: https://github.com/ai-outfitter/channels, *Pi extension: push channel events (email/Slack/Signal/GitHub) into an agent session; wake only on real work.*, MIT  
  This Pi extension watches notifications/mentions on different inbound channels (e.g. Chatto) and runs a durable Pi session on a match.

## Bridges

A *bridge* is a special kind of bot that allows for Rooms being connected to at least one other Room (or "channel") on another Server or even service. Content is shared between the connected Rooms/channels, so governance, data, and trust boundaries become fuzzy. Before deploying, ensure consent of admins/owners and Communities involved.  

NB: You totally could build a bridge using one of the alternative clients listed above. 

### Chatto -- Discord
  - Felix's **chatto-bridge**: https://github.com/TheCodemancerLtd/chatto-bridge, *Discord ↔ Chatto bridge bot (discord.py + chattolib + NATS)*, MPL-2.0  
  Felix says this is in its early days, but it might help communities help to migrate.  

### Chatto -- Matrix
  - else's **mautrix-chatto**: https://github.com/elsbrock/mautrix-chatto, *Chat with Chatto communities via Matrix.*, AGPL-3.0+  
  Lets Matrix users participate in Chatto servers/communities with their preferred Matrix client. Does not bridge calls, but is aware of them.  
  Works with Ghost Bots on both sides. On Chatto's end, an anchor member account lazily creates a ghost bot as a stand-in for each Matrix user that does not have a Chatto identity of their own. So, check with your Chatto server administrator about bot creation permission and limits. Fallback: classic relay behaviour (one shared account with a name prefix). - For a feature mapping rundown, see https://mautrix-chatto.iodev.org/. 

## Libraries

If your prefered language has no entry yet: **Chatto's APIs have reflection enabled (are self-describing).**  

- **Java:**
  - Freakynit's **chatto-java-sdk**: https://github.com/freakynit/chatto-java-sdk, *A Chatto API Library for Java that allows you to interact with a Chatto instance*, MIT
- **Python:**
  - Felix's **chattolib**: https://github.com/TheCodemancerLtd/chattolib, *Async Python client for the Chatto webchat GraphQL API*, MPL-2.0  
  NB: Felix' development closely follows Chatto's beta cycle.
- **Rust:**
  - Jacklak's **churro** crate: https://github.com/jacklak-redstone/churro, *A Rust crate to make Chatto bots*, Apache-2.0  
  While *churro* still is in its early days, there is a demonstrator bot on Chatto HQ already, churrobot. Jacklak is busy with a lot of other things, so this one may fall behind a bit. 
- **TypeScript:**
  - Axodouble's **chatto.ts**: https://github.com/axodouble/chatto.ts, *A Chatto API Library that allows you to interact with a Chatto instance*, MIT  
  Axodouble deployed a bot on Chatto HQ aptly named *chatto.ts* which uses this library, too.
  - ChattoCorp's own **@chatto/client**: https://www.npmjs.com/package/@chatto/client, *@chatto/client is the client for Chatto 0.5 servers.*, Apache-2.0  
  Newly made available in mid-October and still evolving, Hendrik (hmans) is dogfooding this one. Source is available in Chatto's monorepo.  

## Migration Hints

NB: *Some assembly required.*

For our purposes, a *migration* is an export (users, messages, attachments, reactions) from one or more source communications systems like Slack, Discord, Matrix, or MS Teams, followed by an import of that data to your Chatto server. 

As of late October 2026, ``chatto operator`` CLI eyes import functionality using an all-purpose intermediate format, pending format stabilisation. Matching export functionality will follow, likely with one of the next beta releases.  

On Chatto HQ, we also had people importing their chat history from ChatGPT<!-- , Claude, Slack, and Discord  -->.

- Exporting a **Discord** server:
  - Isotopp's **discord-exporter**: https://github.com/isotopp/discord-exporter, *Export the history of a discord server, using the bot API.*, Unlicense  
  Deploys a clever approach to get a full export without breaking the API.

## Further Reading and Listening

- Chatto's documentation:
  - stable: https://docs.chatto.run/
  - dev: https://dev-docs.chatto.run/
- About **Chatto 0.6**:
  - Release Checklist: https://github.com/chattocorp/chatto/issues/3589
  - Milestone Plan: https://github.com/chattocorp/chatto/milestone/5
- About **Chatto 0.5**:
  - Release Notes: https://github.com/chattocorp/chatto/releases/tag/v0.5.0
  - Release Checklist: https://github.com/chattocorp/chatto/issues/1926  *(will be removed from Awesome Chatto no earlier than 2026-11-16)*
  - Milestone Plan: https://github.com/chattocorp/chatto/milestone/4 *(will be removed from Awesome Chatto no earlier than 2026-11-16)*
- **Meta**:
  - [Article] Mans, Hendrik: "Chatto is Robots", personal blog, https://www.hmans.dev/blog/chatto-is-robots, 2026-07-16  
    Hendrik reflecting on his agentic development flow.
  - [Article] Mans, Hendrik: "AI Makes Better Software", personal blog, https://www.hmans.dev/blog/ai-makes-better-software, 2026-08-25  
    Hendrik muses on productivity, velocity, and attention in a world with AI powers.
  - [Podcast] Audiodump: "ad239 - Das ist wie Baby Kafka (mit Hendrik Mans)", podcast episode, https://audiodump.de/2026/10/22/ad239-das-ist-wie-baby-kafka-mit-hendrik-mans/, 2026-10-22  
    (In German.) This 4,5hrs long episode of *Audiodump* features Hendrik as a guest; it led to a nuanced, well-balanced discussion (not only) about Chatto, about AI, and about policy and politics around these. Well worth a listen, especially if you're interested about Hendrik, and Hendrik's intent and deliberations.  

---

The Community is grateful for anyone who participates and contributes. Thank you!

**Hall of Fame:**  
- *freakynit* for graciously building and hosting the best ``@helpbot``, ever. While helpbot is now retired, freakynit's experimenting is always leading the way.  

Ideas? Suggestions? Found a stale link? Join us at [Chatto HQ](https://chat.chatto.run) and discuss!

---

All trademarks mentioned are the property of their respective owners; their use does not constitute a claim of ownership or affiliation.  

This is a community effort not affiliated with ChattoCorp GmbH. Work licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
