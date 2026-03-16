# Task 25: Extract ImageCarousel Component

**Milestone**: M4 — Tier 1 Generic Components
**Status**: not_started
**Estimated Hours**: 2
**Dependencies**: None

---

## Objective

Extract and generalize the ImageCarousel component — a snap-scroll carousel with IntersectionObserver-based tracking, per-slide scaling/opacity animations, dot/counter navigation, keyboard support, and integrated lightbox — from agentbase.me into the ACP starter template package.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/ImageCarousel.tsx`

## Target

`agent/files/src/components/media/ImageCarousel.tsx`

## Steps

1. **Read** the source file at `agentbase.me/src/components/ImageCarousel.tsx`
2. **Generalize** the component:
   - Remove `import type { CropData } from '@/schemas/widget'` — inline the `CropData` type definition or import from a co-located types file within the media directory
   - Update `import { ImageLightbox } from './ImageLightbox'` to resolve within the ACP media directory (`./ImageLightbox`)
   - Update `import { CroppedImage } from './CroppedImage'` to resolve within the ACP media directory (`./CroppedImage`)
   - Keep `lucide-react` imports as-is (peer dependency)
   - No project-specific strings or API references to remove
3. **Write** the generalized file to `agent/files/src/components/media/ImageCarousel.tsx`
4. **Update** `package.yaml` `contents.files` with the new file entry

## Verification

- [ ] File created at `agent/files/src/components/media/ImageCarousel.tsx`
- [ ] No `@/` alias imports remain
- [ ] CropData type is self-contained or imported from a local types file
- [ ] Relative imports to ImageLightbox and CroppedImage resolve within media/
- [ ] No TypeScript errors in isolation
- [ ] `package.yaml` updated with file entry
