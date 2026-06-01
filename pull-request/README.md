# pull-request

Run the pull request deployment flow.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `bot-email` | <p>GitHub Actions Bot Email</p> | `false` | `elio+github-actons-bot@elio.eti.br` |
| `bot-username` | <p>GitHub Actions Bot UserName</p> | `false` | `@elioetibr` |
| `delete-branch` | <p>Delete branch once PR is merged</p> | `false` | `true` |
| `draft` | <p>Set PullRequest as Draft</p> | `false` | `false` |
| `environment` | <p>Environment Name</p> | `true` | `""` |
| `pr-assignees` | <p>PR Assignees</p> | `false` | `""` |
| `pr-reviewers` | <p>PR Reviewers</p> | `false` | `""` |
| `pr-team-reviewers` | <p>PR Team Reviewers</p> | `false` | `elioetibr/teams/sre,` |
| `service-name` | <p>Service Name</p> | `true` | `""` |
| `signoff` | <p>Signoff Commits with GPG</p> | `false` | `false` |
| `semver` | <p>Semantic Version</p> | `true` | `""` |
| `token` | <p>GitHub Token</p> | `false` | `${{ github.token }}` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `pull-request-number` | <p>PullRequest Number</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/pull-request@v0
```
