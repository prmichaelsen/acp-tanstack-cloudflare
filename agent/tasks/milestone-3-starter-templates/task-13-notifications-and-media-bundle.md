# Task 13: Extract Notifications, Media, and Infrastructure Bundle

**Milestone**: M3 — Starter Template Files
**Status**: not_started
**Estimated Hours**: 4
**Dependencies**: Task 9 (uses Modal), Task 11 (uses SlideOverPanel)

---

## Objective

Extract and generalize notification system (DO + components + hooks), media components (gallery + upload), and infrastructure files (router, settings route, consent, contexts).

## Files to Create

| File | Source | Lines | Generalization |
|------|--------|-------|---------------|
| `agent/files/src/durable-objects/notification-hub.ts` | cleanbook DO | 77 | Rename event types to generic |
| `agent/files/src/routes/api/notifications-ws.tsx` | cleanbook route | 39 | Generic service name |
| `agent/files/src/components/notifications/NotificationBell.tsx` | cleanbook component | 65 | Abstract auth check |
| `agent/files/src/components/notifications/NotificationPanel.tsx` | cleanbook component | 165 | Make notification type → icon mapping injectable |
| `agent/files/src/hooks/useNotifications.ts` | cleanbook hook | 135 | Abstract notification engine source |
| `agent/files/src/components/media/PhotoGallery.tsx` | cleanbook component | 150 | Remove Photo schema, use generic `{id, url, alt}` |
| `agent/files/src/components/media/PhotoUpload.tsx` | cleanbook component | 347 | Abstract signed-URL service interface |
| `agent/files/src/durable-objects/upload-manager.ts` | cleanbook DO | 305 | Parameterize MIME types, max size |
| `agent/files/src/routes/api/consent/tos.tsx` | cleanbook route | 83 | Already nearly generic |
| `agent/files/src/routes/settings.tsx` | cleanbook route | 27 | `{{AUTH_REDIRECT}}` for redirect |
| `agent/files/src/routes/router.tsx` | cleanbook router.tsx | 11 | Already generic |
| `agent/files/src/contexts/GlobalSearchContext.tsx` | cleanbook context | 52 | Already generic |
| `agent/files/src/hooks/useActionToast.ts` | cleanbook hook | 35 | Already generic |

## Steps

1. Create all target directories
2. Copy and generalize each file per the table above
3. Ensure notification system files work together (DO ↔ WS route ↔ hook ↔ components)
4. Ensure media files have clean interfaces (no cleanbook Photo schema)
5. Add all `contents.files` entries to `package.yaml`

## Verification

- [ ] All 13 files created
- [ ] Notification system is self-contained and generic
- [ ] Media components use generic interfaces
- [ ] No cleanbook domain references remain
