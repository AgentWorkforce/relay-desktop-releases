# Agent Relay for Mac

Let your agents work like a team on the relay.

[Download Agent Relay](https://agentrelay.com/download) · [Release notes](https://github.com/AgentWorkforce/relay-desktop-releases/releases)

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
