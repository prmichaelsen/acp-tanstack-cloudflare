# ACP Package: tanstack-cloudflare

TanStack + Cloudflare patterns and utilities for ACP projects

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

### Patterns

#### Core Architecture
- **[library-services](agent/patterns/tanstack-cloudflare.library-services.md)** - Service layer architecture for data access operations with database and API service separation
- **[api-route-handlers](agent/patterns/tanstack-cloudflare.api-route-handlers.md)** - TanStack Start API route pattern with auth, validation, and consistent error handling
- **[ssr-preload](agent/patterns/tanstack-cloudflare.ssr-preload.md)** - Server-side data preloading using TanStack Router's beforeLoad to eliminate loading states
- **[zod-schema-validation](agent/patterns/tanstack-cloudflare.zod-schema-validation.md)** - Centralized Zod schemas as single source of truth for data models and TypeScript types

#### Cloudflare Infrastructure
- **[durable-objects-websocket](agent/patterns/tanstack-cloudflare.durable-objects-websocket.md)** - Durable Objects as WebSocket servers with dependency injection for real-time features
- **[wrangler-configuration](agent/patterns/tanstack-cloudflare.wrangler-configuration.md)** - Complete wrangler.toml setup for TanStack Start with DO bindings, rate limiters, and migrations
- **[rate-limiting](agent/patterns/tanstack-cloudflare.rate-limiting.md)** - Cloudflare rate limiting with separate tiers for auth, API, and WebSocket endpoints

#### Security & Auth
- **[auth-session-management](agent/patterns/tanstack-cloudflare.auth-session-management.md)** - Cookie-based session management with Firebase Admin SDK and universal getAuthSession()
- **[user-scoped-collections](agent/patterns/tanstack-cloudflare.user-scoped-collections.md)** - Firestore subcollection pattern for user-specific data isolation and security
- **[acl-permissions](agent/patterns/tanstack-cloudflare.acl-permissions.md)** - Fine-grained flag-based permission model with authority hierarchy for multi-user features

#### Integrations
- **[third-party-api-integration](agent/patterns/tanstack-cloudflare.third-party-api-integration.md)** - Modular architecture for wrapping external APIs (Guesty, Stripe, Algolia, etc.)
- **[email-service](agent/patterns/tanstack-cloudflare.email-service.md)** - Lightweight transactional email service with HTML templates (Mandrill, SendGrid, Resend)
- **[scheduled-tasks](agent/patterns/tanstack-cloudflare.scheduled-tasks.md)** - Cloudflare Cron Triggers for periodic background tasks (digests, reminders, token refresh)

#### Advanced Patterns
- **[provider-adapter](agent/patterns/tanstack-cloudflare.provider-adapter.md)** - Pluggable provider architecture with interfaces for AI, storage, MCP, and vision backends
- **[confirmation-tokens](agent/patterns/tanstack-cloudflare.confirmation-tokens.md)** - Two-step confirmation flow for AI-initiated mutations with single-use tokens

#### Migration
- **[nextjs-to-tanstack-routing](agent/patterns/tanstack-cloudflare.nextjs-to-tanstack-routing.md)** - Side-by-side mapping of Next.js App Router conventions to TanStack Start equivalents

### Designs

(No designs yet - use @acp.design-create to add designs)
<!-- ACP_AUTO_UPDATE_END:CONTENTS -->

## Why Use This Package

This package provides battle-tested patterns extracted from a production TanStack Start + Cloudflare Workers application. It covers the full stack:

- **16 architectural patterns** covering routing, auth, data access, real-time, permissions, integrations, and migration
- **2 deployment commands** for building and monitoring Cloudflare Workers
- All patterns include code examples, anti-patterns, testing strategies, and implementation checklists
- Designed for AI agents — patterns are explicit, self-documenting, and reference each other

## Usage

After installing, agents will have access to all patterns and commands. Reference them when building TanStack Start + Cloudflare applications:

- Start with **wrangler-configuration** and **api-route-handlers** for project setup
- Add **auth-session-management** and **library-services** for authenticated data access
- Use **durable-objects-websocket** and **provider-adapter** for real-time features
- Apply **acl-permissions** and **confirmation-tokens** for multi-user authorization

## Development

### Setup

1. Clone this repository
2. Make changes
3. Run `@acp.package-validate` to validate
4. Run `@acp.package-publish` to publish

### Adding New Content

- Use `@acp.pattern-create` to create patterns
- Use `@acp.command-create` to create commands
- Use `@acp.design-create` to create designs

These commands automatically:
- Add namespace prefix to filenames
- Update package.yaml contents section
- Update this README.md

### Testing

Run `@acp.package-validate` to validate your package locally.

### Publishing

Run `@acp.package-publish` to publish updates. This will:
- Validate the package
- Detect version bump from commits
- Update CHANGELOG.md
- Create git tag
- Push to remote
- Test installation

## Namespace Convention

All files in this package use the `tanstack-cloudflare` namespace:
- Commands: `tanstack-cloudflare.command-name.md`
- Patterns: `tanstack-cloudflare.pattern-name.md`
- Designs: `tanstack-cloudflare.design-name.md`

## Dependencies

(List any required packages or project dependencies here)

## Contributing

Contributions are welcome! Please:

1. Follow the existing pattern structure
2. Use entity creation commands (@acp.pattern-create, etc.)
3. Run @acp.package-validate before committing
4. Document your changes in CHANGELOG.md
5. Test installation before submitting

## License

MIT

## Author

Patrick Michaelsen
