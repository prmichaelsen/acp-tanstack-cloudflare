# Task 19: Extract ToggleSwitch Component

**Milestone**: M4 — Tier 1 Generic Component Extraction
**Status**: not_started
**Estimated Hours**: 1
**Dependencies**: none

---

## Objective

Extract the ToggleSwitch component from agentbase.me — an iOS-style toggle with three sizes, gradient track, animated checkmark knob, and optional label/description.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/ToggleSwitch.tsx` (~171 lines)

## Target

`agent/files/src/components/ui/ToggleSwitch.tsx`

## Steps

1. **Read source** — Review ToggleSwitch.tsx from agentbase.me
2. **Generalize** — Specific changes needed:
   - No project-specific imports to remove (uses only React types)
   - Purple-to-blue gradient on the track (`from-purple-600 to-blue-600`) is a design choice — keep as default or parameterize via `{{PRIMARY_COLOR}}` if appropriate
   - SVG checkmark gradient uses hardcoded `#9333ea` / `#2563eb` — consider making these match the track gradient
   - Ensure proper ARIA attributes are preserved (role="switch", aria-checked)
3. **Write to target** — Place in `agent/files/src/components/ui/ToggleSwitch.tsx`
4. **Update package.yaml** — Add `contents.files` entry with description and target path

## Component Summary

iOS-style toggle switch with sm/md/lg sizes. Features a gradient-filled track when checked, a white knob with an animated checkmark SVG, keyboard support (Space/Enter), and optional label + description layout. Accessible with proper ARIA role and state. Zero external dependencies beyond React.

## Verification

- [ ] File created at `agent/files/src/components/ui/ToggleSwitch.tsx`
- [ ] No agentbase.me-specific imports remain
- [ ] Exports `ToggleSwitch`, `ToggleSwitchSize` types
- [ ] ARIA attributes preserved (role="switch", aria-checked)
- [ ] `package.yaml` updated with new entry
