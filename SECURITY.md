# Security & safety

## Design posture

Rift Companion is **read-only** by design:

- It never writes to the League client, injects no code, and reads no game memory.
- It uses only Riot's official **local** client APIs (on `127.0.0.1`), the same ones Riot's
  guidelines permit.
- It requires **no macOS permissions** by default — no Screen Recording, Accessibility, or
  Input Monitoring.
- It performs **no automation** — it presses no keys and plays nothing for you.
- Your game data never leaves your Mac. The app sends only an anonymous usage ping (opt-out in
  Settings).

Riot's policies can change, and your account is your responsibility. Rift Companion does not claim
to be Riot-approved or ban-proof.

## Reporting a vulnerability

Found a security or privacy issue? Please open a
[private security advisory](../../security/advisories/new), or email
**security@riftcompanion.com**. We'll respond as quickly as we can.

Not affiliated with or endorsed by Riot Games.
