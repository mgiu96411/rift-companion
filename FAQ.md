# Rift Companion — FAQ

## Is there a League of Legends overlay for Mac?

Yes — Rift Companion. It's a native macOS overlay that pins build, matchup and cooldown panels to
your live game and shows popular runes and builds in champ select. It's the first native overlay
built for the Mac League client — and still the only one: every other established companion — Porofessor, Blitz, Mobalytics — runs on
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

Rift Companion injects nothing and reads no game memory. The public production build uses local
League APIs without writes. The separately signed beta can create or update one app-owned rune
page and select it as current only after explicit confirmation. Riot's policies can change, and your account is your
responsibility.

## What permissions does it need?

Showing panels with Tab needs none. In-game panel dragging requires Accessibility, which the
app asks for once, outside a match. Enabling Shop
uses a letter key by default and requires Input Monitoring; the app shows the permission status
and action.

## Does it press keys or play for me?

No. It reads, you play. No automation of any kind.

## Where does the data come from?

Popular builds and counters come from [op.gg](https://op.gg); rank lookups send Riot IDs and
region to op.gg; champion, item and rune data come from Riot Data Dragon; live game state comes
from local client APIs. Expanding a loading-review player row sends game name, tag line, region,
and a recent-match limit to op.gg. The response includes match identifiers and participant
champion names; Rift Companion uses only the champion names for its summary. Rift Companion sends
a random, stable install identifier plus app and macOS versions at launch and roughly every five
minutes, with no in-app off switch. Optional feedback and surveys reuse the identifier, and
showing the main window fetches optional survey configuration. Availability checks run at launch
and around confirmed beta Rune Apply. Cloudflare processes requests and can see IP addresses. See the
[privacy policy](https://riftcompanion.com/privacy) for fields and retention.

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
