# Task 16: Extract Button Component

**Milestone**: M4 — Tier 1 Generic Component Extraction
**Status**: not_started
**Estimated Hours**: 1
**Dependencies**: none

---

## Objective

Extract the Button component from agentbase.me and generalize it as a reusable UI primitive with variant/size support and gradient styling.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/Button.tsx` (~77 lines)

## Target

`agent/files/src/components/ui/Button.tsx`

## Steps

1. **Read source** — Review Button.tsx from agentbase.me
2. **Generalize** — Specific changes needed:
   - No project-specific imports to remove (already generic)
   - Verify gradient color tokens are not agentbase.me-branded; replace any app-specific colors with `{{PRIMARY_COLOR}}` CSS variable references if needed
   - Ensure only React types are imported (no external deps)
3. **Write to target** — Place in `agent/files/src/components/ui/Button.tsx`
4. **Update package.yaml** — Add `contents.files` entry with description and target path

## Component Summary

Multi-variant button (primary, secondary, danger, success, ghost) with three sizes (sm, md, lg). Supports icons, full-width mode, and disabled state. Uses Tailwind gradient classes. Zero external dependencies beyond React.

## Verification

- [ ] File created at `agent/files/src/components/ui/Button.tsx`
- [ ] No agentbase.me-specific imports remain
- [ ] Exports `Button`, `ButtonVariant`, `ButtonSize` types
- [ ] `package.yaml` updated with new entry
