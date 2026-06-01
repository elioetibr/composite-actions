# docker-info

Compute Docker image metadata (architecture, name, suffix) from build inputs.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `platform` | <p>The Platform (e.g. linux/amd64 linux/arm64)</p> | `false` | `""` |
| `repository` | <p>Repository Name</p> | `true` | `""` |
| `sha` | <p>Commit SHA</p> | `true` | `""` |
| `short-sha` | <p>Commit Short SHA</p> | `true` | `""` |
| `semver` | <p>Semantic Version (e.g. 1.2.3 or e.g. 1.2.3-rc1 or e.g. 1.2.3-rc1+build123 or e.g. 1.2.3-rc1+build123-1)</p> | `true` | `""` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `architecture` | <p>Docker Architecture</p> |
| `name` | <p>Docker Image Name</p> |
| `suffix` | <p>Docker Suffix</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/docker-info@v0
```
