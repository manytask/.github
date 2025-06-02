# .github

Community health files for the @manytask organization.

- [Code of Conduct](./CODE_OF_CONDUCT.md)
- [Contributing Guide](./CONTRIBUTING.md)
- [Issue Templates](./ISSUE_TEMPLATE)

Also, [organization profile README.md](./profile/README.md) is available.


## Reusable Workflows

`.github/workflows` directory contains GitHub Actions workflows that can be **re-used** in multiple repositories.  
The following reusable workflows are available:
- `reusable-validate-pr.yml` - checks pull request title for compliance with [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) format and PR labels.
- `reusable-update-changelog-version.yml` - updates `CHANGELOG.md` and `VERSION` files on release (move exising tag).

This folder contains only `on: workflow_call:` jobs, so nothing will be executed automatically.
To use a workflow from this folder, you need to call it from another workflow in your repository.
```yaml
jobs:
  call-workflow-passing-data:
    uses: manytask/.github/.github/workflows/reusable-workflow.yml@main
    with:
      config-path: .github/labeler.yml
    secrets:
      envPAT: ${{ secrets.envPAT }}
    permissions:
      contents: read
```

## Action Configs

`.github` directory contains GitHub Actions configurations that can be **re-used** in multiple repositories.
- `release-drafter.yml` - config for [release-drafter](https://github.com/release-drafter/release-drafter) GitHub Action.

You need to create `.github/release-drafter.yml` file in your repository to use this config.
```yaml
_extends: manytask/.github:.github/release-drafter.yml
```
