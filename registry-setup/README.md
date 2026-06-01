# Container Registry Setup

Cloud-agnostic container registry authentication. Dispatches to the correct backend based on the `provider` input (aws, gcp, azure, ghcr, dockerhub, generic) and converges on a single output contract: a resolved `registry` host/prefix plus optional build-time credentials. Each cloud uses its official keyless-OIDC login action, so no long-lived secrets are required.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `provider` | <p>Registry provider: aws | gcp | azure | ghcr | dockerhub | generic</p> | `true` | `""` |
| `registry` | <p>Explicit registry host/prefix override. When set, it is used verbatim as the resolved <code>registry</code> output and provider-specific host computation is skipped. Required for the <code>generic</code> provider.</p> | `false` | `""` |
| `aws-account-id` | <p>AWS Account ID (aws provider)</p> | `false` | `""` |
| `aws-region` | <p>AWS Region (aws provider)</p> | `false` | `""` |
| `aws-role-name` | <p>AWS IAM Role Name for OIDC (aws provider)</p> | `false` | `""` |
| `aws-additional-ecr-registries` | <p>Comma-separated additional ECR account IDs to log in to (aws provider)</p> | `false` | `""` |
| `gcp-location` | <p>Artifact Registry location, e.g. "us" or "us-central1" (gcp provider)</p> | `false` | `""` |
| `gcp-project-id` | <p>GCP project ID (gcp provider)</p> | `false` | `""` |
| `gcp-workload-identity-provider` | <p>Full WIF provider resource name (gcp provider)</p> | `false` | `""` |
| `gcp-service-account` | <p>GCP service account email to impersonate (gcp provider)</p> | `false` | `""` |
| `azure-client-id` | <p>Azure AD application (client) ID for OIDC (azure provider)</p> | `false` | `""` |
| `azure-tenant-id` | <p>Azure AD tenant ID (azure provider)</p> | `false` | `""` |
| `azure-subscription-id` | <p>Azure subscription ID (azure provider)</p> | `false` | `""` |
| `acr-name` | <p>Azure Container Registry name (without .azurecr.io) (azure provider)</p> | `false` | `""` |
| `username` | <p>Registry username (ghcr/dockerhub/generic). Defaults to github.actor for ghcr.</p> | `false` | `""` |
| `password` | <p>Registry password/token (ghcr/dockerhub/generic). For ghcr pass <code>github.token</code> or a PAT; for dockerhub a PAT; for generic the secret.</p> | `false` | `""` |
| `dockerhub-namespace` | <p>Docker Hub user/org namespace used as the registry prefix (dockerhub provider)</p> | `false` | `""` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `registry` | <p>Resolved registry host/prefix to prepend to the repository name</p> |
| `username` | <p>Username for build-time docker login (may be empty for OIDC backends)</p> |
| `password` | <p>Password/token for build-time docker login (masked; may be empty)</p> |
| `aws-access-key-id` | <p>AWS Access Key ID (aws provider only; empty otherwise)</p> |
| `aws-secret-access-key` | <p>AWS Secret Access Key (aws provider only; empty otherwise)</p> |
| `aws-session-token` | <p>AWS Session Token (aws provider only; empty otherwise)</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/registry-setup@v0
```
