# docker-tags

Compute Docker image tags from semantic version, SHA, and platform inputs.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `architecture` | <p>The Platform (e.g. amd64 or arm64)</p> | `false` | `""` |
| `platform` | <p>The Platform (e.g. linux/amd64 or linux/arm64)</p> | `false` | `""` |
| `semver` | <p>Semantic Version (e.g. 1.2.3 or e.g. 1.2.3-rc1 or e.g. 1.2.3-rc1+build123 or e.g. 1.2.3-rc1+build123-1)</p> | `true` | `""` |
| `suffix` | <p>Docker Tag Suffix</p> | `false` | `""` |
| `create-latest-tag` | <p>Create and push the latest tag alongside the version tag</p> | `false` | `false` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `docker-tags-json` | <p>Docker Tags Json</p> |
| `tags` | <p>Docker Tags</p> |
| `version` | <p>Docker Tag Version</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/docker-tags@v0
```
