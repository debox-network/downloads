# Changelog

## [Unreleased]

## [v0.2.0] - 2026-08-05

### Added

- Manage share members, including names, roles, removal, and restoration.
- Edit and remove share invites with explicit deletion confirmation.
- Review and manage file version history, including authors, activation,
  restoration, and deletion.
- Start the managed daemon on either a random or configured dynamic port.

### Changed

- Keep Explorer Refresh local-only and use Sync for remote share
  reconciliation.
- Apply daemon action permissions consistently to member, invite, and version
  operations.
- Load access and version data on demand and guard panels against stale async
  results.

### Fixed

- Enforce a single application instance on Linux.
- Improve daemon, Keeper, share sync, and pass-status error handling.
- Keep access and version panels consistent after sync, refresh, permission
  changes, and file navigation.

## [v0.1.1] - 2026-05-22

### Fixed

- Handle updated local Keeper error codes when recovering failed operations.
- Ignore transient local Keeper connection errors in the UI error panel.

## [v0.1.0] - 2026-04-21

- Initial release of **debox-gui**. See details in the [README](README.md).

[Unreleased]: ../../compare/v0.2.0...HEAD
[v0.2.0]: ../../releases/tag/v0.2.0
[v0.1.1]: ../../releases/tag/v0.1.1
[v0.1.0]: ../../releases/tag/v0.1.0
