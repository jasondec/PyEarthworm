# Changelog

## [Unreleased]

### Fixed
- PID comparison in `stopThread` and `restartThread` now strips null bytes and whitespace, extracts digits only via regex, and uses exact equality instead of substring matching. Prevents unintended PID matches (e.g., PID 12 matching inside "1234").
### Added
- Dockerfile using pre-compiled Earthworm v8.0b8 binaries on Rocky Linux 9.6 (no source compilation required).
- `docker-compose.yaml` for running the container with bind-mounted params and demo scripts.
- `.dockerignore` to exclude build artifacts and state files from the build context.
- `test/earthworm/` directory with Earthworm runtime configuration (params, bin scripts) for containerized testing.
- `demo_getwave.py` example script showing continuous waveform reading with `EWModule.get_wave()`.
- GitHub Actions CI pipeline (`.github/workflows/test-pyew.yaml`) that builds the container, starts Earthworm, and verifies PyEW can import, attach to rings, and receive waveform data.

### Changed
- Updated `.gitignore` for test directory paths.

## [1.41] - Previous release

See README.md for prior history.
