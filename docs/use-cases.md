# What players use Rift Companion for

Real use cases, in the words players search with. Everything below is read-only and works with
zero setup.

## "I don't want to alt-tab to op.gg mid-game on my Mac"

The core use case. Runes and the current-patch build appear in champ select the moment you lock
your champion, and build/matchup panels sit beside the game while you play. No second monitor, no
phone propped against the keyboard, no alt-tabbing out of a fullscreen game.

## "I switched from Windows and miss Porofessor / Blitz / Mobalytics"

Those apps run on Overwolf, which doesn't exist for macOS — they will not run on your Mac.
Rift Companion is the native Mac alternative: champ-select runes and builds, in-game panels, and
summoner-spell timers, built directly for the Mac League client. See the
[comparison in the README](../README.md#rift-companion-vs-the-windows-only-companions-on-mac).

## "Is enemy Flash up?"

Click an enemy's summoner spell in the cooldowns panel when they use it. The timer counts back
up — aware of cooldown-reducing items and summoner levels — so you know when Flash or Ignite is
back. Marking is manual and deliberate: the app never watches the game for you, which is exactly
why it stays clean. (It does not track ability or ultimate cooldowns — there is no honest way to
know them without reading game memory, which the app will never do.)

## "Am I actually ahead in lane?"

Hold Tab: the gold panel pairs you against your direct lane opponent, colors whoever is ahead,
and shows per-champion totals and which team leads overall. Release Tab and it's gone.

## "I play ARAM / Arena, not just Summoner's Rift"

Panels work across Summoner's Rift, ARAM, and Arena, and remember their positions separately per
mode.

## "I want help, but I'm not risking my account"

Rift Companion is read-only: official local Riot APIs only, no memory reading, no injection, no
input automation, and no macOS permissions by default. It runs alongside the embedded Vanguard
anti-cheat on macOS. Riot's policies can change and your account is your responsibility — but the
design never crosses the lines Riot's guidelines draw. Details: [SECURITY.md](../SECURITY.md) and
the [FAQ](../FAQ.md).

---

Something you'd use it for that isn't covered? [Tell us](../../../discussions) — feature ideas
within the read-only scope are genuinely welcome.
