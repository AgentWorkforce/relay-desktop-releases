# Agent Relay for Mac

Let your agents work like a team on the relay.

[Download Agent Relay](https://agentrelay.com/download) · [Release notes](https://github.com/AgentWorkforce/relay-desktop-releases/releases)

## Release channels

- [Stable releases](https://github.com/AgentWorkforce/relay-desktop-releases/releases?q=prerelease%3Afalse) are the default for downloads and app updates.
- [Beta releases](https://github.com/AgentWorkforce/relay-desktop-releases/releases?q=prerelease%3Atrue) preview upcoming features and may be less reliable. Opt in with **Settings → Updates → Include beta releases** on macOS or Linux.

Release titles identify **Stable** and **Beta**. Beta versions are numbered
(`2026.10.2-beta.1`, `2026.10.2-beta.2`, …), followed by a final stable version
(`2026.10.2`). Beta users also receive newer stable releases. Turning beta off
keeps the installed version until a newer stable release is available.

## Downloads

Requires macOS 13 or later.

| Mac | Latest stable release |
| --- | --- |
| Apple silicon (M1 and later) | [AgentRelay-macOS-arm64.dmg](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-macOS-arm64.dmg) |
| Intel | [AgentRelay-macOS-x64.dmg](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-macOS-x64.dmg) |

Downloads become available after the first release is published.

Open the disk image, drag **Agent Relay** to **Applications**, then open the app and sign in. Choose which coding sessions to share from the app. Upload status and pause controls are available in the menu bar.

## Verify a download

Each disk image has a matching `.sha256` file on its release page. Download both into the same directory, then run:

```sh
shasum -a 256 -c AgentRelay-macOS-arm64.dmg.sha256
```

For Intel, use `AgentRelay-macOS-x64.dmg.sha256` instead.

## About this repository

This repository distributes signed and notarized installers, checksums, and release notes. Application source and build credentials are maintained separately. Versioned filenames preserve older downloads; the stable filenames above follow the latest non-prerelease build.

Visit [agentrelay.com](https://agentrelay.com) for more about Agent Relay.
