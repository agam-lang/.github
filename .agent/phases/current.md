# Current Development

## Active Workstreams

1. **Reusable Workflow Library**
   - Status: active
   - Hosts rust-ci, node-ci, markdown-lint, benchmarks, sdk-dist as reusable workflows
   - All other repos call these via `uses: agam-lang/.github/.github/workflows/...@main`

2. **Organization Profile**
   - Status: active
   - `profile/README.md` is the public landing page at github.com/agam-lang

3. **Automation Workflows**
   - Status: active
   - auto-assign.yml and add-to-project.yml are org-wide

## Decision Rules

- Test workflow changes on a feature branch before merging to main.
- Do not break other repos' CI by changing reusable workflow interfaces.
