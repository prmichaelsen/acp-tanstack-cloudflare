# Task 12: Extract Firebase Auth Bundle

**Milestone**: M3 — Starter Template Files
**Status**: not_started
**Estimated Hours**: 3
**Dependencies**: None

---

## Objective

Extract and generalize 5 Firebase auth files (2 components + 3 API routes) into template files. These form a complete Firebase session-cookie auth flow for TanStack Start + Cloudflare Workers.

## Files to Create

| File | Source | Lines | Generalization |
|------|--------|-------|---------------|
| `agent/files/src/components/auth/AuthContext.tsx` | cleanbook `auth/AuthContext.tsx` | 61 | Remove cleanbook service import, use generic service interface |
| `agent/files/src/components/auth/AuthForm.tsx` | cleanbook `auth/AuthForm.tsx` | 270 | `{{APP_NAME}}` for branding, `{{AUTH_REDIRECT}}` for post-login path |
| `agent/files/src/routes/api/auth/login.tsx` | cleanbook `api/auth/login.tsx` | 46 | Already generic |
| `agent/files/src/routes/api/auth/logout.tsx` | cleanbook `api/auth/logout.tsx` | 21 | Already generic |
| `agent/files/src/routes/api/auth/session.tsx` | cleanbook `api/auth/session.tsx` | 30 | Already generic |

## Steps

1. Create `agent/files/src/components/auth/` and `agent/files/src/routes/api/auth/` directories
2. Copy API routes as-is (already generic Firebase session cookie endpoints)
3. Generalize AuthContext: define a generic `AuthService` interface, remove cleanbook-specific service
4. Generalize AuthForm: replace brand references with `{{APP_NAME}}`, redirect with `{{AUTH_REDIRECT}}`
5. Add `contents.files` entries with variables

## Verification

- [ ] All 5 files created
- [ ] No cleanbook-specific service imports
- [ ] `{{APP_NAME}}` and `{{AUTH_REDIRECT}}` placeholders work
- [ ] Auth flow is self-contained (context + form + 3 API routes)
