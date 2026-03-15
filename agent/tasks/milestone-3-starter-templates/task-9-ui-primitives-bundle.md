# Task 9: Extract UI Primitives Bundle

**Milestone**: M3 — Starter Template Files
**Status**: not_started
**Estimated Hours**: 3
**Dependencies**: None

---

## Objective

Extract and generalize 5 core UI primitive components from cleanbook-tanstack into `agent/files/src/components/ui/`.

## Files to Create

| File | Source | Lines | Generalization |
|------|--------|-------|---------------|
| `agent/files/src/components/ui/Modal.tsx` | cleanbook `ui/Modal.tsx` | 201 | None needed — already generic |
| `agent/files/src/components/ui/SlideOverPanel.tsx` | cleanbook `SlideOverPanel.tsx` | 46 | None needed |
| `agent/files/src/components/ui/PillInput.tsx` | cleanbook `ui/PillInput.tsx` | 201 | None needed |
| `agent/files/src/components/ui/Typeahead.tsx` | cleanbook `ui/Typeahead.tsx` | 215 | None needed |
| `agent/files/src/components/ui/SearchBar.tsx` | cleanbook `SearchBar.tsx` | 37 | Replace GlobalSearchContext import path |

## Steps

1. Create `agent/files/src/components/ui/` directory
2. Copy each file from cleanbook-tanstack, removing any cleanbook-specific imports
3. Ensure all imports reference relative paths (not cleanbook aliases)
4. Verify no domain-specific strings remain
5. Add `contents.files` entries to `package.yaml` for each file

## Verification

- [ ] All 5 files created in `agent/files/src/components/ui/`
- [ ] No cleanbook-specific imports or references
- [ ] No TypeScript errors in isolation (correct relative imports)
- [ ] `package.yaml` updated with 5 file entries
