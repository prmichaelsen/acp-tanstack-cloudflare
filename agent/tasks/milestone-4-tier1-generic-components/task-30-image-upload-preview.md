# Task 30: Extract ImageUploadPreview Component

**Milestone**: M4 — Tier 1 Generic Components
**Status**: not_started
**Estimated Hours**: 1.5
**Dependencies**: None

---

## Objective

Extract and generalize the ImageUploadPreview component — a reusable image upload preview with circular progress indicator, moderation spinner (Bot icon), success checkmark, error retry overlay, remove button, and configurable size/shape variants — from agentbase.me into the ACP starter template package.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/ImageUploadPreview.tsx`

## Target

`agent/files/src/components/media/ImageUploadPreview.tsx`

## Steps

1. **Read** the source file at `agentbase.me/src/components/ImageUploadPreview.tsx`
2. **Generalize** the component:
   - No `@/` alias imports to remove (component only imports from `lucide-react`)
   - Component is already fully generic — uses `X`, `RefreshCw`, `Bot` from lucide-react as peer deps
   - No project-specific strings, API calls, or domain references
   - No changes needed — copy as-is
3. **Write** the generalized file to `agent/files/src/components/media/ImageUploadPreview.tsx`
4. **Update** `package.yaml` `contents.files` with the new file entry

## Verification

- [ ] File created at `agent/files/src/components/media/ImageUploadPreview.tsx`
- [ ] No `@/` alias imports
- [ ] No project-specific imports or references
- [ ] No TypeScript errors in isolation
- [ ] `package.yaml` updated with file entry
