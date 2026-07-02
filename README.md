# Rift Companion — League of Legends overlay for Mac

[![Latest release](https://img.shields.io/github/v/release/mgiu96411/rift-companion?label=latest&color=6f2ccf)](https://github.com/mgiu96411/rift-companion/releases/latest)
![Platform](https://img.shields.io/badge/platform-macOS%2014%2B%20·%20Apple%20silicon-111)
![Price](https://img.shields.io/badge/price-free-2a9d5c)

The native macOS overlay for League of Legends. Popular runes and builds the moment you lock your
champion, matchup/counter-build and gold-lead panels pinned to your live game, and click-to-mark
enemy summoner-spell cooldowns. The only native overlay built for the Mac League client — every
other established companion (Porofessor, Blitz, Mobalytics) runs on Overwolf and is Windows-only.

**[⬇ Download for Mac](https://riftcompanion.com/download)** · macOS 14+ · Apple silicon · free ·
no account

> Rift Companion is a free, **closed-source** app. This repository is its official public home for
> downloads ([Releases](../../releases)), documentation, changelog, and support — the product site
> is [riftcompanion.com](https://riftcompanion.com/).

![Champ select: popular runes and build](screenshots/champ-select.png)

## Why it exists

Mac players had no native League overlay. Overwolf — what Porofessor, Blitz and Mobalytics are
built on — doesn't run on macOS. Rift Companion fills that gap natively.

## Rift Companion vs the Windows-only companions, on Mac

| | Rift Companion | Porofessor / Blitz / Mobalytics |
|---|:---:|:---:|
| Runs natively on macOS (Apple silicon) | ✅ | ❌ (Overwolf is Windows-only) |
| In-game overlay on Mac | ✅ | ❌ |
| Champ-select runes & builds | ✅ | ✅ (Windows) |
| Enemy summoner-spell timers | ✅ (click to mark) | ✅ (Windows) |
| macOS permissions required | None by default | n/a |
| Price | Free | Freemium |

## What it does

- **Champ select** — popular runes and the current-patch build the moment you lock your champion.
- **In game** — build and matchup/counter-build panels pinned beside the League window.
- **Cooldowns** — click an enemy summoner spell when it's used; the panel counts it back up,
  item- and level-aware. Manual marking, no automation.
- **Gold** — hold Tab for your lane gold lead and per-champion totals; release and it's gone.
- Panels show on your terms (hold Tab, tap the shop key, or always-on) and are repositionable,
  with positions saved per game mode — Summoner's Rift, ARAM and Arena.

![In-game build and matchup panels](screenshots/overlay-builds.png)
![Enemy summoner-spell cooldown timers](screenshots/cooldowns.png)
![Gold lead on Tab](screenshots/gold.png)

## Install

1. Download the `.dmg` from [riftcompanion.com/download](https://riftcompanion.com/download) or
   the [latest GitHub Release](../../releases/latest).
2. Open it and drag **Rift Companion** into **Applications**.
3. Launch it — the app lives in your menu bar. Start League and it does the rest.

The app is Developer ID-signed and Apple-notarized, so macOS opens it without warnings. From
version 1.3 it updates itself in-app. Full steps and fixes: **[docs/install.md](docs/install.md)**.

## Verify your download

Every release ships with a `SHA256SUMS-<version>.txt` you can check the `.dmg`/`.zip` against,
and the app's code signature and notarization are verifiable with built-in macOS tools. How-to:
**[docs/verify.md](docs/verify.md)**.

## Built to stay clean

- **Read-only.** Never writes to the client, injects nothing, reads no game memory.
- **Official local APIs only** — the same ones Riot's guidelines permit.
- **Zero macOS permissions** by default — no Screen Recording, Accessibility, or Input Monitoring.
- Runs alongside the embedded Vanguard anti-cheat on macOS.

Riot's policies can change, and your account is your responsibility.

## Privacy

Your game data never leaves your Mac. The app sends only an anonymous usage ping, which you can
turn off in Settings. Full policy: [riftcompanion.com/privacy](https://riftcompanion.com/privacy).

## Requirements

macOS 14 (Sonoma) or later · Apple silicon · League of Legends installed · free, no account.

## Docs

- [FAQ](FAQ.md) — including *"Is there a League of Legends overlay for Mac?"* and
  *"Will it get me banned?"*
- [Install & troubleshooting](docs/install.md)
- [Verify a download](docs/verify.md)
- [Product facts](docs/facts.md) — canonical one-page summary
- [Use cases](docs/use-cases.md) — what players actually use it for
- [Changelog](CHANGELOG.md) · full history at
  [riftcompanion.com/changelog](https://riftcompanion.com/changelog)

## Support & feedback

Bugs and feature requests welcome in [Issues](../../issues), questions in
[Discussions](../../discussions) — see [SUPPORT.md](SUPPORT.md) for all channels.

## License

Rift Companion is proprietary software, free to download and use — see [LICENSE.md](LICENSE.md).
It is **not** open source; no source code is published in this repository.

## Credits

Build and counter data from [op.gg](https://op.gg). Champion, item and rune data from Riot's
Data Dragon. In-app updates delivered by the open-source
[Sparkle](https://sparkle-project.org) framework.

Not affiliated with or endorsed by Riot Games. League of Legends and Riot Games are trademarks of
Riot Games, Inc.
