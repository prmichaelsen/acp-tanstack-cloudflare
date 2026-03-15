# ACP Package: tanstack-cloudflare

TanStack + Cloudflare patterns, commands, and starter template files for ACP projects

## Installation

```bash
@acp.package-install https://github.com/prmichaelsen/acp-tanstack-cloudflare.git
```

Or using the installation script:

```bash
./agent/scripts/acp.package-install.sh https://github.com/prmichaelsen/acp-tanstack-cloudflare.git
```

## What's Included

<!-- ACP_AUTO_UPDATE_START:CONTENTS -->
### Commands

- **[deploy](agent/commands/tanstack-cloudflare.deploy.md)** - Build and deploy TanStack Start application to Cloudflare Workers using local environment configuration
- **[tail](agent/commands/tanstack-cloudflare.tail.md)** - Stream real-time logs from deployed TanStack Start application on Cloudflare Workers

### Patterns (48)

#### Core Architecture
- **[library-services](agent/patterns/tanstack-cloudflare.library-services.md)** - Service layer architecture with database and API service separation
- **[api-route-handlers](agent/patterns/tanstack-cloudflare.api-route-handlers.md)** - TanStack Start API route pattern with auth, validation, and error handling
- **[ssr-preload](agent/patterns/tanstack-cloudflare.ssr-preload.md)** - Server-side data preloading using TanStack Router's beforeLoad
- **[zod-schema-validation](agent/patterns/tanstack-cloudflare.zod-schema-validation.md)** - Centralized Zod schemas as single source of truth for data models

#### Cloudflare Infrastructure
- **[durable-objects-websocket](agent/patterns/tanstack-cloudflare.durable-objects-websocket.md)** - Durable Objects as WebSocket servers with dependency injection
- **[wrangler-configuration](agent/patterns/tanstack-cloudflare.wrangler-configuration.md)** - Complete wrangler.toml setup for TanStack Start with DO bindings
- **[rate-limiting](agent/patterns/tanstack-cloudflare.rate-limiting.md)** - Cloudflare rate limiting with separate tiers for auth, API, and WebSocket
- **[scheduled-tasks](agent/patterns/tanstack-cloudflare.scheduled-tasks.md)** - Cloudflare Cron Triggers for periodic background tasks

#### Security & Auth
- **[auth-session-management](agent/patterns/tanstack-cloudflare.auth-session-management.md)** - Cookie-based session management with Firebase Admin SDK
- **[firebase-auth](agent/patterns/tanstack-cloudflare.firebase-auth.md)** - Firebase Authentication client-side integration
- **[firebase-firestore](agent/patterns/tanstack-cloudflare.firebase-firestore.md)** - Firestore data access patterns
- **[firebase-storage](agent/patterns/tanstack-cloudflare.firebase-storage.md)** - Firebase/GCS storage integration
- **[firebase-anonymous-sessions](agent/patterns/tanstack-cloudflare.firebase-anonymous-sessions.md)** - Anonymous auth session management
- **[user-scoped-collections](agent/patterns/tanstack-cloudflare.user-scoped-collections.md)** - Firestore subcollection pattern for user data isolation
- **[acl-permissions](agent/patterns/tanstack-cloudflare.acl-permissions.md)** - Fine-grained permission model with authority hierarchy
- **[confirmation-tokens](agent/patterns/tanstack-cloudflare.confirmation-tokens.md)** - Two-step confirmation flow for AI-initiated mutations
- **[tos-consent](agent/patterns/tanstack-cloudflare.tos-consent.md)** - Versioned TOS consent tracking with IP logging

