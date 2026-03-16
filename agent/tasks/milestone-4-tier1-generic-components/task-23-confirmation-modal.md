# Task 23: Extract ConfirmationModal Component

**Milestone**: M4 — Tier 1 Generic Component Extraction
**Status**: not_started
**Estimated Hours**: 1.5
**Dependencies**: none

---

## Objective

Extract the ConfirmationModal component from agentbase.me — a confirm/cancel dialog with variant-based icon and button styling (danger, warning, info), built on top of a generic Modal component.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/modals/ConfirmationModal.tsx` (~105 lines)

## Target

`agent/files/src/components/modals/ConfirmationModal.tsx`

## Steps

1. **Read source** — Review ConfirmationModal.tsx from agentbase.me
2. **Generalize** — Specific changes needed:
   - Imports `Modal` from `./Modal` — verify that a generic Modal component exists in the template tree (from M3 or earlier tasks); if not, this task must also extract or stub the Modal dependency
   - No other project-specific imports
   - Three variants (danger, warning, info) use gradient icon backgrounds and gradient buttons — all use standard Tailwind colors
   - SVG icon paths are inline (no external icon library needed)
   - Supports dark mode via `dark:` Tailwind prefixes — already generic
3. **Write to target** — Place in `agent/files/src/components/modals/ConfirmationModal.tsx`
4. **Update package.yaml** — Add `contents.files` entry with description and target path

## Component Summary

Confirmation dialog with three visual variants (danger, warning, info). Each variant renders a different gradient icon circle and matching confirm button. Supports custom confirm/cancel text, loading state with "Processing..." text, and prevents close during loading. Built on a `Modal` wrapper component. Dependencies: React, sibling Modal component.

## Verification

- [ ] File created at `agent/files/src/components/modals/ConfirmationModal.tsx`
- [ ] No agentbase.me-specific imports remain
- [ ] Import path to `Modal` resolves within the template tree
- [ ] Exports `ConfirmationModal` component
- [ ] All three variants (danger, warning, info) have correct styling
- [ ] `package.yaml` updated with new entry
