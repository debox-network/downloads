<p align="center">
  <img src="docs/debox-logo.svg" width="240" alt="Debox">
</p>

<h3 align="center">
    A decentralized, end-to-end encrypted drive for storing, syncing, and sharing your data
    <br><br>
    <a href="https://debox.network/">https://debox.network</a>
</h3>

This repository is the public distribution point for Debox. Download the latest release assets for your platform from
[GitHub Releases][latest].

> [!WARNING]
> **Debox is alpha software intended for testing and evaluation.**
>
> Features may be incomplete, bugs and security vulnerabilities may exist, and future releases may introduce breaking
> changes or require resetting local data.
>
> Keep independent backups of data stored in Debox during the alpha period.
>
> The software is provided as is, without guarantees of stability, compatibility, or performance. By using Debox, you
> accept these risks.

## Usage Guide

Watch the [Debox video guide][video-guide] for a walkthrough of the application.

## Minimum OS Requirements

- Ubuntu 24.04 LTS
- macOS 15.4
- Windows 11

## Installation

### Linux (`.deb`)

```bash
sudo apt install ./debox_0.4.0_linux_amd64.deb
```

### macOS (`.dmg`)

1. Open the downloaded `.dmg` file.
2. Drag `Debox.app` to the `Applications` folder.
3. Start Debox from the `Applications` folder.

### Windows (`.exe`)

1. Run the downloaded installer.
2. Follow the setup steps.
3. Allow the installer to install Dokany if prompted.

## Uninstall

### Linux

Remove the application:

```bash
sudo apt remove debox
```

Remove the application and its package configuration:

```bash
sudo apt purge debox
```

Remove user data:

```bash
rm -rf ~/.local/share/debox
```

### macOS

Remove the application:

```bash
rm -rf /Applications/Debox.app
```

Remove user data:

```bash
rm -rf ~/Library/Application\ Support/Debox
```

### Windows

Remove the application from Settings > Apps > Installed apps, or run the Debox uninstaller.

Remove user data with PowerShell:

```powershell
Remove-Item -Recurse -Force "$env:LOCALAPPDATA\Debox"
```

## Changelog

Each release entry lists included components, their versions, and links to their `CHANGELOG.md` files.

### [v0.4.0] - 2026-09-03

#### Components

- Debox - [debox v0.5.0][debox-changelog]
- Debox GUI - [debox-gui v0.2.1][debox-gui-changelog]
- Debox CLI - [debox-cli v0.4.0][debox-cli-changelog]
- IPFS Kubo - [kubo v0.43.0][kubo-changelog]
- FSKitBridge - [FSKitBridge v0.2.0][fskitbridge-changelog]
- Dokany - [Dokany v2.3.1.1000][dokany-changelog]

### [v0.3.0] - 2026-08-11

#### Components

- Debox - [debox v0.4.0][debox-changelog]
- Debox GUI - [debox-gui v0.2.0][debox-gui-changelog]
- Debox CLI - [debox-cli v0.3.0][debox-cli-changelog]
- IPFS Kubo - [kubo v0.43.0][kubo-changelog]
- FSKitBridge - [FSKitBridge v0.2.0][fskitbridge-changelog]
- Dokany - [Dokany v2.3.1.1000][dokany-changelog]

### [v0.2.0] - 2026-05-22

#### Components

- Debox - [debox v0.3.0][debox-changelog]
- Debox GUI - [debox-gui v0.1.1][debox-gui-changelog]
- Debox CLI - [debox-cli v0.2.0][debox-cli-changelog]
- IPFS Kubo - [kubo v0.41.0][kubo-changelog]
- FSKitBridge - [FSKitBridge v0.2.0][fskitbridge-changelog]
- Dokany - [Dokany v2.3.1.1000][dokany-changelog]

### [v0.1.0] - 2026-04-21

#### Components

- Debox - [debox v0.2.0][debox-changelog]
- Debox GUI - [debox-gui v0.1.0][debox-gui-changelog]
- Debox CLI - [debox-cli v0.2.0][debox-cli-changelog]
- IPFS Kubo - [kubo v0.40.1][kubo-changelog]
- FSKitBridge - [FSKitBridge v0.2.0][fskitbridge-changelog]
- Dokany - [Dokany v2.3.1.1000][dokany-changelog]

[video-guide]: https://youtu.be/z3QGAdwM3Ec
[latest]: ../../releases/latest
[v0.4.0]: ../../releases/tag/v0.4.0
[v0.3.0]: ../../releases/tag/v0.3.0
[v0.2.0]: ../../releases/tag/v0.2.0
[v0.1.0]: ../../releases/tag/v0.1.0
[debox-changelog]: changelogs/debox.md
[debox-gui-changelog]: changelogs/debox-gui.md
[debox-cli-changelog]: changelogs/debox-cli.md
[kubo-changelog]: https://github.com/ipfs/kubo/blob/master/CHANGELOG.md
[fskitbridge-changelog]: https://github.com/debox-network/FSKitBridge/blob/main/CHANGELOG.md
[dokany-changelog]: https://github.com/dokan-dev/dokany/blob/master/CHANGELOG.md
