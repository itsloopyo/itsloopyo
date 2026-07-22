# Hi, I'm Loop 👋

I'm on a mission to make head tracking happen.

---

## What I'm building

### Apps

- **Headcam iOS** - iPhone head tracking ([get it on the App Store](https://apps.apple.com/us/app/headcam/id6759300260))
- **Headcam Android** - Android head tracking ([join the testers group](https://groups.google.com/g/headcam-testers) for early access)
- **[Lopari](https://lopari.app)** - universal launcher for games with native *or* mod-available head tracking, runs them with head tracking enabled in one click.

### Tech & libraries

- **QuickFeed** - ultra low-latency, zero drift phone-to-OBS video streaming library.
- **QuickFeed OBS Plugin** - OBS receiver.
- **[cameraunlock-core](https://github.com/itsloopyo/cameraunlock-core)** - shared, multi-engine head-tracking core for mods.
- **[arucogen](https://github.com/itsloopyo/arucogen)** - generates ArUco/ChArUco tags and boards used to capture ground-truth head pose when gathering training data for our model (an opentrack neuralnet tracker, used in the Android app).
- **headshot** - the full head tracking model pipeline: drives Blender headlessly to generate synthetic head-pose visuals and data, trains the model on it, and owns the model I/O contract (preprocessing and label encoding) that keeps everything in lockstep with opentrack's neuralnet tracker.

### Tooling

- **head-tracking-tester** - containerised app for testing and debugging head trackers.
- **[qrdrop](https://github.com/itsloopyo/qrdrop)** - quickly share files and folders bidirectionally over the LAN via HTTP. `uvx qrdrop` brings it up with no traditional install and shows a code you scan with your phone to start transferring. Built it to streamline copying training data back and forth between devices.
- **[Lab](https://lab.decoupled.cam)** - the agentic development environment I made for managing all this stuff. ([video](https://www.youtube.com/watch?v=8Z1JwJWF_A0))

### Released mods

| Game | Links | Latest release |
|---|---|---|
| Black and White | [GitHub](https://github.com/itsloopyo/black-and-white-headtracking) · [Nexus](https://www.nexusmods.com/games/blackandwhite/mods/26) | v0.1.2 (2026-06-07) |
| BioShock Remastered | [GitHub](https://github.com/itsloopyo/bioshock-remastered-headtracking) · [Nexus](https://www.nexusmods.com/bioshock/mods/144) | v0.3.5 (2026-06-07) |
| Dying Light 2 | [GitHub](https://github.com/itsloopyo/dying-light-2-headtracking) · [Nexus](https://www.nexusmods.com/dyinglight2/mods/1900) | v1.2.4 (2026-06-07) |
| Easy Delivery Co | [GitHub](https://github.com/itsloopyo/easy-delivery-co-headtracking) · [Nexus](https://www.nexusmods.com/easydeliveryco/mods/18) | v0.1.1 (2026-06-07) |
| Eternal Afternoon | [GitHub](https://github.com/itsloopyo/eternal-afternoon-headtracking) | v0.1.4 (2026-06-07) |
| Firewatch | [GitHub](https://github.com/itsloopyo/firewatch-headtracking) | v0.1.1 (2026-06-07) |
| Gone Home | [GitHub](https://github.com/itsloopyo/gone-home-headtracking) | v1.3.2 (2026-06-08) |
| Green Hell | [GitHub](https://github.com/itsloopyo/green-hell-headtracking) · [Nexus](https://www.nexusmods.com/greenhell/mods/83) | v1.1.3 (2026-06-07) |
| Outer Wilds | [GitHub](https://github.com/itsloopyo/outer-wilds-headtracking) | v1.1.0 (2026-04-29) |
| PEAK | [GitHub](https://github.com/itsloopyo/peak-headtracking) · [Nexus](https://www.nexusmods.com/peak/mods/167) | v1.1.2 (2026-06-07) |
| Resident Evil Requiem | [GitHub](https://github.com/itsloopyo/resident-evil-requiem-headtracking) · [Nexus](https://www.nexusmods.com/residentevilrequiem/mods/1678) | v0.2.2 (2026-06-07) |
| Return of the Obra Dinn | [GitHub](https://github.com/itsloopyo/obra-dinn-headtracking) · [Nexus](https://www.nexusmods.com/returnoftheobradinn/mods/9) | v1.1.3 (2026-06-07) |
| RV There Yet | [GitHub](https://github.com/itsloopyo/rv-there-yet-headtracking) | v0.1.0 (2026-07-10) |
| Skyrim Special Edition | [GitHub](https://github.com/itsloopyo/skyrim-special-edition-headtracking) · [Nexus](https://www.nexusmods.com/skyrimspecialedition/mods/180328) | v0.1.1 (2026-06-08) |
| Subnautica | [GitHub](https://github.com/itsloopyo/subnautica-headtracking) · [Nexus](https://www.nexusmods.com/subnautica/mods/3169) | v1.2.0 (2026-06-22) |
| Subnautica 2 | [GitHub](https://github.com/itsloopyo/subnautica-2-headtracking) · [Nexus](https://www.nexusmods.com/subnautica2/mods/250) | v0.4.1 (2026-07-15) |
| Valheim | [GitHub](https://github.com/itsloopyo/valheim-headtracking) · [Nexus](https://www.nexusmods.com/valheim/mods/3356) | v0.1.5 (2026-06-07) |

New mods are released regularly.

### Pre-release mods

| Game | Links | Latest release |
|---|---|---|
| Abzu | [GitHub](https://github.com/itsloopyo/abzu-headtracking) | v0.0.0 (2026-06-07) |
| Assassin's Creed Unity | [GitHub](https://github.com/itsloopyo/assassins-creed-unity-headtracking) | v0.0.0 (2026-06-07) |
| Cyberpunk 2077 | [GitHub](https://github.com/itsloopyo/cyberpunk-2077-headtracking) | v0.0.0 (2026-06-07) |
| Fallout: New Vegas | [GitHub](https://github.com/itsloopyo/fallout-new-vegas-headtracking) | v0.0.0 (2026-06-07) |
| Metaphor: ReFantazio | [GitHub](https://github.com/itsloopyo/metaphor-refantazio-headtracking) | v0.0.0 (2026-06-27) |
| Mirror's Edge | [GitHub](https://github.com/itsloopyo/mirrors-edge-headtracking) | v0.0.0 (2026-07-05) |
| Resident Evil 2 | [GitHub](https://github.com/itsloopyo/resident-evil-2-headtracking) | v0.0.0 (2026-06-07) |
| Resident Evil 3 | [GitHub](https://github.com/itsloopyo/resident-evil-3-headtracking) | v0.0.0 (2026-06-08) |
| Resident Evil 4 | [GitHub](https://github.com/itsloopyo/resident-evil-4-headtracking) | v0.0.0 (2026-06-08) |
| Resident Evil 7 | [GitHub](https://github.com/itsloopyo/resident-evil-7-headtracking) | v0.0.0 (2026-06-08) |
| Resident Evil Village | [GitHub](https://github.com/itsloopyo/resident-evil-village-headtracking) | v0.0.0 (2026-06-08) |
| Sons of the Forest | [GitHub](https://github.com/itsloopyo/sons-of-the-forest-headtracking) | v0.0.0 (2026-06-07) |
| The Painscreek Killings | [GitHub](https://github.com/itsloopyo/the-painscreek-killings-headtracking) | v0.0.0 (2026-06-08) |
| Wobbly Life | [GitHub](https://github.com/itsloopyo/wobbly-life-headtracking) | v0.0.0 (2026-06-07) |
| Yakuza 0 | [GitHub](https://github.com/itsloopyo/yakuza-0-headtracking) | v0.0.0 (2026-06-07) |
| YAPYAP | [GitHub](https://github.com/itsloopyo/yapyap-headtracking) | v0.0.0 (2026-06-07) |

Pre-release mods may have bugs or missing functionality, but are in a playable state. The latest dev build is available for download on each mod's release page.

---

## Support

Want to help?

All mods are open source, and dev builds are freely available from each GitHub repo.

[Patreon](https://www.patreon.com/itsloopyo) backers help fund future development and bug fixes, and get one-click install of pre-release mods via [Lopari](https://lopari.app), access to Lab and any other tooling I develop, along with insider info about upcoming mods.

---

## Discord

Want to follow along, test stuff, suggest games, or report bugs?

Join the [Discord](https://discord.gg/dxyZdyFNT9).
