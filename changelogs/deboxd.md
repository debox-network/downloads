# Changelog

## [Unreleased]

## [v0.2.0] - 2026-04-21
### common
- **Added:** Shared runtime infrastructure for configuration, process execution, clocks, path
  resolution, and embedded key-value storage.
- **Changed:** Unified command wiring and service bootstrap behavior across workspace modules.

### daemon
- **Added:** A coordinated shutdown path for the local JSON-RPC runtime and managed services.
- **Changed:** Improved command execution, detached lifecycle commands, and daemon startup/shutdown
  orchestration.

### drive
- **Added:** Cross-platform drive backends for Linux FUSE, macOS FSKit, and Windows Dokan.
- **Changed:** Standardized mount, unmount, status, and mount-confirmation flows across platform
  implementations.
- **Fixed:** Improved mount lifecycle cleanup, external unmount handling, and path-based status
  reporting.

### fs
- **Added:** A broader filesystem core around CRDT-backed tree state, operations, snapshots,
  versions, file metadata, directories, files, and symlinks.
- **Changed:** Reworked internal file and directory handling to use richer operation/state models.
- **Fixed:** Improved compatibility with expected filesystem semantics, including timestamps,
  ownership, rename, truncate, streams, and link behavior.

### ipfs
- **Added:** Stronger daemon and peer separation for local IPFS runtime management.
- **Changed:** Improved repository/config handling, binary/data path resolution, and daemon control
  flow.
- **Fixed:** Better startup, shutdown, timeout, initialization, and peer-side error reporting.

### protocol
- **Added:** Expanded keeper/client workflows for share creation, invites, passes, members, push,
  and pull flows.
- **Changed:** Reworked session, identity, local store, role/action, and connection handling for
  peer-to-peer communication.
- **Fixed:** Improved keeper/client startup, dialing, relay/direct address handling, and access
  checks.

### webdav
- **Changed:** Updated WebDAV integration to align with the newer filesystem and daemon runtime.

### os
- **Added:** Expanded platform-specific helpers for mounting, Windows system operations, and OS
  integration paths.

## [v0.1.0] - 2024-10-09

- Initial release of **debox**. See details in the [README](README.md).

[Unreleased]: ../../compare/v0.2.0...HEAD
[v0.2.0]: ../../releases/tag/v0.2.0
[v0.1.0]: ../../releases/tag/v0.1.0
