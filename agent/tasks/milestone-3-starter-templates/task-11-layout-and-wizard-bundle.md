# Task 11: Extract Layout Shell + Wizard Bundle

**Milestone**: M3 — Starter Template Files
**Status**: not_started
**Estimated Hours**: 3
**Dependencies**: None

---

## Objective

Extract and generalize 5 layout components + 2 wizard files from cleanbook-tanstack. These require variable substitution for brand name, colors, and nav items.

## Files to Create

| File | Source | Lines | Generalization |
|------|--------|-------|---------------|
| `agent/files/src/components/layout/UnifiedHeader.tsx` | cleanbook `UnifiedHeader.tsx` | 147 | `{{APP_NAME}}` for brand, parameterize nav routes |
| `agent/files/src/components/layout/UnifiedFooter.tsx` | cleanbook `UnifiedFooter.tsx` | 17 | None needed |
| `agent/files/src/components/layout/Sidebar.tsx` | cleanbook `Sidebar.tsx` | 49 | Make `NAV_ITEMS` a config array prop |
| `agent/files/src/components/layout/MobileBottomNav.tsx` | cleanbook `MobileBottomNav.tsx` | 64 | Make nav items a config prop |
| `agent/files/src/components/layout/MenuDropdown.tsx` | cleanbook `MenuDropdown.tsx` | 68 | Make menu items a config prop |
| `agent/files/src/components/wizard/WizardShell.tsx` | cleanbook `onboarding/WizardShell.tsx` | 84 | `{{PRIMARY_COLOR}}` for gradient |
| `agent/files/src/hooks/useWizardState.ts` | cleanbook `hooks/useWizardState.ts` | 146 | None needed — already generic |

## Steps

1. Create `agent/files/src/components/layout/` and `wizard/` directories
2. Copy layout files, replacing hardcoded nav items with config-driven props
3. Replace "Cleanbook" with `{{APP_NAME}}` in UnifiedHeader
4. Replace gradient colors with `{{PRIMARY_COLOR}}` in WizardShell
5. Copy useWizardState as-is (already fully generic)
6. Add `contents.files` entries with `variables` for APP_NAME, PRIMARY_COLOR

## Verification

- [ ] All 7 files created
- [ ] `{{APP_NAME}}` and `{{PRIMARY_COLOR}}` placeholders present
- [ ] Nav items are config-driven (not hardcoded to cleanbook routes)
- [ ] `package.yaml` updated with variable declarations
