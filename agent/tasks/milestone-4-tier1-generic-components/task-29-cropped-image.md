# Task 29: Extract CroppedImage Component

**Milestone**: M4 — Tier 1 Generic Components
**Status**: not_started
**Estimated Hours**: 2
**Dependencies**: None

---

## Objective

Extract and generalize the CroppedImage component — a drop-in `<img>` replacement that renders CSS-based cropping with two sizing modes (intrinsic for galleries, fill for avatars/banners), auto-resolves crop data from proxy URL headers with module-level caching and request deduplication — from agentbase.me into the ACP starter template package.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/CroppedImage.tsx`

## Target

`agent/files/src/components/media/CroppedImage.tsx`

## Steps

1. **Read** the source file at `agentbase.me/src/components/CroppedImage.tsx`
2. **Generalize** the component:
   - Remove `import type { CropData } from '@/schemas/widget'` — import CropData from the co-located `./ImageCrop` (which exports it) or define inline
   - The `isProxyUrl` function references `/api/storage/image` (project-specific) — generalize this to be configurable or document as a customization point
   - The `fetchCropFromHeaders` function reads project-specific `X-Crop-*` headers — same treatment as isProxyUrl
   - No other project-specific imports or strings
3. **Write** the generalized file to `agent/files/src/components/media/CroppedImage.tsx`
4. **Update** `package.yaml` `contents.files` with the new file entry

## Verification

- [ ] File created at `agent/files/src/components/media/CroppedImage.tsx`
- [ ] No `@/` alias imports remain
- [ ] CropData imported from local media directory, not from `@/schemas/widget`
- [ ] `isProxyUrl` / `fetchCropFromHeaders` are generalized or documented as customization points
- [ ] No TypeScript errors in isolation
- [ ] `package.yaml` updated with file entry
