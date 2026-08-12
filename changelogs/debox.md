# Changelog

## [Unreleased]

## [v0.4.0] - 2026-08-11

### common

- **Added:** Unified typed operation storage with deduplication, shared HLC metadata, and ordered
  replay.
- **Added:** Versioned operation snapshots with bounded retention.

### daemon

- **Added:** Exposed RPC commands for version activation and recovery, version remove/restore,
  share leave, invite remove/restore, and member management.
- **Changed:** Shutdown now rejects new commands, drains active work with bounded timeouts, and
  coordinates cleanup of managed services.
- **Fixed:** Shutdown failures and timeouts are now propagated to the daemon process result.

### fs

- **Added:** Complete checkpoint lifecycle with activate, activate-my, remove, remove-all, and
  restore commands.
- **Added:** Version metadata now reports the resolved author, `is_me`, removal state, and the
  current local version.
- **Added:** Explicit overwrite and replace controls for filesystem operations.
- **Changed:** Local versions are persisted immediately and pinned through the background IPFS
  scheduler.
- **Fixed:** Avoided duplicate checkpoints when the current content is already saved.
- **Fixed:** Enforced read-only share boundaries and validated parent trees for create, copy, and
  move operations.
- **Fixed:** Excluded platform-local filesystem entries and Windows alternate data streams from
  share synchronization.
- **Fixed:** Hardened remote operation materialization against placement conflicts and cyclic
  parent relationships.
- **Fixed:** Improved current-version resolution, recursive directory creation, cache fetches, and
  stale operation replay.

### ipfs

- **Added:** A daemon-aware background pin scheduler with deduplication, bounded concurrency, and
  retry backoff.
- **Added:** Bounded recovery for content fetches stalled by stale provider/Bitswap connections.
- **Changed:** Pinning now starts only while the managed Kubo daemon is running and is paused on
  daemon stop or unexpected exit.
- **Changed:** The pin scheduler reloads Kubo's recursive pinset after resume and skips content
  that is already pinned.
- **Changed:** Managed Kubo configuration disables anonymous telemetry and peer event logging.
- **Fixed:** Serialized Kubo lifecycle transitions with pin scheduler state changes.

### peer

- **Added:** Operation-backed client and keeper state with snapshots, pull inboxes, and per-action
  watermarks.
- **Added:** Member role, shared-name, local-alias, remove, restore, and self-leave workflows.
- **Added:** Invite remove/restore and automatic invite pass acceptance.
- **Changed:** Share push and pull now synchronize filesystem and control operations through the
  unified operation model.
- **Changed:** Pass synchronization runs in the background and preserves failed submission status.
- **Fixed:** Improved concurrent push behavior, permission-change handling, credential refresh,
  owner bootstrap, share leave finalization, and missing-share reporting.
- **Fixed:** Prevented owner role changes and synchronized filesystem write access with active
  share membership.

### webdav

- **Changed:** WebDAV now owns platform-specific mount handling and performs bounded connection
  draining during shutdown.

### docs

- **Added:** Architecture, filesystem, share synchronization, project decision, and IPFS recovery
  documentation.
- **Added:** An architecture backlog for deferred filesystem synchronization and CRDT convergence
  issues.

## [v0.3.0] - 2026-05-22

### common
- **Changed:** Unix mount paths now resolve under the user's home directory.
- **Changed:** Moved more configuration ownership into the modules that define each runtime
  section.

### daemon
- **Changed:** Updated daemon runtime wiring for the refactored peer and service modules.

### drive
- **Fixed:** Improved platform drive backends to respect filesystem/share access boundaries.

### fs
- **Changed:** Improved tree lookup, readonly handling, and file operation behavior around
  copy, move, remove, and metadata flows.
- **Fixed:** Enforced share boundaries in filesystem operations and CRDT synchronization.

### ipfs
- **Added:** Cache-oriented IPFS helpers, including DAG export and retry support for fetching
  data through the cache path.
- **Changed:** Improved Kubo startup, peer configuration, routing provide, name publish, and
  network reachability handling.

### peer
- **Added:** Debox Cache upload flow for making keeper-published content available through Mesh.
- **Added:** Keeper-side Mesh auth, probe, relay reservation, and event-driven identity publish
  flow.
- **Changed:** Reworked keeper runtime logic and split share handling into focused keeper modules.
- **Fixed:** Improved direct and relay dialing, relay address publication, identity retry behavior,
  and client connection logging.

### webdav
- **Changed:** Updated WebDAV runtime wiring and dependency versions.

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

### peer
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

[Unreleased]: ../../compare/v0.4.0...HEAD
[v0.4.0]: ../../releases/tag/v0.4.0
[v0.3.0]: ../../releases/tag/v0.3.0
[v0.2.0]: ../../releases/tag/v0.2.0
[v0.1.0]: ../../releases/tag/v0.1.0
