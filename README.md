# Awesome Chatto

This is an *Awesome Chatto* list curated for the Chatto Community by nickk @ [Chatto HQ](https://chat.chatto.run).

Chatto is a *A fully-featured team and group chat application that you can easily selfhost*. It is free to use, lightweight, easy to spin up and manage, and respects your privacy. Its international community is very friendly.

---

![Awesome](https://awesome.re/badge-flat2.svg)

NB: Chatto is currently pre-1.0 software. Some breakage is to be expected. Most authors are on Chatto HQ, so stop by and share your experiences.

## Deployment 

- **Proxmox Virtual Environment/LXC:**
    - MickLesk's Community Script: https://community-scripts.org/scripts/chatto, MIT. *(Testers wanted.)*
- **Installation helpers:**
    - poga's **Emergency Box** for Civil Protection scenarios: https://github.com/poga/emergency-box, *A chat room that lives on your wifi and keeps working when the Internet dies*, AGPL-3.0  
	  "It's a 1 shot script for setting up a Chatto Server on a MacBook which allows anyone on the same LAN to join. Includes some built-in bots for fetching news if there's still intermittent internet connection."
	
## Community frontend work

- **App Wrappers:**
  These applications are native wrappers around Chatto's web frontend. This results in a standalone experience that includes native OS notifications, and badges. 
  - Kaihanga's **Solander**, a Tauri shell: https://github.com/jrimmer/solander-desktop, *Chatto desktop client*, Apache-2.0
  - Teal's Tauri shell: https://github.com/teal-bauer/chatto-tauri, AGPL-3.0+
  The earliest known shell, a proof-of-concept at this point.

- **Browser extensions:**
  These enrich Chatto's standard web client experience. 
  - Loading's Chromium extension: https://chat.chatto.run/chat/-/RTKVVgllAweTw3h/m/Ed7xXBVTYttxQ9W, *Chatto Enhancer*, t.b.d. 
  Aimed at Chatto 0.4, it provides enhanced voice chat UI, chat bar, and Markdown controls.
        
- **Client demonstrators:**
  - Felix's Python/Tk and Tcl/Tk clients: https://github.com/TheCodemancerLtd/chatto-native, t.b.d.

## Bots

NB: There will be a dedicated Bot API surface coming up with Chatto 0.5+.

- **Python:**
  - Felix's **robochatto**: https://github.com/TheCodemancerLtd/robochatto, *A bot demonstrator based on chattolib*, t.b.d.

## Community Libraries

- **Python:**
  - Felix's **chattolib**: https://github.com/TheCodemancerLtd/chattolib, *Async Python client for the Chatto webchat GraphQL API*, MPL-2.0
- **TypeScript:**
  - Axodouble's **chatto.ts**: https://github.com/axodouble/chatto.ts, *A Chatto API Library that allows you to interact with a Chatto instance. Pull requests welcome!*, MIT

---

This is a community effort not affiliated with ChattoCorp GmbH. Work licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). 

The Community is grateful for anyone who participates and contributes. Thank you!

Ideas? Suggestions? Come on over to [Chatto HQ](https://chat.chatto.run) and discuss!