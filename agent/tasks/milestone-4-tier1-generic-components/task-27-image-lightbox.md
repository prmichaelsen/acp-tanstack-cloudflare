# Task 27: Extract ImageLightbox Component

**Milestone**: M4 — Tier 1 Generic Components
**Status**: not_started
**Estimated Hours**: 2
**Dependencies**: None

---

## Objective

Extract and generalize the ImageLightbox component — a fullscreen image viewer with keyboard/swipe navigation, crop-aware rendering via ScaledCropPreview, adjacent image preloading, and auto-crop resolution from proxy URL headers — from agentbase.me into the ACP starter template package.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/ImageLightbox.tsx`

## Target

`agent/files/src/components/media/ImageLightbox.tsx`

## Steps

1. **Read** the source file at `agentbase.me/src/components/ImageLightbox.tsx`
2. **Generalize** the component:
   - Remove `import type { CropData } from '@/schemas/widget'` — import CropData from the co-located `./ImageCrop` (which exports it) or a shared types file
   - Update `import { LightboxContainer } from './LightboxContainer'` to resolve within the ACP media directory (`./LightboxContainer`)
   - The `isProxyUrl` and `fetchCropFromHeaders` helpers are project-specific (they reference `/api/storage/image` and custom `X-Crop-*` headers) — make these configurable or clearly document them as customization points that consumers should override
   - No other project-specific strings
3. **Write** the generalized file to `agent/files/src/components/media/ImageLightbox.tsx`
4. **Update** `package.yaml` `contents.files` with the new file entry

## Verification

- [ ] File created at `agent/files/src/components/media/ImageLightbox.tsx`
- [ ] No `@/` alias imports remain
- [ ] CropData imported from local media directory, not from `@/schemas/widget`
- [ ] `isProxyUrl` / `fetchCropFromHeaders` are generalized or documented as customization points
- [ ] Relative import to LightboxContainer resolves within media/
- [ ] No TypeScript errors in isolation
- [ ] `package.yaml` updated with file entry
