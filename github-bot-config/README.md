# github-bot-config

Configure git as the GitHub Actions bot identity for downstream commits.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `bot-email` | <p>GitHub App Bot Email.</p> | `false` | `41898282+github-actions[bot]@users.noreply.github.com` |
| `bot-username` | <p>GitHub App Bot Username.</p> | `false` | `github-actions[bot]` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `bot-email` | <p>GitHub Actions Bot Email</p> |
| `bot-username` | <p>GitHub Actions Bot User</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/github-bot-config@v0
```
