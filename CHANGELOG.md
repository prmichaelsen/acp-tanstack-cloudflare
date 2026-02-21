# Changelog

All notable changes to this package will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2026-02-21

### Added
- Three production-ready patterns for TanStack Start + Cloudflare Workers development:
  - `library-services` - Service layer architecture with database and API service separation
  - `ssr-preload` - Server-side data preloading using TanStack Router's beforeLoad
  - `user-scoped-collections` - Firestore subcollection pattern for user data isolation
- Two deployment and debugging commands:
  - `deploy` - Build and deploy TanStack Start applications to Cloudflare Workers
  - `tail` - Stream real-time logs from deployed Cloudflare Workers
- All patterns follow ACP template structure with comprehensive documentation
- All patterns include implementation examples, anti-patterns, testing strategies, and migration guides

### Changed
- Updated package.yaml with all patterns and commands
- Updated README.md with auto-generated contents section

## [1.0.0] - 2026-02-21

### Added
- Initial release
- Package structure created with full ACP installation
