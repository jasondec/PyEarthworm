# Changelog

## [Unreleased]

### Added
- `CHANGELOG.md` to track project changes.
- `instid` and `modid` fields to the dictionary returned by `EWModule.get_wave()`, exposing the source module and installation IDs from the message logo.
- Dockerfile for building PyEarthworm using pre-compiled Earthworm v8.0b8 binaries on Rocky Linux 9.6 (no source compilation required).
- `docker-compose.yaml` for running the container with bind-mounted params and demo scripts.
- `demo_getwave.py` example script showing continuous waveform reading with `EWModule.get_wave()`.

### Fixed
- PID comparison in `stopThread` and `restartThread` now strips null bytes and whitespace, extracts digits only, and uses exact equality instead of substring matching. Prevents false-positive PID matches (e.g., PID 12 matching inside "1234").

### Changed
- Created `test/earthworm/` directory with Earthworm runtime configuration (params, bin scripts) for containerized testing.
- Updated `.gitignore` to ignore `.vscode/`, `*.state` files, and test directory paths.

## [1.41] - Previous release

See README.md for prior history.
