# Task 18: Extract Popover Component

**Milestone**: M4 — Tier 1 Generic Component Extraction
**Status**: not_started
**Estimated Hours**: 1.5
**Dependencies**: none

---

## Objective

Extract the Popover component from agentbase.me — a portal-based popover with viewport-aware positioning, click-outside dismissal, and escape key handling.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/Popover.tsx` (~117 lines)

## Target

`agent/files/src/components/ui/Popover.tsx`

## Steps

1. **Read source** — Review Popover.tsx from agentbase.me
2. **Generalize** — Specific changes needed:
   - No project-specific imports to remove (uses only React and react-dom)
   - Default className uses `bg-gray-800 border-gray-700` — keep as generic dark-mode defaults
   - Verify no app-specific z-index conflicts (currently uses z-50)
3. **Write to target** — Place in `agent/files/src/components/ui/Popover.tsx`
4. **Update package.yaml** — Add `contents.files` entry with description and target path

## Component Summary

Renders children into a portal anchored to a ref element. Supports `above` and `below` positioning with automatic flip when viewport space is insufficient. Handles click-outside, touch-outside, and Escape key dismissal. Uses `createPortal` for rendering. Zero external dependencies beyond React/ReactDOM.

## Verification

- [ ] File created at `agent/files/src/components/ui/Popover.tsx`
- [ ] No agentbase.me-specific imports remain
- [ ] Exports `Popover` component
- [ ] Viewport clamping logic preserved
- [ ] `package.yaml` updated with new entry
