<p align="center">
  <img src="docs/debox-logo.svg" width="240" alt="Debox">
</p>

<h3 align="center">
    A decentralized end-to-end encrypted data storage & sharing platform
    <br><br>
    <a href="https://debox.network/">https://debox.network</a>
</h3>

This repository is the public distribution point for Debox. Releases are published via [GitHub
Releases][latest], where you can download the latest release assets for your platform.

Each release entry below lists included components, their versions, and links to their `CHANGELOG.md` files.

### Minimum OS Requirements

- Ubuntu 24.04 LTS
- macOS 15.4
- Windows 11

### Installation

#### Linux (`.deb`)

```bash
sudo apt install ./debox_<version>_linux_<arch>.deb
```

#### macOS (`.dmg`)

1. Open the downloaded `.dmg` file.
2. Move `Debox.app` to `Applications`.
3. Start Debox from `Applications`.

#### Windows (`.exe`)

1. Run the downloaded installer.
2. Follow the setup steps.
3. If needed, allow the bundled Dokany prerequisite to be installed during setup.

### Uninstall

#### Linux

Remove the application:

```bash
sudo apt remove debox
```

Remove package-managed files:

```bash
sudo apt purge debox
```

Remove user data:

```bash
rm -rf ~/.local/share/debox
```

#### macOS

Remove the application:

```bash
rm -rf /Applications/Debox.app
```

Remove user data:

```bash
rm -rf ~/Library/Application\ Support/Debox
```

#### Windows

Remove the application from Settings -> Apps -> Installed apps, or run the Debox uninstaller.

Remove user data:

```text
%LocalAppData%\Debox
```

## Changelog

## [v0.2.0] - 2026-05-22

### Components:

- Debox - [debox v0.3.0][debox-changelog]
- Debox GUI - [debox-gui v0.1.1][debox-gui-changelog]
- Debox CLI - [debox-cli v0.2.0][debox-cli-changelog]
- IPFS Kubo - [kubo v0.41.0][kubo-changelog]
- FSKitBridge - [FSKitBridge v0.2.0][fskitbridge-changelog]
- Dokany - [Dokany v2.3.1.1000][dokany-changelog]

## [v0.1.0] - 2026-04-21

### Components:

- Debox - [debox v0.2.0][debox-changelog]
- Debox GUI - [debox-gui v0.1.0][debox-gui-changelog]
- Debox CLI - [debox-cli v0.2.0][debox-cli-changelog]
- IPFS Kubo - [kubo v0.40.1][kubo-changelog]
- FSKitBridge - [FSKitBridge v0.2.0][fskitbridge-changelog]
- Dokany - [Dokany v2.3.1.1000][dokany-changelog]

[latest]: ../../releases/latest
[v0.2.0]: ../../releases/tag/v0.2.0
[v0.1.0]: ../../releases/tag/v0.1.0
[debox-changelog]: changelogs/debox.md
[debox-gui-changelog]: changelogs/debox-gui.md
[debox-cli-changelog]: changelogs/debox-cli.md
[kubo-changelog]: https://github.com/ipfs/kubo/blob/master/CHANGELOG.md
[fskitbridge-changelog]: https://github.com/debox-network/FSKitBridge/blob/main/CHANGELOG.md
[dokany-changelog]: https://github.com/dokan-dev/dokany/blob/master/CHANGELOG.md
