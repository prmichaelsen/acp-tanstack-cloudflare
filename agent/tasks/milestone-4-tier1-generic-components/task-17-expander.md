# Task 17: Extract Expander Component

**Milestone**: M4 — Tier 1 Generic Component Extraction
**Status**: not_started
**Estimated Hours**: 2
**Dependencies**: none

---

## Objective

Extract the Expander component from agentbase.me — a multi-variant collapsible/accordion with 10 visual styles and a built-in collapse animation hook.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/Expander.tsx` (~287 lines)

## Target

`agent/files/src/components/ui/Expander.tsx`

## Steps

1. **Read source** — Review Expander.tsx from agentbase.me
2. **Generalize** — Specific changes needed:
   - Imports `lucide-react` icons (ChevronDown, Plus, Minus, ArrowRight, Sparkles, Zap, Layers, Eye, EyeOff, CornerDownRight) — keep as-is since lucide-react is a standard dependency
   - No project-specific imports to remove
   - Verify all 10 variant color tokens are generic Tailwind colors (blue, green, purple, amber, etc.) — no app-specific branding
   - The internal `useCollapse` hook is self-contained; keep inline
3. **Write to target** — Place in `agent/files/src/components/ui/Expander.tsx`
4. **Update package.yaml** — Add `contents.files` entry with description and target path

## Component Summary

Collapsible section with 10 visual variants: gradient-glow, neon-accent, glass-float, slide-arrow, border-sweep, stacked-lift, visibility, thread, highlight, segmented. Includes a `useCollapse` hook for smooth height animation. Each variant uses different icons and visual treatments. Dependencies: React, lucide-react.

## Verification

- [ ] File created at `agent/files/src/components/ui/Expander.tsx`
- [ ] No agentbase.me-specific imports remain
- [ ] Exports `Expander`, `ExpanderVariant`, `ExpanderProps`, `EXPANDER_VARIANTS`
- [ ] All 10 variants render correctly
- [ ] `package.yaml` updated with new entry
