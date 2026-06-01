# aws-ecr-setup

Configure AWS credentials via OIDC and log in to Amazon ECR.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `aws-account-id` | <p>AWS Account ID</p> | `false` | `557206274117` |
| `aws-region` | <p>AWS Region</p> | `false` | `us-east-1` |
| `aws-role-name` | <p>AWS IAM Role Name for OIDC</p> | `false` | `github-actions-role` |
| `additional-registries` | <p>Comma-separated list of ECR registries to login to. If empty, logs in to the default registry for the account.</p> | `false` | `""` |
| `role-duration-seconds` | <p>Role session duration in seconds</p> | `false` | `900` |
| `role-session-name` | <p>Role session name</p> | `false` | `ViafouraGitHubActions` |
| `mask-aws-account-id` | <p>Mask AWS Account ID in logs</p> | `false` | `false` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `aws-access-key-id` | <p>AWS Access Key ID</p> |
| `aws-secret-access-key` | <p>AWS Secret Access Key</p> |
| `aws-session-token` | <p>AWS Session Token</p> |
| `registry` | <p>ECR Registry URL for primary account</p> |
| `additional-registries` | <p>Comma-separated list of additional ECR Registry URLs</p> |
| `all-registries` | <p>Comma-separated list of all ECR Registry URLs (primary + additional)</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/aws-ecr-setup@v0
```
