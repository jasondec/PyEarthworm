# Changelog

## [Unreleased]

### Added
- Optional `instid` parameter to `get_wave()`, `get_msg()`, and `copymsg_type()`. Pass `instid=0` for wildcard (all installations) or a specific ID to filter. Default behavior is unchanged.
- `modid` and `instid` fields in the dictionary returned by `get_wave()`, exposing the source module and installation IDs from the MSG_LOGO.
- `copymsg_type()` now returns the response MSG_LOGO struct as a 4th element in its return tuple.
- Docstrings for `copymsg_type()`, `get_msg()`, and `get_wave()`.
- Updated README API documentation to reflect new parameters and return values.

## [1.41] - Previous release

See README.md for prior history.
