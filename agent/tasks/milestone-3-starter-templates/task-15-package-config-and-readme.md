# Task 15: Update Package Config, README, and Version

**Milestone**: M3 — Starter Template Files
**Status**: not_started
**Estimated Hours**: 2
**Dependencies**: Tasks 9-14 (all template files and patterns created)

---

## Objective

Finalize package.yaml with all `contents.files` entries, update README with template file documentation and installation instructions, bump version, update CHANGELOG.

## Steps

1. Ensure `package.yaml` `contents.files` has all ~35 file entries with:
   - `name` (path relative to `agent/files/`)
   - `description` (one-line)
   - `target` (where to install, e.g., `src/components/ui/`)
   - `required: false` (all templates are optional)
   - `variables` (where applicable: APP_NAME, PRIMARY_COLOR, AUTH_REDIRECT)
2. Update README.md:
   - Add "Starter Templates" section documenting the file bundles
   - Document `acp install tanstack-cloudflare --files` usage
   - List required npm dependencies per bundle
   - Add cherry-picking examples
3. Bump version to 2.0.0 in package.yaml (new content type = semver major)
4. Update CHANGELOG.md with M3 entry
5. Update progress.yaml: M3 complete, version, counts

## Verification

- [ ] `package.yaml` has complete `contents.files` section
- [ ] README documents all template bundles with install instructions
- [ ] Version bumped to 2.0.0
- [ ] CHANGELOG updated
- [ ] progress.yaml reflects M3 completion
