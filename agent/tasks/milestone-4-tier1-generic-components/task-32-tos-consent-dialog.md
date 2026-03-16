# Task 32: Extract TosConsentDialog Component

**Milestone**: M4 — Tier 1 Generic Components
**Status**: not_started
**Estimated Hours**: 2
**Dependencies**: None

---

## Objective

Extract and generalize the TosConsentDialog component — a persistent modal requiring users to scroll through and accept Terms of Service, with scroll-gating on the agree button and a logout option — from agentbase.me into the ACP starter template package.

## Source

`/home/prmichaelsen/.acp/projects/agentbase.me/src/components/TosConsentDialog.tsx`

## Target

`agent/files/src/components/ui/TosConsentDialog.tsx`

## Steps

1. **Read** the source file at `agentbase.me/src/components/TosConsentDialog.tsx`
2. **Generalize** the component — significant changes needed:
   - Remove `import { Modal } from '@/components/modals/Modal'` — replace with relative import to ACP Modal (`../modals/Modal` or `./Modal` depending on final layout)
   - Remove `import { Button } from '@/components/Button'` — replace with relative import or inline button styling
   - Remove `import { TermsOfServiceContent } from '@/components/TermsOfServiceContent'` — replace with a `children` or `content` prop so consumers supply their own ToS content
   - Remove `import { useTosConsent } from '@/contexts/TosConsentContext'` — extract `isOpen`, `onAccept`, and `loading` as props instead of reading from a project-specific context
   - Remove `import { useAuth } from '@/components/auth/AuthContext'` — remove auth dependency; let the consumer control visibility via the `isOpen` prop
   - Remove `import { logout } from '@/lib/firebase-client'` — accept `onLogout` or `onDecline` as a prop instead
   - Remove hardcoded `/api/auth/logout` fetch call — handled by onLogout prop
   - Make the component accept props: `isOpen`, `onAccept`, `onDecline`, `loading`, `children` (ToS content), and optional `title`
3. **Write** the generalized file to `agent/files/src/components/ui/TosConsentDialog.tsx`
4. **Update** `package.yaml` `contents.files` with the new file entry

## Verification

- [ ] File created at `agent/files/src/components/ui/TosConsentDialog.tsx`
- [ ] No `@/` alias imports remain
- [ ] No Firebase, auth context, or ToS context imports
- [ ] Component accepts generic props instead of reading from project-specific contexts
- [ ] ToS content is supplied via children/render prop, not hardcoded
- [ ] Scroll-gating behavior preserved (agree button disabled until scrolled to bottom)
- [ ] No TypeScript errors in isolation
- [ ] `package.yaml` updated with file entry
