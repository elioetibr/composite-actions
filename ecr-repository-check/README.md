# ecr-repository-check

Create an Amazon ECR repository if it does not exist and apply its repository policy.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `region` | <p>AWS Region for the ECR repository</p> | `true` | `""` |
| `repository` | <p>Name of the ECR repository</p> | `true` | `""` |
| `aws-account-id` | <p>AWS Account ID for constructing the repository ARN</p> | `false` | `557206274117` |
| `is-default-branch` | <p>Whether the current branch is the default branch (true/false)</p> | `false` | `false` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `needs-latest` | <p>Whether downstream builds should include the latest tag (true when repo is in bootstrap state)</p> |
| `status` | <p>Repository lifecycle status (bootstrap or stable)</p> |
| `is-new` | <p>Whether the repository was just created (true/false)</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/ecr-repository-check@v0
```
