# Verify a download

Every Rift Companion release is Developer ID-signed and Apple-notarized, and ships with SHA-256
checksums. You can verify all of it with tools already on your Mac.

## 1. Checksum (file integrity)

Each [GitHub Release](../../../releases) attaches a `SHA256SUMS-<version>.txt` covering the
`.dmg` and `.zip`. With the downloaded files and the checksum file in the same folder:

```sh
shasum -a 256 -c SHA256SUMS-1.2.txt
```

Expected output: `RiftCompanion-1.2.dmg: OK` (and the same for the `.zip`). Or hash a single
file and compare against the sums file by eye:

```sh
shasum -a 256 RiftCompanion-1.2.dmg
```

Naming note: GitHub release assets carry dot-free names (`RiftCompanion-1.2.dmg`), while the
website download has a space (`Rift Companion-1.2.dmg`). The bytes are identical — to verify a
website download with `-c`, rename it to the GitHub name first, or just compare the hash by eye.

Checksums are attached from version 1.2 onward. The 1.1 release predates the notarization
pipeline and no longer distributes binaries — download the latest version instead.

## 2. Code signature (who built it)

```sh
codesign -dv --verbose=2 "/Applications/Rift Companion.app"
```

The `Authority` chain must read:

```
Authority=Developer ID Application: Jose Mariano Macri (AR6HZG8A2K)
Authority=Developer ID Certification Authority
Authority=Apple Root CA
```

## 3. Notarization (Apple scanned it)

```sh
spctl -a -vv "/Applications/Rift Companion.app"
xcrun stapler validate "/Applications/Rift Companion.app"
```

Expected: `accepted · source=Notarized Developer ID` and `The validate action worked!`.

## 4. In-app updates

Auto-updates (version 1.3+) are delivered by [Sparkle](https://sparkle-project.org) over HTTPS
and must carry a valid EdDSA signature before they install. The public key embedded in the app:

```
UvmYuMcZxFalNDFPnywXWLMsjTL1QYC7wvI+hYn6cDI=
```

## Something doesn't match?

Don't run the app. Delete the download, fetch it again from
[riftcompanion.com/download](https://riftcompanion.com/download), and if it still fails, report
it privately — see [SECURITY.md](../SECURITY.md).
