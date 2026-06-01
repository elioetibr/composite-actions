# install-deployment-tools

Install essential deployment tools that may be missing on the runner.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `argocd-version` | <p>ArgoCD Version</p> | `false` | `v2.12.6` |
| `helm-version` | <p>Helm Charts Version</p> | `false` | `v3.17.0` |
| `sops-version` | <p>Sops Version</p> | `false` | `v3.9.4` |
| `helm-secrets-version` | <p>Helm Secrets Plugin Version</p> | `false` | `4.6.2` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/install-deployment-tools@v0
```
