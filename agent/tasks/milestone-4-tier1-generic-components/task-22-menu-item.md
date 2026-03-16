# Task 22: Extract MenuItem Component

**Milestone**: M4 — Tier 1 Generic Component Extraction
**Status**: not_started
**Estimated Hours**: 1
**Dependencies**: none

---

## Objective

Extract the MenuItem component from agentbase.me — a reusable menu row with icon, label, loading spinner, danger variant, and optional suffix element.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/MenuItem.tsx` (~29 lines)

## Target

`agent/files/src/components/ui/MenuItem.tsx`

## Steps

1. **Read source** — Review MenuItem.tsx from agentbase.me
2. **Generalize** — Specific changes needed:
   - Imports `LucideIcon` type and `Loader2` from `lucide-react` — keep as-is since lucide-react is a standard dependency
   - No project-specific imports to remove
   - Color tokens are generic Tailwind (gray-300, red-400, gray-800) — no changes needed
   - The `icon` prop uses `LucideIcon` type — this couples to lucide-react; keep since it is a standard icon library
3. **Write to target** — Place in `agent/files/src/components/ui/MenuItem.tsx`
4. **Update package.yaml** — Add `contents.files` entry with description and target path

## Component Summary

Compact menu item button with a lucide icon, text label, and optional suffix. Supports danger styling (red text), loading state (spinner replaces icon), and disabled state. Designed for dropdown menus, sidebars, or action lists. Dependencies: React, lucide-react.

## Verification

- [ ] File created at `agent/files/src/components/ui/MenuItem.tsx`
- [ ] No agentbase.me-specific imports remain
- [ ] Exports `MenuItem` component
- [ ] Loading state shows Loader2 spinner
- [ ] `package.yaml` updated with new entry
