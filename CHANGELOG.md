# Changelog

All notable changes to GREX are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project uses version tags compatible with Semantic Versioning.

## [Unreleased]

## [v1.2.5] - Unreleased

### Added

- Repository migration guidance for existing installations.
- A fallback update source for continuity during the repository move.
- Basic CI checks for Bash syntax and ShellCheck.
- Runovel-ready governance, security, contribution, and issue templates.

### Changed

- The primary installation and update source is now `runovelhq/grex`.
- Upgrade metadata now keeps the selected version and repository together so
  the download always uses the source that supplied the version.

### Compatibility

- `/srv/GREX`, `/etc/gre-tunnel.conf`, the `grex` command, the `gre-tunnel`
  systemd service, tunnel interface names, and GREX iptables chains remain
  unchanged.

[Unreleased]: https://github.com/runovelhq/grex/compare/v1.2.5...HEAD
[v1.2.5]: https://github.com/runovelhq/grex/compare/v1.2.4...v1.2.5
