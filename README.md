# Awesome Chatto

This is an *Awesome Chatto* list curated for the Chatto Community by nickk @ [Chatto HQ](https://chat.chatto.run) Server.

Chatto is a *A fully-featured team and group chat application that you can easily selfhost*. It is free to use, lightweight, easy to spin up and manage, and respects your privacy. Its international community is very friendly.

---

![Awesome](https://awesome.re/badge-flat2.svg)

NB: Chatto currently is pre-1.0 software. Consequently, some breakage *will* occur. Most authors are on Chatto HQ, so stop by and share your experiences.

## Table of Contents

* [Deployment](#deployment)
* [Frontend](#frontend)
* [Bots](#bots)
* [Bridges](#bridges)
* [Libraries](#libraries)
* [Further Reading](#further-reading)

## Deployment 

### Proxmox Virtual Environment/LXC
- MickLesk's Community Script: https://community-scripts.org/scripts/chatto, MIT.  
  *(Testers wanted.)*

### Installation and operations helpers

- poga's **Emergency Box** for Civil Protection scenarios: https://github.com/poga/emergency-box, *A chat room that lives on your wifi and keeps working when the Internet dies*, AGPL-3.0  
  "It's a 1 shot script for setting up a Chatto Server on a MacBook which allows anyone on the same LAN to join. Includes some built-in bots for fetching news if there's still intermittent internet connection."
- SeanGSR's **chatto-admin** as alternative to Chatto's *Operator CLI*: https://github.com/SeanGSR/chatto-admin, *A community made Admin Panel for Chatto*, MIT  
  Chatto 0.4 has made a deliberate security/AX choice of having certain administration functionality exposed only at its *Operator CLI* for the time being. If you need or want to have a web interface nevertheless - including all the potential drawbacks that might bring - this project is for you. Make sure you and your agent read its SECURITY.md before deploying. 
	
## Frontend

### App Wrappers
These applications are native wrappers around Chatto's web frontend. This results in a standalone experience that includes native OS notifications, and badges.  
  
NB: The natural drawback of this approach is that you are being tied to the wrapper's release cycle, which might not match your Server's upgrade policy. In other words: If the version difference between App Wrapper and Server becomes too large, expect some (feature) breakage.  
  
NB: 0.4 PWA and consequently App Wrappers make no good job at showing that there are always two version numbers involved: One for the frontend (shown) and one for the Server(s) it connects to (not shown). 0.5+ will be better at that.  

There *will* be official ChattoCorp apps at one point.  
  
- Kaihanga's **Solander**, a Tauri shell: https://github.com/jrimmer/solander-desktop, *Chatto desktop client*, Apache-2.0  
  As of 2026-08-09, this was tested with Chatto Server 0.4.8 only - but likely works with later 0.4 releases. It just shows 0.4.8 on its User Interface because that was the PWA's version that got "app wrapped".  
- Teal's Tauri shell: https://github.com/teal-bauer/chatto-tauri, AGPL-3.0+  
  The earliest known shell, a proof-of-concept at this point.

### Browser extensions
These enrich Chatto's standard web client experience. 
- SeanGSR's Chromium extension: https://github.com/SeanGSR/chatto-enhancer, *Chatto Enhancer*, MIT  
  Aimed at Chatto 0.4. The extension provides enhancements for voice/video chat UI and chat bar (namely: Emoji picker, Giphy integration, local nicknames, enhanced theming, and Markdown controls).
        
### Client demonstrators
These are alternative Chatto client implementations, usually focussing on text (chat) experience.
  - Teal's **chatto-cli**: https://github.com/teal-bauer/chatto-cli, *Command-line client for Chatto (chatto.run)*, AGPL-3.0  
    Probably the very first alternative client for Chatto. Text mode, implemented in Go. Less of a classic client UI, more of a command-line interface to participating on a Server. 
  - Felix's **chatto-native**, i.e. Python/Tk and Tcl/Tk clients: https://github.com/TheCodemancerLtd/chatto-native, MIT

## Bots

NB: Improved bot support coming up with Chatto 0.5+ - e.g. dedicated bot accounts, and clearly scoped capabilities.

### Python
- Teal's **chatto-bot**: https://github.com/teal-bauer/chatto-bot, *Python bot framework for Chatto — decorator-based commands, cog system, WebSocket subscriptions*, AGPL-3.0  
  This is probably the first ever bot for Chatto.
- Felix's **robochatto**: https://github.com/TheCodemancerLtd/robochatto, *A bot demonstrator based on chattolib*, MIT

## Bridges

A *bridge* is a special kind of bot that allows for Rooms being connected to at least one other Room (or "channel") on another Server or even service. Content is shared between the connected Rooms/channels, so governance, data, and trust boundaries become fuzzy. Before deploying, ensure consent of admins/owners and Communities involved. 

### Chatto -- Discord
  - Felix's **chatto-bridge**: https://github.com/TheCodemancerLtd/chatto-bridge, *Discord ↔ Chatto bridge bot (discord.py + chattolib + NATS)*, MPL-2.0  
  Felix says this is in its very early days as of early August 2026.
  
## Libraries

- **Java:**
  - Freakynit's **chatto-java-sdk**: https://github.com/freakynit/chatto-java-sdk, *A Chatto API Library for Java that allows you to interact with a Chatto instance*, MIT
- **Python:**
  - Felix's **chattolib**: https://github.com/TheCodemancerLtd/chattolib, *Async Python client for the Chatto webchat GraphQL API*, MPL-2.0
- **Rust:**
  - Jacklak's **churro** crate: https://github.com/jacklak-redstone/churro, *A Rust crate to make Chatto bots*, Apache-2.0  
  While *churro* still is in its early days, there is a demonstrator bot on Chatto HQ already, churrobot.
- **TypeScript:**
  - Axodouble's **chatto.ts**: https://github.com/axodouble/chatto.ts, *A Chatto API Library that allows you to interact with a Chatto instance*, MIT  
  Axodouble deployed a bot on Chatto HQ aptly named *chatto.ts* which uses this library, too. 

## Further Reading

- About **Chatto 0.5**:
  - Release Checklist: https://github.com/chattocorp/chatto/issues/1926
  - Milestone Plan: https://github.com/chattocorp/chatto/milestone/4
- **Meta**:
  - Mans, Hendrik: "Chatto is Robots", personal blog, https://www.hmans.dev/blog/chatto-is-robots, 2026-07-16  
    Hendrik reflecting on his agentic development flow.

---

The Community is grateful for anyone who participates and contributes. Thank you!

Ideas? Suggestions? Found a stale link? Join us at [Chatto HQ](https://chat.chatto.run) and discuss!

---

This is a community effort not affiliated with ChattoCorp GmbH. Work licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). 
