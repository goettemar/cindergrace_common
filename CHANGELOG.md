# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.0] - 2026-01-12

### Added
- DateTime utilities: `utcnow()` and `generate_id()` for consistent timestamps and ULID-based IDs
- Exported at package level for easy access

### Changed
- Updated exports in `__init__.py` and `utils/__init__.py`

## [0.3.0] - 2025-12-15

### Added
- Git backup utilities: `create_git_mirror_backup()`, `restore_from_backup()`, `list_backups()`
- Secret store for secure credential management

## [0.2.0] - 2025-11-01

### Added
- Gradio UI theming utilities
- Path sanitization and security utilities
- Logging setup with colored formatter

## [0.1.0] - 2025-10-01

### Added
- Initial release
- Base configuration with environment variable support
- Security mixin for localhost binding
- Branding utilities
- i18n support
- State persistence (JSON, XDG)
- CLI argument parsing
- Retry utilities
