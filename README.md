# Awesome Chatto

This is an *Awesome Chatto* list curated for the Chatto Community by nickk @ [Chatto HQ](https://chat.chatto.run) Server.

Chatto is a *A fully-featured team and group chat application that you can easily selfhost*. It is free to use, lightweight, easy to spin up and manage, and respects your privacy. Its international community is very friendly.

---

![Awesome](https://awesome.re/badge-flat2.svg)

NB: Chatto currently is pre-1.0 software. Consequently, some breakage *will* occur. Most authors are on Chatto HQ, so stop by and share your experiences.  

Also, please note that Chatto HQ migrated to 0.5 beta releases in Mid-September. Many entries on here assume 0.4 servers, others already provide 0.5 beta compatibility.

At the time of writing this, we're closing in on 0.5 release candidates. **If you're new to Chatto and pondering self-hosting, jump on the 0.5 release candidates (RC).** 0.4 very clearly feels dated at this point.  
If you do install via Docker, just make sure you switch from *chatto:next* to *chatto:latest* as soon as 0.5 release lands. 

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
  This closely follows Chatto's (beta/RC) release cycle. *Testers wanted.*

### AWS Lightsail 
- jessedc's **chatto-on-lightsail**: https://github.com/jessedc/chatto-on-lightsail, MIT  
  Lightsail is AWS's Virtual Private Server (VPS) offering. This repository guides you through installing Chatto 0.4 on Lightsail.

### Nix
- abl's **nix-chatto**: https://github.com/abl/nix-chatto, *Nix flake for the Chatto release binary*, MIT  
  Nix is a package manager, and NixOS is a Linux distribution based on Nix. It allows for reproducible builds and deployments, think "OS as code" - a declarative system configuration. A *Flake* can be imagined as part of a pipeline that builds these declarations, so nix-chatto is a quasi-installer for Chatto on NixOS.  
  NB: Deliberately on Chatto's 0.4 cycle.

### Installation and operations helpers

- lizard77's **chatto-ttrpg-patches**: https://github.com/lizzard77/chatto-ttrpg-patches, (license pending)  
  A collection of patches for Chatto's upstream source that provide an improved tabletop / pen & paper role-playing game experience. Example functionality added: Dice support, and an image annotation functionality (i.e. for shared world maps and the like).
- poga's **Emergency Box** for Civil Protection scenarios: https://github.com/poga/emergency-box, *A chat room that lives on your wifi and keeps working when the Internet dies*, AGPL-3.0  
  "It's a 1 shot script for setting up a Chatto Server on a MacBook which allows anyone on the same LAN to join. Includes some built-in bots for fetching news if there's still intermittent internet connection."
- SeanGSR's **chatto-admin** as alternative to Chatto's *Operator CLI*: https://github.com/SeanGSR/chatto-admin, *A community made Admin Panel for Chatto*, MIT  
  Chatto 0.4 has made a deliberate security/AX choice of having certain administration functionality exposed only at its *Operator CLI* for the time being. If you need or want to have a web interface nevertheless - including all the potential drawbacks that might bring - this project is for you. Make sure you and your agent read its SECURITY.md before deploying. 
	
## Frontend

### App Wrappers
These applications are native wrappers around Chatto's web frontend. This results in a standalone experience that includes native OS notifications, and badges.  
  
NB: The natural drawback of this approach is that you are being tied to the wrapper's release cycle, which might not match your Server's upgrade policy. In other words: If the version difference between App Wrapper and Server becomes too large, expect some (feature) breakage.  

There will be official ChattoCorp desktop apps (Linux, macOS, Windows) released alongside 0.5, but the PWA remains an excellent choice. 
  
- Kaihanga's **Solander**, a Tauri shell: https://github.com/jrimmer/solander-desktop, *Chatto desktop client*, Apache-2.0  
  As of 2026-08-09, this was tested with Chatto Server 0.4.8 only - but likely works with later 0.4 releases. It just shows 0.4.8 on its User Interface because that was the PWA's version that got "app wrapped".  
- Teal's Tauri shell: https://github.com/teal-bauer/chatto-tauri, AGPL-3.0+  
  The very first community-made shell, follows Chatto's (beta/RC) release cycle. 

### Browser extensions
These enrich Chatto's standard web client experience. 
- SeanGSR's Chromium extension: https://github.com/SeanGSR/chatto-enhancer, *Chatto Enhancer*, MIT  
  Currently aimed at Chatto 0.4. The extension provides enhancements for voice/video chat UI and chat bar (namely: Emoji picker, Giphy integration, local nicknames, enhanced theming, and Markdown controls).  
  NB: It's likely that SeanGSR will update the extension as soon as the feature set for Chatto 0.5 stabilises.  
        
### Client demonstrators
These are alternative Chatto client implementations, usually focussing on text (chat) experience.
  - Teal's **chatto-cli**: https://github.com/teal-bauer/chatto-cli, *Command-line client for Chatto (chatto.run)*, AGPL-3.0  
    Probably the very first alternative client for Chatto. Text mode, implemented in Go. Less of a classic client UI, more of a command-line interface to participating on a Server. Follows Chatto's 0.5 (beta) cycle. 
  - Felix's **chatto-native**, i.e. Python/Tk and Tcl/Tk clients: https://github.com/TheCodemancerLtd/chatto-native, MIT  
    [Chatto 0.4] Initially a Proof of Concept that even older stacks are able to connect to Chatto.  

## Bots

NB: Bot support is vastly improved in 0.5 beta/RC, including an optional MCP server for agents. I'd encourage you to start with Chatto 0.5 if you plan on deploying more than just simple bots. Most projects listed here already need 0.5.

### Python
- Teal's **chatto-bot**: https://github.com/teal-bauer/chatto-bot, *Python bot framework for Chatto — decorator-based commands, cog system, WebSocket subscriptions*, AGPL-3.0  
  This is probably the first ever bot for Chatto.
- Felix's **robochatto**: https://github.com/TheCodemancerLtd/robochatto, *A bot demonstrator based on chattolib*, MIT  

### Rust
- TimesZ's **Chatto Tidal Bot**: https://github.com/Times-Z/tidal-bot-chatto, *A music bot for Chatto that plays Tidal HiFi streams in voice channels via LiveKit*, GPL-3.0  
  NB: This was the very first 0.5+ entry we had on *Awesome Chatto!*

## Agents

  - Kaihanga's **Hermes Chatto Plugin**: https://github.com/jrimmer/hermes-chatto-plugin/, *Chatto platform adapter plugin for Hermes Agent — WebSocket realtime, ConnectRPC API, thread support, dynamic room discovery*, MIT
  - PaulK's **Hermes Chatto Plugin**: https://gogs.netdome.biz/paul/hermes-chatto-plugin/, *Full-featured Hermes Chatto Plugin. So you can use Chatto to talk to your Hermes Agent*, MIT  
  This first started out as a fork of Kaihanga's work, and vendored in Felix' *chattolib*. 
  - ncmro's **channels** for Pi: https://github.com/ai-outfitter/channels, *Pi extension: push channel events (email/Slack/Signal/GitHub) into an agent session; wake only on real work.*, MIT  
  This Pi extension watches notifications/mentions on different inbound channels (e.g. Chatto) and runs a durable Pi session on a match.

## Bridges

A *bridge* is a special kind of bot that allows for Rooms being connected to at least one other Room (or "channel") on another Server or even service. Content is shared between the connected Rooms/channels, so governance, data, and trust boundaries become fuzzy. Before deploying, ensure consent of admins/owners and Communities involved. 

### Chatto -- Discord
  - Felix's **chatto-bridge**: https://github.com/TheCodemancerLtd/chatto-bridge, *Discord ↔ Chatto bridge bot (discord.py + chattolib + NATS)*, MPL-2.0  
  Felix says this is in its early days, but it might help communities help to migrate.
  
## Libraries

NB: Most projects listed here already switched to 0.5 compatibility.

If your prefered language has no entry yet: **Chatto's APIs have reflection enabled (are self-describing).**  

- **Java:**
  - Freakynit's **chatto-java-sdk**: https://github.com/freakynit/chatto-java-sdk, *A Chatto API Library for Java that allows you to interact with a Chatto instance*, MIT
- **Python:**
  - Felix's **chattolib**: https://github.com/TheCodemancerLtd/chattolib, *Async Python client for the Chatto webchat GraphQL API*, MPL-2.0  
  NB: Felix' development closely follows Chatto's beta cycle.
- **Rust:**
  - Jacklak's **churro** crate: https://github.com/jacklak-redstone/churro, *A Rust crate to make Chatto bots*, Apache-2.0  
  While *churro* still is in its early days, there is a demonstrator bot on Chatto HQ already, churrobot.
- **TypeScript:**
  - Axodouble's **chatto.ts**: https://github.com/axodouble/chatto.ts, *A Chatto API Library that allows you to interact with a Chatto instance*, MIT  
  Axodouble deployed a bot on Chatto HQ aptly named *chatto.ts* which uses this library, too.
  - ChattoCorp's own **@chatto/client**: https://www.npmjs.com/package/@chatto/client, *@chatto/client is the client for Chatto 0.5 servers.*, Apache-2.0  
  Newly made available in mid-October and still evolving, Hendrik (hmans) is dogfooding this one. Source is available in Chatto's monorepo.  

## Migration Hints

NB: *Some assembly required.*

For our purposes, a *migration* is an export (users, messages, attachments, reactions) from one or more source communications systems like Slack, Discord, Matrix, or MS Teams, followed by an import of that data to Chatto. 

As of late October 2026, ``chatto operator`` CLI eyes import functionality using an all-purpose intermediate format, pending format stabilisation. Matching export functionality will follow, likely with one of the next beta releases.  

On Chatto HQ, we also had people importing their chat history from ChatGPT<!-- , Claude, Slack, and Discord  -->.

- Exporting a **Discord** server:
  - Isotopp's **discord-exporter**: https://github.com/isotopp/discord-exporter, *Export the history of a discord server, using the bot API.*, Unlicense  
  Deploys a clever approach to get a full export without breaking the API.

## Further Reading and Listening

- About **Chatto 0.5**:
  - Release Checklist: https://github.com/chattocorp/chatto/issues/1926
  - Milestone Plan: https://github.com/chattocorp/chatto/milestone/4
- About **Chatto 0.6**: 
  - Milestone Plan: https://github.com/chattocorp/chatto/milestone/5
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
