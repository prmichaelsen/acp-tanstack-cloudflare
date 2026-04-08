# Changelog

All notable changes to this package will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.1.0] - 2026-04-08

### Added
- 7 new pattern documents extracted from cleanbook-tanstack:
  - `authenticated-loader` — createAuthenticatedLoader factory and requireSession helper for DRY route loaders
  - `action-token-validation` — centralized token-parse/validate helpers for email action links (claim, confirm, decline)
  - `subdomain-routing` — middleware that maps vanity subdomains to internal routes
  - `search-param-validation` — inline and Zod-based validateSearch for type-safe URL search params
  - `chat-messages-hook` — useChatMessages combining REST initial load with WebSocket live updates
  - `perf-timing` — lightweight perf() utility for server-side operation timing
  - `pagination-params-hook` — usePaginationParams for URL-synced page/pageSize/mode state

## [2.0.0] - 2026-03-15

### Added
- **39 starter template files** in `agent/files/src/` — production-tested source code installable via `acp install tanstack-cloudflare --files`
  - **UI Primitives** (5): Modal, SlideOverPanel, PillInput, Typeahead, SearchBar
  - **Data Display** (9): SortableTable, MobileCardList, EntityTable, Paginator, PaginationToggle, PaginationSlideOver, ColumnFilter, SortIndicator, useSortableData
  - **Layout** (5): UnifiedHeader, UnifiedFooter, Sidebar, MobileBottomNav, MenuDropdown
  - **Wizard** (2): WizardShell, useWizardState
  - **Auth** (5): AuthContext, AuthForm, login/logout/session API routes
  - **Notifications** (5): NotificationBell, NotificationPanel, useNotifications, notification-hub DO, notifications-ws route
  - **Media** (3): PhotoGallery, PhotoUpload, upload-manager DO
  - **Infrastructure** (5): GlobalSearchContext, useActionToast, TOS consent, settings route, router
- 5 new pattern documents:
  - `wizard-system` — multi-step wizard with URL-synced state and sessionStorage
  - `typeahead` — multi-select combobox with search and keyboard navigation
  - `signed-url-upload` — two-phase upload with progress tracking
  - `tos-consent` — versioned consent tracking with IP logging
  - `mobile-bottom-nav` — fixed bottom navigation for mobile
- ACP variable substitution support (APP_NAME, PRIMARY_COLOR, AUTH_REDIRECT)
- `contents.files` section in package.yaml with 39 file entries
- Design document for starter templates architecture

### Changed
- **BREAKING**: Package now ships `contents.files` (requires ACP >=5.21.0)
- Package version bumped from 1.3.0 to 2.0.0
- README reorganized with template file documentation, dependency table, and variable reference
- Package now contains 48 patterns, 2 commands, and 39 template files

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
