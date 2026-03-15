# Task 10: Extract Data Display Bundle

**Milestone**: M3 — Starter Template Files
**Status**: not_started
**Estimated Hours**: 4
**Dependencies**: Task 9 (uses Modal from UI primitives)

---

## Objective

Extract and generalize 8 data display components from cleanbook-tanstack into `agent/files/src/components/data/`.

## Files to Create

| File | Source | Lines | Generalization |
|------|--------|-------|---------------|
| `agent/files/src/components/data/SortableTable.tsx` | cleanbook `ui/SortableTable.tsx` | 150 | None needed |
| `agent/files/src/components/data/MobileCardList.tsx` | cleanbook `ui/MobileCardList.tsx` | 150 | None needed |
| `agent/files/src/components/data/useSortableData.ts` | cleanbook `ui/useSortableData.ts` | 89 | None needed |
| `agent/files/src/components/data/ColumnFilter.tsx` | cleanbook `entity-table/ColumnFilter.tsx` | 82 | None needed |
| `agent/files/src/components/data/SortIndicator.tsx` | cleanbook `entity-table/SortIndicator.tsx` | 11 | None needed |
| `agent/files/src/components/data/EntityTable.tsx` | cleanbook `entity-table/EntityTable.tsx` | 339 | Remove i18n `useT()`, make entity config injectable |
| `agent/files/src/components/data/Paginator.tsx` | cleanbook `Paginator.tsx` | 161 | None needed |
| `agent/files/src/components/data/PaginationToggle.tsx` | cleanbook `PaginationToggle.tsx` | 76 | None needed |
| `agent/files/src/components/data/PaginationSlideOver.tsx` | cleanbook `PaginationSlideOver.tsx` | 79 | Update import paths |

## Steps

1. Create `agent/files/src/components/data/` directory
2. Copy each file, updating internal import paths to reference sibling files
3. Generalize EntityTable: remove i18n dependency, make entity config a prop
4. Ensure SortableTable/MobileCardList share column config types
5. Add `contents.files` entries to `package.yaml`

## Verification

- [ ] All 8+1 files created
- [ ] Internal imports resolve correctly between data/ files
- [ ] EntityTable no longer depends on i18n or entity-config registry
- [ ] `package.yaml` updated
