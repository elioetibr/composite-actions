# checkout-as-bot

Generate a GitHub App installation token, check out the repository using that
token, and configure git as `github-actions[bot]`. Returns the token as a step
output for downstream uses (e.g. authenticated API calls, release-please).

Useful when enterprise policy blocks the default `GITHUB_TOKEN` from creating
pull requests or pushing to protected branches — the App's installation token
acts as a separate identity that retains those permissions.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `client-id` | <p>GitHub App Client ID (e.g. vars.CLIENT_ID).</p> | `true` | `""` |
| `private-key` | <p>GitHub App private key (e.g. secrets.PRIVATE_KEY).</p> | `true` | `""` |
| `owner` | <p>App installation owner. Defaults to the current repository owner.</p> | `false` | `${{ github.repository_owner }}` |
| `repositories` | <p>Repositories to grant the token access to. Defaults to the current repository.</p> | `false` | `${{ github.event.repository.name }}` |
| `ref` | <p>Git ref to checkout. Defaults to the PR head SHA on pull_request events, else the workflow SHA.</p> | `false` | `${{ github.event.pull_request.head.sha || github.sha }}` |
| `fetch-depth` | <p>Number of commits to fetch. 0 fetches full history.</p> | `false` | `0` |
| `fetch-tags` | <p>Whether to fetch tags.</p> | `false` | `true` |
| `submodules` | <p>Submodule checkout mode (false / true / recursive).</p> | `false` | `false` |
| `persist-credentials` | <p>Whether actions/checkout persists the token in the repo's git config.</p> | `false` | `true` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `token` | <p>The generated GitHub App installation access token.</p> |
| `app-slug` | <p>The App's slug (e.g. 'my-bot' for 'my-bot[bot]').</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/checkout-as-bot@v0
  id: setup
  with:
    client-id: ${{ vars.CLIENT_ID }}
    private-key: ${{ secrets.PRIVATE_KEY }}

# downstream step that needs the App token
- env:
    GH_TOKEN: ${{ steps.setup.outputs.token }}
  run: gh api repos/${{ github.repository }}/pulls
```
