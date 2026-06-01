# Ensure Container Repository

Cloud-agnostic repository provisioning. For the `aws` provider this delegates to ecr-repository-check (ECR repositories must be created explicitly and need an access policy + lifecycle tags). All other providers (ghcr, gcp, azure, dockerhub, generic) auto-create the repository on first push, so this becomes a no-op while still emitting the same output contract.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `provider` | <p>Registry provider: aws | gcp | azure | ghcr | dockerhub | generic</p> | `true` | `""` |
| `repository` | <p>Repository name</p> | `true` | `""` |
| `is-default-branch` | <p>Whether the current branch is the default branch (true/false)</p> | `false` | `false` |
| `aws-region` | <p>AWS Region (aws provider)</p> | `false` | `""` |
| `aws-account-id` | <p>AWS Account ID (aws provider)</p> | `false` | `""` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `needs-latest` | <p>Whether downstream builds should include the latest tag</p> |
| `status` | <p>Repository lifecycle status (bootstrap/stable for aws; n/a otherwise)</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/registry-repository-ensure@v0
```
