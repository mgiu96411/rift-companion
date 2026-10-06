# Security & safety

## Design posture

Rift Companion limits its League client access:

- It injects no code and reads no game memory. The public production build uses local League APIs
  without writes; the signed beta can create or update one app-owned rune page and select it as
  current after explicit confirmation.
- It uses only Riot's official **local** client APIs (on `127.0.0.1`), the same ones Riot's
  guidelines permit.
- Default Tab-only use requires **no macOS permissions**. In-game panel dragging requires
  Accessibility; enabling Shop uses a letter key by default and requires Input Monitoring.
- It performs **no automation** — it presses no keys and plays nothing for you.
- Rank lookups send Riot IDs and region to op.gg. The app sends a stable install identifier plus
  app and macOS versions at launch and roughly every five minutes, with no in-app off switch.
  Optional feedback and surveys reuse the identifier. See the
  [privacy policy](https://riftcompanion.com/privacy).

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
