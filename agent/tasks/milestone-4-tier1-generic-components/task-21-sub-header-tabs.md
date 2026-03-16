# Task 21: Extract SubHeaderTabs Component

**Milestone**: M4 — Tier 1 Generic Component Extraction
**Status**: not_started
**Estimated Hours**: 1
**Dependencies**: none

---

## Objective

Extract the SubHeaderTabs component from agentbase.me — a horizontally scrollable tab bar with bottom-border active indicator and ghost variant support.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/SubHeaderTabs.tsx` (~60 lines)

## Target

`agent/files/src/components/ui/SubHeaderTabs.tsx`

## Steps

1. **Read source** — Review SubHeaderTabs.tsx from agentbase.me
2. **Generalize** — Specific changes needed:
   - No project-specific imports to remove (uses only React types)
   - Uses inline `<style>` tag to hide webkit scrollbar — keep as-is, it targets a generic class
   - Active indicator uses `border-purple-500` — keep as default or note for `{{PRIMARY_COLOR}}` substitution
   - Tab data structure (`SubHeaderTab`) supports icon ReactNode and ghost variant — already generic
3. **Write to target** — Place in `agent/files/src/components/ui/SubHeaderTabs.tsx`
4. **Update package.yaml** — Add `contents.files` entry with description and target path

## Component Summary

Horizontal tab bar with overflow scroll, hidden scrollbar, and bottom-border active indicator. Each tab can have an icon and a "ghost" variant for secondary styling. Uses a controlled `activeId` / `onSelect` pattern. Zero external dependencies beyond React.

## Verification

- [ ] File created at `agent/files/src/components/ui/SubHeaderTabs.tsx`
- [ ] No agentbase.me-specific imports remain
- [ ] Exports `SubHeaderTabs`, `SubHeaderTab` types
- [ ] Horizontal scroll with hidden scrollbar works
- [ ] `package.yaml` updated with new entry
