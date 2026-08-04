# Changelog

## [Unreleased]

### Fixed
- PID comparison in `stopThread` and `restartThread` now strips null bytes and whitespace, extracts digits only via regex, and uses exact equality instead of substring matching. Prevents unintended PID matches (e.g., PID 12 matching inside "1234").

## [1.41] - Previous release

See README.md for prior history.
