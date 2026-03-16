# Task 26: Extract ImageCrop Component

**Milestone**: M4 — Tier 1 Generic Components
**Status**: not_started
**Estimated Hours**: 2
**Dependencies**: None

---

## Objective

Extract and generalize the ImageCrop component — an interactive image cropper with drag handles for edge cropping (N/S/E/W) and proportional resize (SE corner), touch support, and display scaling — from agentbase.me into the ACP starter template package.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/ImageCrop.tsx`

## Target

`agent/files/src/components/media/ImageCrop.tsx`

## Steps

1. **Read** the source file at `agentbase.me/src/components/ImageCrop.tsx`
2. **Generalize** the component:
   - The source already defines and exports its own `CropData` interface inline — keep this as the canonical definition for the media directory
   - Also exports `cropDataFromDimensions` helper — retain this export
   - No `@/` alias imports to remove (component is already self-contained)
   - No project-specific imports or references
3. **Write** the generalized file to `agent/files/src/components/media/ImageCrop.tsx`
4. **Update** `package.yaml` `contents.files` with the new file entry

## Verification

- [ ] File created at `agent/files/src/components/media/ImageCrop.tsx`
- [ ] `CropData` interface and `cropDataFromDimensions` are exported
- [ ] No `@/` alias imports remain
- [ ] No project-specific imports or references
- [ ] No TypeScript errors in isolation
- [ ] `package.yaml` updated with file entry
