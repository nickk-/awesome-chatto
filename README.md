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

## Deployment 

- **Proxmox Virtual Environment/LXC:**
    - MickLesk's Community Script: https://community-scripts.org/scripts/chatto, MIT.  
	*(Testers wanted.)*
- **Installation helpers:**
    - poga's **Emergency Box** for Civil Protection scenarios: https://github.com/poga/emergency-box, *A chat room that lives on your wifi and keeps working when the Internet dies*, AGPL-3.0  
	  "It's a 1 shot script for setting up a Chatto Server on a MacBook which allows anyone on the same LAN to join. Includes some built-in bots for fetching news if there's still intermittent internet connection."
	
## Frontend

- **App Wrappers:**
  These applications are native wrappers around Chatto's web frontend. This results in a standalone experience that includes native OS notifications, and badges. 
  - Kaihanga's **Solander**, a Tauri shell: https://github.com/jrimmer/solander-desktop, *Chatto desktop client*, Apache-2.0
  - Teal's Tauri shell: https://github.com/teal-bauer/chatto-tauri, AGPL-3.0+  
  The earliest known shell, a proof-of-concept at this point.

- **Browser extensions:**
  These enrich Chatto's standard web client experience. 
  - Loading's Chromium extension: https://github.com/SeanGSR/chatto-enhancer, *Chatto Enhancer*, MIT  
  Aimed at Chatto 0.4. The extension provides enhancements for voice chat UI and chat bar (namely: Emoji picker, Giphy integration, and Markdown controls).
        
- **Client demonstrators:** These are alternative Chatto client implementations, usually focussing on text (chat) experience.
  - Felix's Python/Tk and Tcl/Tk clients: https://github.com/TheCodemancerLtd/chatto-native, MIT

## Bots

NB: There will be a dedicated Bot API surface coming up with Chatto 0.5+.

- **Python:**
  - Felix's **robochatto**: https://github.com/TheCodemancerLtd/robochatto, *A bot demonstrator based on chattolib*, MIT

## Bridges

A *bridge* is a special kind of bot that allows for Rooms being connected to at least one other Room (or "channel") on another Server or even service. Content is shared between the connected Rooms/channels, so data and trust boundaries become fuzzy. Before deploying, ensure consent of admins/owners and Communities involved. 

- **Chatto -- Discord:**
  - Felix's **chatto-bridge**: https://github.com/TheCodemancerLtd/chatto-bridge, *Discord ↔ Chatto bridge bot (discord.py + chattolib + NATS)*, MPL-2.0  
  Felix says this is in its very early days as of early August 2026.
  
## Libraries

- **Java:**
  - Freakynit's **chatto-java-sdk**: https://github.com/freakynit/chatto-java-sdk, *A Chatto API Library for Java that allows you to interact with a Chatto instance*, MIT
- **Python:**
  - Felix's **chattolib**: https://github.com/TheCodemancerLtd/chattolib, *Async Python client for the Chatto webchat GraphQL API*, MPL-2.0
- **Rust:**
  - Jacklak spearheaded a Rust effort at one point.
- **TypeScript:**
  - Axodouble's **chatto.ts**: https://github.com/axodouble/chatto.ts, *A Chatto API Library that allows you to interact with a Chatto instance*, MIT  
  Axodouble deployed a bot on Chatto HQ aptly named *chatto.ts* which uses this library, too. 

---

The Community is grateful for anyone who participates and contributes. Thank you!

Ideas? Suggestions? Found a stale link? Join us at [Chatto HQ](https://chat.chatto.run) and discuss!

---

This is a community effort not affiliated with ChattoCorp GmbH. Work licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). 
