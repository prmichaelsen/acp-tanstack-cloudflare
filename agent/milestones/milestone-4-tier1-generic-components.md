# Milestone 4: Tier 1 Generic Component Extraction

**Status**: not_started
**Started**: null
**Estimated**: 2 weeks
**Tasks**: 17 (T16-T32)

---

## Goal

Extract 17 fully generic, zero-dependency components from agentbase.me into package template files. These are Tier 1 components identified by audit-2: they have no project-specific imports and are ready to copy into any TanStack/Cloudflare project with ACP variable substitution.

## Deliverables

1. 17 generalized component files in `agent/files/src/components/` (ui/ and modals/ subdirectories)
2. `contents.files` entries in `package.yaml` for all new template files
3. Each component free of agentbase.me-specific imports, styles, or configuration

## Success Criteria

- [ ] All 17 component files created under `agent/files/src/components/`
- [ ] Zero project-specific imports (no agentbase.me paths, no app-specific config)
- [ ] ACP variables (`{{APP_NAME}}`, `{{PRIMARY_COLOR}}`) applied where appropriate
- [ ] Each component compiles standalone with only React + Tailwind + lucide-react dependencies
- [ ] `package.yaml` `contents.files` updated for every new file
- [ ] Internal cross-component imports use relative paths within the template tree

## Design Reference

- [Audit-2 Report](../reports/audit-2-agentbase-extractable-components.md)
- [Milestone 3 (prior art)](./milestone-3-starter-templates.md)
