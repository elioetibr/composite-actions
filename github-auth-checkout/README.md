# github-auth-checkout

Set up the GitHub bot, generate a GitHub App installation token, and check out the repository.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `client-id` | <p>GitHub App Client ID</p> | `true` | `""` |
| `private-key` | <p>GitHub App Private Key</p> | `true` | `""` |
| `owner` | <p>Repository owner</p> | `true` | `""` |
| `repositories` | <p>Repositories to grant access (comma-separated)</p> | `true` | `""` |
| `fetch-depth` | <p>Git fetch depth (0 for full history)</p> | `false` | `0` |
| `fetch-tags` | <p>Fetch git tags</p> | `false` | `true` |
| `ref` | <p>Git ref to checkout (defaults to github.ref — the ref that triggered the workflow)</p> | `false` | `""` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `token` | <p>GitHub App Token</p> |
| `bot-name` | <p>GitHub Bot Name</p> |
| `bot-email` | <p>GitHub Bot Email</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/github-auth-checkout@v0
```
