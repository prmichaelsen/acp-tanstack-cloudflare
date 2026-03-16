# Task 28: Extract LightboxContainer Component

**Milestone**: M4 — Tier 1 Generic Components
**Status**: not_started
**Estimated Hours**: 2
**Dependencies**: None

---

## Objective

Extract and generalize the LightboxContainer component — a shared fullscreen lightbox shell providing portal rendering, backdrop with blur, body scroll lock, keyboard navigation (Escape/Arrow keys), touch swipe (horizontal nav + vertical dismiss), slide animation, prev/next chevrons, counter badge, and configurable nav-disabled mode — from agentbase.me into the ACP starter template package.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/LightboxContainer.tsx`

## Target

`agent/files/src/components/media/LightboxContainer.tsx`

## Steps

1. **Read** the source file at `agentbase.me/src/components/LightboxContainer.tsx`
2. **Generalize** the component:
   - No `@/` alias imports to remove (component only imports from `react`, `react-dom`, and `lucide-react`)
   - Component is already fully generic with no project-specific references
   - Keep `lucide-react` imports (ChevronLeft, ChevronRight, X) as peer dependencies
   - No changes needed — copy as-is
3. **Write** the generalized file to `agent/files/src/components/media/LightboxContainer.tsx`
4. **Update** `package.yaml` `contents.files` with the new file entry

## Verification

- [ ] File created at `agent/files/src/components/media/LightboxContainer.tsx`
- [ ] No `@/` alias imports
- [ ] No project-specific imports or references
- [ ] No TypeScript errors in isolation
- [ ] `package.yaml` updated with file entry