#### UI Components
- **[unified-header](agent/patterns/tanstack-cloudflare.unified-header.md)** - Fixed header with nav, notifications, and menu
- **[modal](agent/patterns/tanstack-cloudflare.modal.md)** - Portal-based modal with confirmation variants
- **[slide-over](agent/patterns/tanstack-cloudflare.slide-over.md)** - Animated slide-over panel
- **[toast-system](agent/patterns/tanstack-cloudflare.toast-system.md)** - Toast notification system
- **[pill-input](agent/patterns/tanstack-cloudflare.pill-input.md)** - Multi-select pill/tag input
- **[typeahead](agent/patterns/tanstack-cloudflare.typeahead.md)** - Multi-select combobox with search
- **[pagination](agent/patterns/tanstack-cloudflare.pagination.md)** - Pagination controls with toggle modes
- **[card-and-list](agent/patterns/tanstack-cloudflare.card-and-list.md)** - Responsive card/list views
- **[sortable-filterable-tables](agent/patterns/tanstack-cloudflare.sortable-filterable-tables.md)** - Sortable/filterable data tables
- **[form-controls](agent/patterns/tanstack-cloudflare.form-controls.md)** - Form control patterns
- **[lightbox](agent/patterns/tanstack-cloudflare.lightbox.md)** - Image lightbox viewer
- **[image-carousel](agent/patterns/tanstack-cloudflare.image-carousel.md)** - Image carousel component
- **[expander](agent/patterns/tanstack-cloudflare.expander.md)** - Expandable content sections
- **[mobile-bottom-nav](agent/patterns/tanstack-cloudflare.mobile-bottom-nav.md)** - Fixed bottom nav for mobile
- **[searchable-settings](agent/patterns/tanstack-cloudflare.searchable-settings.md)** - Searchable settings page
- **[action-bar-item](agent/patterns/tanstack-cloudflare.action-bar-item.md)** - Config-driven action bar

#### Real-time & Communication
- **[notifications-engine](agent/patterns/tanstack-cloudflare.notifications-engine.md)** - Real-time notification system
- **[websocket-manager](agent/patterns/tanstack-cloudflare.websocket-manager.md)** - WebSocket connection management
- **[chat-engine](agent/patterns/tanstack-cloudflare.chat-engine.md)** - Real-time chat system
- **[fcm-push](agent/patterns/tanstack-cloudflare.fcm-push.md)** - Firebase Cloud Messaging push notifications
- **[mention-suggestions](agent/patterns/tanstack-cloudflare.mention-suggestions.md)** - @mention suggestion system
- **[global-search-context](agent/patterns/tanstack-cloudflare.global-search-context.md)** - Cross-component search state

#### Integrations
- **[third-party-api-integration](agent/patterns/tanstack-cloudflare.third-party-api-integration.md)** - Wrapping external APIs
- **[email-service](agent/patterns/tanstack-cloudflare.email-service.md)** - Transactional email service
- **[oauth-token-refresh](agent/patterns/tanstack-cloudflare.oauth-token-refresh.md)** - OAuth token refresh patterns
- **[provider-adapter](agent/patterns/tanstack-cloudflare.provider-adapter.md)** - Pluggable provider architecture

#### Advanced Patterns
- **[wizard-system](agent/patterns/tanstack-cloudflare.wizard-system.md)** - Multi-step wizard with URL-synced state
- **[signed-url-upload](agent/patterns/tanstack-cloudflare.signed-url-upload.md)** - Two-phase signed-URL upload with progress
- **[og-metadata](agent/patterns/tanstack-cloudflare.og-metadata.md)** - Open Graph metadata handling
- **[markdown-content](agent/patterns/tanstack-cloudflare.markdown-content.md)** - Markdown rendering

#### Migration
- **[nextjs-to-tanstack-routing](agent/patterns/tanstack-cloudflare.nextjs-to-tanstack-routing.md)** - Next.js App Router to TanStack Start mapping

### Starter Template Files (39)

Production-tested source files you can install directly into your project:

```bash
# Install all template files
acp install tanstack-cloudflare --files

# Install specific files
acp install tanstack-cloudflare --files src/components/ui/Modal.tsx src/hooks/useWizardState.ts
```

#### UI Primitives (`components/ui/`)
| File | Description |
|------|-------------|
| `Modal.tsx` | Portal modal + ConfirmationModal (ESC dismiss, scroll lock) |
| `SlideOverPanel.tsx` | Right-slide panel with backdrop |
| `PillInput.tsx` | Multi-select pill/tag input (fuse.js) |
| `Typeahead.tsx` | Multi-select combobox with search |
| `SearchBar.tsx` | Search input + clear button |

#### Data Display (`components/data/`)
| File | Description |
|------|-------------|
| `SortableTable.tsx` | Generic sortable table with column config |
| `MobileCardList.tsx` | Mobile card companion to SortableTable |
| `EntityTable.tsx` | Responsive table+card with Fuse search |
| `Paginator.tsx` | Full pagination bar with inline editing |
| `PaginationToggle.tsx` | Pages vs infinite scroll toggle |
| `PaginationSlideOver.tsx` | Slide-over composing pagination controls |
| `ColumnFilter.tsx` | Inline column filter dropdown |
| `SortIndicator.tsx` | Sort direction arrow |
| `useSortableData.ts` | Sort/filter state hook |

