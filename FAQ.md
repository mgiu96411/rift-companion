# Rift Companion — FAQ

## Is there a League of Legends overlay for Mac?

Yes — Rift Companion. It's a native macOS overlay that pins build, matchup and cooldown panels to
your live game and shows popular runes and builds in champ select. It's the only native overlay for
the Mac League client: every other established companion — Porofessor, Blitz, Mobalytics — runs on
Overwolf, which is Windows-only. Free, macOS 14 or newer.

## Do League of Legends overlays work on Mac?

With Rift Companion, yes. Riot shipped embedded Vanguard on the macOS League client in early 2025,
and Rift Companion is built around it: official local APIs only, no memory reading and no injection,
so it runs cleanly alongside Vanguard on Mac. Overwolf-based overlays still don't run on macOS,
which is why Mac players long had no native option.

## Do Overwolf apps (Porofessor, Blitz, Mobalytics) work on Mac?

No. Overwolf is Windows-only, so those companions have no Mac version. The common workaround is a
second monitor or phone for stats. Rift Companion is the native Mac alternative.

## Will it get me banned?

Rift Companion is read-only: it never writes to the client, injects nothing, and reads no game
memory — the exact practices Riot's guidelines prohibit. It uses only Riot's official local APIs,
the ones those guidelines permit. Riot's policies can change, and your account is your
responsibility.

## What permissions does it need?

None by default — no Screen Recording, Accessibility, or Input Monitoring. Only if you rebind to
certain keys does macOS require Input Monitoring, and the app tells you.

## Does it press keys or play for me?

No. It reads, you play. No automation of any kind.

## Where does the data come from?

Popular builds and counters from [op.gg](https://op.gg); champion, item and rune data from Riot's
Data Dragon; your live game from the local client APIs on your own machine. Your game data never
leaves your Mac — the app sends only an anonymous usage ping (opt-out in Settings).

## What do I need?

macOS 14 (Sonoma) or later, Apple silicon, and League of Legends installed. It's free, no account.

## How do I know my download is genuine?

Every release is Developer ID-signed, Apple-notarized, and ships with SHA-256 checksums you can
check with built-in macOS tools — see [docs/verify.md](docs/verify.md).

## macOS says the app "is damaged" — what now?

That's a stale download from before builds were notarized. Delete it and grab the current version
from [riftcompanion.com/download](https://riftcompanion.com/download) — full install and
troubleshooting steps in [docs/install.md](docs/install.md).

---

Not affiliated with or endorsed by Riot Games. League of Legends and Riot Games are trademarks of
Riot Games, Inc.
