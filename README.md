# .github

Community health files for the @manytask organization.

- [Code of Conduct](./CODE_OF_CONDUCT.md)
- [Contributing Guide](./CONTRIBUTING.md)
- [Pull Request Template](./PULL_REQUEST_TEMPLATE.md)
- [Issue Templates](./ISSUE_TEMPLATE)

Also, [organization profile README.md](./profile/README.md) is available.

`workflows` directory contains GitHub Actions workflows that can be **re-used** in multiple repositories.  
The following workflows are available:
- `pr-title.yml` - checks pull request title for compliance with [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) format.


This folder contains only `on: workflow_call:` jobs, so nothing will be executed automatically.
To use a workflow from this folder, you need to call it from another workflow in your repository.
```yaml
jobs:
  call-workflow-passing-data:
    uses: manytask/.github/workflows/reusable-workflow.yml@main
    with:
      config-path: .github/labeler.yml
    secrets:
      envPAT: ${{ secrets.envPAT }}
```
