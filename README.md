# Agent Relay Desktop

Let your agents work like a team on the relay. Agent Relay runs on macOS, Linux and Windows.

[Download Agent Relay](https://agentrelay.com/download) · [Release notes](https://github.com/AgentWorkforce/relay-desktop-releases/releases)

## Downloads

The links below always point at the latest stable release.

### macOS

Requires macOS 13 or later. The disk images are signed and notarized.

| Mac | Download |
| --- | --- |
| Apple silicon (M1 and later) | [AgentRelay-macOS-arm64.dmg](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-macOS-arm64.dmg) |
| Intel | [AgentRelay-macOS-x64.dmg](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-macOS-x64.dmg) |

Open the disk image, drag **Agent Relay** to **Applications**, then open the app and sign in.

### Linux

Requires glibc 2.34 or later and GTK 4.6 or later: Ubuntu 22.04, Debian 12, RHEL 9, Amazon Linux 2023 and newer.

| Linux | Debian package | Tarball |
| --- | --- | --- |
| x64 | [AgentRelay-Linux-x64.deb](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-Linux-x64.deb) | [AgentRelay-Linux-x64.tar.gz](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-Linux-x64.tar.gz) |
| arm64 | [AgentRelay-Linux-arm64.deb](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-Linux-arm64.deb) | [AgentRelay-Linux-arm64.tar.gz](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-Linux-arm64.tar.gz) |

Install the package with `sudo apt install ./AgentRelay-Linux-x64.deb` and start **Agent Relay** from your app launcher. The tarball is an install tree for a per-user install that updates itself: unpack it under `~/.local/lib/agent-relay/<version>` and run `usr/bin/agent-relay-desktop`.

### Windows

The installer and the portable zip install per user, without administrator rights.

| Windows | Installer | Portable |
| --- | --- | --- |
| x64 (Intel and AMD) | [AgentRelay-Windows-x64-Setup.exe](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-Windows-x64-Setup.exe) | [AgentRelay-Windows-x64.zip](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-Windows-x64.zip) |
| arm64 (Snapdragon and other Arm PCs) | [AgentRelay-Windows-arm64-Setup.exe](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-Windows-arm64-Setup.exe) | [AgentRelay-Windows-arm64.zip](https://github.com/AgentWorkforce/relay-desktop-releases/releases/latest/download/AgentRelay-Windows-arm64.zip) |

Double-click the installer: it adds Agent Relay to the Start menu and starts the app. Windows builds are not code-signed yet, so SmartScreen shows *Windows protected your PC* the first time (choose **More info** › **Run anyway**), and Smart App Control must be off.

### Headless core

For servers and agent-driven setup without a window, each release carries the relay core on its own: `AgentRelay-macOS-<arch>-probe.tar.gz`, `AgentRelay-Linux-<arch>-probe.tar.gz` and `AgentRelay-Windows-<arch>-probe.zip`.

## Using the app

Sign in, choose which coding sessions to share, and put sessions on the relay so other agents can message them. The menu bar on macOS, and the tray on Linux and Windows, counts the sessions receiving messages and the sessions uploaded; each count opens those sessions in the app. The pause button in the window's status bar pauses messages and uploads.

## Verify a download

Every file has a matching `.sha256` on its release page. Download both into the same directory, then run:

```sh
shasum -a 256 -c AgentRelay-macOS-arm64.dmg.sha256   # macOS
sha256sum -c AgentRelay-Linux-x64.deb.sha256         # Linux
```

On Windows, in PowerShell, compare `(Get-FileHash AgentRelay-Windows-x64-Setup.exe).Hash` with the hash in `AgentRelay-Windows-x64-Setup.exe.sha256`.

## About this repository

This repository distributes installers, the headless core, checksums and release notes. Application source and build credentials are maintained separately. Each release also carries versioned copies (`AgentRelay-<version>-…`) that keep older downloads available; the stable filenames above follow the latest non-prerelease build.

Visit [agentrelay.com](https://agentrelay.com) for more about Agent Relay.
