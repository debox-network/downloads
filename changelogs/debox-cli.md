# Changelog

## v0.4.0 - 2026-09-03

### Added

- Added `share info`, `pass info`, and `keeper info` commands.
- Added `keeper check` with identity details.

### Changed

- Updated member identifiers and share operation output.
- Updated invite and file version lifecycle commands.

## v0.3.0 - 2026-08-11

### Added

- Added share leave and invite/member remove and restore commands.
- Added file version activation, removal, and restoration.
- Added overwrite and replace options for file transfers.

### Changed

- Updated member management and metadata output for the latest API.

### Removed

- Removed the unsupported `pass remove` command.

## v0.2.0 - 2026-04-21

### Added

- Added the top-level `drive` command group with `mount`, `unmount`, `status`,
  and `driver install`.

### Changed

- Expanded `drive status` output with mount details.
- Updated CLI integration to match the current `debox-api-rust` API.
- Moved the crate to Rust 2024 and refreshed core dependencies.

## v0.1.0 - 2024-10-09

- Initial release of **debox-cli**.
