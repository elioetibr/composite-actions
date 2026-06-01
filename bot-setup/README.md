# bot-setup

Configure git locally as the `github-actions[bot]` user for downstream commits in a workflow.

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
| `bot-email` | <p>GitHub App Bot Email.</p> |
| `bot-username` | <p>GitHub App Bot Username.</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/bot-setup@v0
- run: git commit -m "automated change" -a
```
