# Changelog

All notable changes to this package will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.3.0] - 2026-03-15

### Added
- `tanstack-cloudflare.sortable-filterable-tables` pattern — unified sortable/filterable data table system with ColumnConfig, useSortableData hook, and responsive desktop table + mobile card views

### Changed
- Updated ACP core to v5.21.0
- Package now contains 43 patterns and 2 commands

## [1.2.0] - 2026-03-14

### Added
- 26 new patterns registered in package.yaml across 5 categories:
  - **Firebase**: auth, firestore, storage, anonymous-sessions
  - **UI Components**: unified-header, modal, lightbox, slide-over, toast-system, card-and-list, image-carousel, form-controls, pagination, pill-input, searchable-settings, action-bar-item, expander
  - **Real-time/Communication**: chat-engine, websocket-manager, notifications-engine, fcm-push, mention-suggestions
  - **Utilities**: og-metadata, oauth-token-refresh, markdown-content, global-search-context
- New `tanstack-cloudflare.og-metadata` pattern for Open Graph metadata handling

### Changed
- Updated ACP core to v5.18.2
- Package now contains 42 patterns and 2 commands (up from 16 patterns)

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
