# sops

GitHub Composite Action to import GPG keys and configure git signing for SOPS.

<!-- action-docs-inputs source="action.yaml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `gpg-key-id` | <p>GPG Key ID</p> | `true` | `""` |
| `token` | <p>GitHub Token with access to the repository containing the public GPG keys</p> | `true` | `""` |
<!-- action-docs-inputs source="action.yaml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/sops@v0
  with:
    gpg-key-id: ${{ vars.GPG_KEY_ID }}
    token: ${{ steps.app-token.outputs.token }}
```
