# Milestone 3: Starter Template Files

**Status**: not_started
**Started**: null
**Estimated**: 2 weeks
**Tasks**: 7

---

## Goal

Ship production-tested starter template source files alongside existing pattern docs. Files install to consumer projects via `acp install tanstack-cloudflare --files`, landing in their natural `src/` locations ready to use.

## Deliverables

1. `agent/files/` directory with ~35 generalized template files extracted from cleanbook-tanstack
2. `contents.files` entries in `package.yaml` for all template files
3. 5 new pattern docs for net-new patterns (wizard, typeahead, signed-url-upload, tos-consent, chunked-upload-do)
4. Updated README.md documenting template files and their usage

## Success Criteria

- [ ] All template files compile (no cleanbook-specific imports)
- [ ] Every template file maps to a pattern doc
- [ ] `package.yaml` `contents.files` lists all files with descriptions and targets
- [ ] Variable substitution works for `{{APP_NAME}}`, `{{PRIMARY_COLOR}}`, `{{AUTH_REDIRECT}}`
- [ ] README documents installation and cherry-picking of files
- [ ] Package version bumped to 2.0.0 (breaking: new file content type)

## Design Reference

- [Starter Templates Design](../design/starter-templates-design.md)
- [Audit Report](../reports/audit-1-cleanbook-extractable-ux-components.md)
