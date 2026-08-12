# Changelog

## [Unreleased]

## [v0.3.0] - 2026-08-11

### Added

- Added share leave and invite/member remove and restore commands.
- Added file version activation, removal, and restoration.
- Added overwrite and replace options for file transfers.

### Changed

- Updated member management and metadata output for the latest API.

### Removed

- Removed the unsupported `pass remove` command.

## [v0.2.0] - 2026-04-21

### Added

- Added the top-level `drive` command group with `mount`, `unmount`, `status`,
  and `driver install`.

### Changed

- Expanded `drive status` output with mount details.
- Updated CLI integration to match the current `debox-api-rust` API.
- Moved the crate to Rust 2024 and refreshed core dependencies.

## [v0.1.0] - 2024-10-09

- Initial release of **debox-cli**. See details in the [README](README.md).

[Unreleased]: ../../compare/v0.3.0...HEAD
[v0.3.0]: ../../releases/tag/v0.3.0
[v0.2.0]: ../../releases/tag/v0.2.0
[v0.1.0]: ../../releases/tag/v0.1.0
