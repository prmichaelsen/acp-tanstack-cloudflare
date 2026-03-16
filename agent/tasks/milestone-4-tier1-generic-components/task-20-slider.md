# Task 20: Extract Slider Component

**Milestone**: M4 — Tier 1 Generic Component Extraction
**Status**: not_started
**Estimated Hours**: 1
**Dependencies**: none

---

## Objective

Extract the Slider component from agentbase.me — a range slider supporting both continuous and discrete modes with gradient fill styling.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/Slider.tsx` (~104 lines)

## Target

`agent/files/src/components/ui/Slider.tsx`

## Steps

1. **Read source** — Review Slider.tsx from agentbase.me
2. **Generalize** — Specific changes needed:
   - No project-specific imports to remove (uses only React types)
   - References a global CSS class `slider-styled` from the app's styles.css — document this dependency or inline the necessary CSS as a comment
   - Gradient fill uses hardcoded `#3b82f6` (blue-500) and `#8b5cf6` (violet-500) — keep as sensible defaults
   - Generic type parameter `<T extends number | string>` for discrete mode is already well-abstracted
3. **Write to target** — Place in `agent/files/src/components/ui/Slider.tsx`
4. **Update package.yaml** — Add `contents.files` entry with description and target path

## Component Summary

Dual-mode range slider: continuous (min/max/step) and discrete (options array with type-safe generic). Uses inline gradient background style for the fill effect. Discrete mode supports custom label formatting. Requires a `slider-styled` CSS class for thumb/track styling. Zero external dependencies beyond React.

## Verification

- [ ] File created at `agent/files/src/components/ui/Slider.tsx`
- [ ] No agentbase.me-specific imports remain
- [ ] Exports `Slider`, `SliderProps` types
- [ ] CSS dependency on `slider-styled` class is documented
- [ ] `package.yaml` updated with new entry
