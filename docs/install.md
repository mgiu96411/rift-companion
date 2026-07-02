# Install & troubleshooting

## Install

1. Download `Rift Companion-<version>.dmg` from
   [riftcompanion.com/download](https://riftcompanion.com/download) or the
   [latest GitHub Release](../../releases/latest). (A `.zip` of the same app is also published if
   you prefer that format.)
2. Open the `.dmg` and drag **Rift Companion** into **Applications**.
3. Launch **Rift Companion**. It lives in the **menu bar** (top-right of your screen) — there is
   no Dock icon to look for.
4. Start League of Legends. The app detects champ select and the live game automatically; no
   setup, no account, no permissions dialogs.

Want to check the download first? See [Verify a download](verify.md).

## Requirements

- macOS 14 (Sonoma) or later
- Apple silicon (M-series) Mac
- League of Legends installed

## Updates

From version **1.3**, Rift Companion updates itself: when a new version is ready you'll see a
"Relaunch to update" prompt in the app. Versions before 1.3 must be updated manually by
downloading the latest build from the site — one last time.

## Troubleshooting

### "Rift Companion is damaged and can't be opened"

You have a stale download from before builds were notarized (mid-2026). Delete it and download
the current version from [riftcompanion.com/download](https://riftcompanion.com/download) —
current builds are Developer ID-signed and Apple-notarized and open cleanly.

### Panels don't show in game

- Confirm the menu-bar icon is there (the app is running).
- Panels appear when you **hold Tab**, **tap the shop key**, or when set to always-on — check
  which display mode you're in via the menu-bar icon.
- League must be running on the same Mac; the app reads the local client only.

### Champ select shows nothing

The app reads champ select from the local League client. Make sure the League client (not just
the game) is running, and that you're actually in champ select. If it persists, file a
[bug report](../../../issues/new/choose) with your app and macOS versions.

### Panels are in the wrong place

Use **Reposition Panels** from the menu-bar icon to drag them where you want. Positions are saved
per game mode (Summoner's Rift, ARAM, Arena).

### Uninstall

1. Quit Rift Companion from the menu-bar icon.
2. Move **Rift Companion.app** from Applications to the Trash.
3. Optional, to remove all local data:

```sh
rm -rf ~/Library/Application\ Support/RiftCompanion
defaults delete com.riftcompanion.app
```

## Still stuck?

Open an [issue](../../../issues/new/choose) or ask in [Discussions](../../../discussions) — see
[SUPPORT.md](../SUPPORT.md).
