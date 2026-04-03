# Agam Organization Defaults — Agent Instructions

This file is the agent entrypoint for the `.github` organizational repository.
The canonical shared source of truth lives under `.agent/`.

## Read First

- `.agent/README.md`
- `.agent/include/project-context.md`
- `.agent/include/workflow.md`
- `.agent/phases/current.md`

## Non-Negotiables

- This repository defines the organization-wide defaults for all `agam-lang` repos.
- Changes here affect the entire organization: CI/CD, issue templates, PR templates, and the org profile.
- All reusable workflows live in `.github/workflows/` and are called by other repos via `uses:`.
- The `profile/README.md` is the public face of the organization.
