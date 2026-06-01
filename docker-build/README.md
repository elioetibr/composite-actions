# docker-build

Build a Docker image with Buildx, applying computed tags and platform settings.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `client-id` | <p>GitHub App Client ID</p> | `true` | `""` |
| `aws-account-id` | <p>AWS Account ID</p> | `true` | `""` |
| `dockerfile-path` | <p>Docker Path</p> | `true` | `""` |
| `ecr-registry` | <p>Registry Name</p> | `true` | `""` |
| `ecr-repository` | <p>Repository Name</p> | `true` | `""` |
| `owner` | <p>GitHub Organization Owner / GitHub Personal Account</p> | `true` | `""` |
| `private-key` | <p>GitHub App Secret Key</p> | `true` | `""` |
| `region` | <p>AWS Region</p> | `true` | `""` |
| `repositories` | <p>GitHub Repository Name</p> | `true` | `""` |
| `role-name` | <p>AWS GitHub OIDC Role Name</p> | `true` | `""` |
| `semver` | <p>Semantic Versioning</p> | `true` | `""` |
| `send-slack-notification` | <p>Send Slack Notification</p> | `true` | `""` |
| `sha` | <p>Commit SHA</p> | `true` | `""` |
| `short-sha` | <p>Commit Short SHA</p> | `true` | `""` |
| `target-arch` | <p>The Target Architecture (e.g. amd64 arm64)</p> | `true` | `""` |
| `version-spec` | <p>GitVersion Version Specification</p> | `true` | `""` |
| `context` | <p>Dockerfile Directory</p> | `false` | `.` |
| `create-latest-tag` | <p>Create and push the latest tag alongside the version tag</p> | `false` | `false` |
| `image` | <p>Image Name</p> | `false` | `""` |
| `platform` | <p>The Platform (e.g. linux/amd64 linux/arm64)</p> | `false` | `""` |
| `provenance` | <p>Generate provenance attestations</p> | `false` | `false` |
| `push` | <p>Push Image after Build</p> | `false` | `true` |
| `sonar-token` | <p>SonarCloud Token</p> | `false` | `""` |
| `tag` | <p>Image Tag Version</p> | `false` | `""` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `architecture` | <p>Target architecture for the build</p> |
| `build-datetime` | <p>Build date and time information</p> |
| `platform` | <p>Target platform for the build</p> |
| `ref-name` | <p>Reference name (branch or tag)</p> |
| `run-attempt` | <p>Workflow run attempt number</p> |
| `semver` | <p>Semantic version</p> |
| `sha` | <p>Git commit SHA</p> |
| `sha-short` | <p>Short Git commit SHA</p> |
| `suffix` | <p>Tag suffix</p> |
| `tags` | <p>Docker image tags</p> |
| `tags-json` | <p>Docker image tags in JSON format</p> |
| `meta-version` | <p>Metadata version info</p> |
| `meta-tags` | <p>Metadata tags info</p> |
| `meta-labels` | <p>Metadata labels info</p> |
| `meta-annotations` | <p>Metadata annotations info</p> |
| `meta-json` | <p>Metadata in JSON format</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/docker-build@v0
```