#### Layout (`components/layout/`)
| File | Description |
|------|-------------|
| `UnifiedHeader.tsx` | Fixed header with nav, notifications, menu |
| `UnifiedFooter.tsx` | Fixed footer with safe-area padding |
| `Sidebar.tsx` | Responsive sidebar with mobile overlay |
| `MobileBottomNav.tsx` | Fixed bottom nav bar for mobile |
| `MenuDropdown.tsx` | Full-width dropdown menu |

#### Wizard (`components/wizard/` + `hooks/`)
| File | Description |
|------|-------------|
| `WizardShell.tsx` | Multi-step wizard layout with progress bar |
| `useWizardState.ts` | URL-synced wizard state with sessionStorage |

#### Auth — Firebase (`components/auth/` + `routes/api/auth/`)
| File | Description |
|------|-------------|
| `AuthContext.tsx` | Firebase auth context + session sync |
| `AuthForm.tsx` | Login/signup/forgot multi-mode form |
| `login.tsx` | Session cookie login endpoint |
| `logout.tsx` | Session cookie clear endpoint |
| `session.tsx` | Session check endpoint |

#### Notifications (`components/notifications/` + `hooks/` + `durable-objects/`)
| File | Description |
|------|-------------|
| `NotificationBell.tsx` | Bell icon with unread badge |
| `NotificationPanel.tsx` | Dropdown notification list |
| `useNotifications.ts` | WebSocket + REST notification hook |
| `notification-hub.ts` | Per-user WebSocket broadcast DO |
| `notifications-ws.tsx` | WebSocket upgrade proxy route |

#### Media (`components/media/` + `durable-objects/`)
| File | Description |
|------|-------------|
| `PhotoGallery.tsx` | Grid gallery with lightbox |
| `PhotoUpload.tsx` | Signed-URL upload with progress |
| `upload-manager.ts` | Chunked upload DO with progress relay |

#### Infrastructure (`contexts/` + `hooks/` + `routes/`)
| File | Description |
|------|-------------|
| `GlobalSearchContext.tsx` | Keyed pub/sub search state |
| `useActionToast.ts` | withToast() async action wrapper |
| `tos.tsx` | Versioned TOS consent tracking |
| `settings.tsx` | Protected layout route with auth guard |
| `router.tsx` | Minimal TanStack router factory |

<!-- ACP_AUTO_UPDATE_END:CONTENTS -->

### Template Variables

Some template files use ACP variable substitution:

| Variable | Default | Used In |
|----------|---------|---------|
| `APP_NAME` | `My App` | UnifiedHeader, AuthForm |
| `PRIMARY_COLOR` | `#3B82F6` | WizardShell |
| `AUTH_REDIRECT` | `/home` | AuthForm, settings, tos |

### Required Dependencies

Install these npm packages based on which template files you use:

| Package | Required By |
|---------|-------------|
| `lucide-react` | Most UI components |
| `fuse.js` | PillInput, EntityTable |
| `firebase` | AuthContext, AuthForm |
| `firebase-admin` | login, logout, session routes |
| `@prmichaelsen/pretty-toasts` | useActionToast |

## Why Use This Package

This package provides battle-tested patterns and starter code extracted from production TanStack Start + Cloudflare Workers applications:

- **48 architectural patterns** covering routing, auth, data access, real-time, UI, permissions, integrations, and migration
- **39 starter template files** — production-tested source code you can install directly
- **2 deployment commands** for building and monitoring Cloudflare Workers
- All patterns include code examples, anti-patterns, testing strategies, and implementation checklists
- Designed for AI agents — patterns are explicit, self-documenting, and reference each other

## Usage

After installing, agents will have access to all patterns, commands, and template files:

- Start with **wrangler-configuration** and **api-route-handlers** for project setup
- Install template files with `--files` for instant scaffolding
- Add **auth-session-management** and **library-services** for authenticated data access
- Use **durable-objects-websocket** and **provider-adapter** for real-time features

## Development

### Adding New Content

- Use `@acp.pattern-create` to create patterns
- Use `@acp.command-create` to create commands
- Use `@acp.design-create` to create designs
- Add template files to `agent/files/` and register in `package.yaml` `contents.files`

### Testing

Run `@acp.package-validate` to validate your package locally.

### Publishing

Run `@acp.package-publish` to publish updates.

## Namespace Convention

All files use the `tanstack-cloudflare` namespace:
- Commands: `tanstack-cloudflare.command-name.md`
- Patterns: `tanstack-cloudflare.pattern-name.md`
- Template files: `agent/files/src/...`

## License

MIT

## Author

Patrick Michaelsen
