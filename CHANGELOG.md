# 📜 Changelog

## [0.1.1] - 2025-04-21

## [0.1.2] - 2025-04-22
### Added
- Receive Mode (V) Listen for incoming UDP packets on a user-selected or default IP.
- Interface Selection for Receive Mode: Defaults to 0.0.0.0 (all interfaces) for maximum compatibility.
- Command History Logging: Every sent command (via UDP) is logged in command.history.json.
- Resend from History (R): View a numbered list of recently sent commands.
### Changed
- Improved setup.py: Fixed UnicodeDecodeError on install by adding encoding="utf-8" to README.md loading.

## [0.1.3] - 2025-04-22
### Fixed
- Fixed bug in bump_version.py

## [0.1.4] - 2025-04-22
