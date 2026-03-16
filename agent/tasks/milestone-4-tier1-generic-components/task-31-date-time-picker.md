# Task 31: Extract DateTimePicker Component

**Milestone**: M4 — Tier 1 Generic Components
**Status**: not_started
**Estimated Hours**: 1.5
**Dependencies**: None

---

## Objective

Extract and generalize the DateTimePicker component — a self-contained dark-theme datetime picker with calendar (day/month/year drill-down views), scrollable hour/minute columns, past-date disabling, and confirm callback — from agentbase.me into the ACP starter template package.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/datetime-picker/DateTimePicker.tsx`
`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/datetime-picker/index.ts`

## Target

`agent/files/src/components/ui/DateTimePicker.tsx`

## Steps

1. **Read** the source files at `agentbase.me/src/components/datetime-picker/DateTimePicker.tsx` and `index.ts`
2. **Generalize** the component:
   - No `@/` alias imports to remove — component only imports from `react` and `lucide-react`
   - Component is already designed for extraction (source comments say "Designed for extraction into a standalone package — all helpers are co-located, no project-specific imports")
   - Merge into a single file (no need for separate index.ts barrel since target is a single file)
   - Keep `lucide-react` imports (ChevronLeft, ChevronRight, Clock, Calendar, Check) as peer deps
   - No changes needed — copy as-is
3. **Write** the generalized file to `agent/files/src/components/ui/DateTimePicker.tsx`
4. **Update** `package.yaml` `contents.files` with the new file entry

## Verification

- [ ] File created at `agent/files/src/components/ui/DateTimePicker.tsx`
- [ ] No `@/` alias imports
- [ ] No project-specific imports or references
- [ ] `DateTimePicker` component and `DateTimePickerProps` type are exported
- [ ] No TypeScript errors in isolation
- [ ] `package.yaml` updated with file entry
