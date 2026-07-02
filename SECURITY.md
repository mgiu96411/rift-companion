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

## Release integrity

Every build is Developer ID-signed and Apple-notarized, releases ship with SHA-256 checksums, and
in-app updates (from 1.3) are EdDSA-signed Sparkle updates served over HTTPS. How to verify all of
it yourself: [docs/verify.md](docs/verify.md).

## Supported versions

Only the [latest release](../../releases/latest) is supported. From version 1.3 the app updates
itself, so staying current is automatic.

## Reporting a vulnerability

Found a security or privacy issue? Please open a
[private security advisory](../../security/advisories/new), or email
**security@riftcompanion.com**. We'll respond as quickly as we can.

Not affiliated with or endorsed by Riot Games.
