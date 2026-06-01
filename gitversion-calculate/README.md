# gitversion-calculate

Cache, install, and execute GitVersion for semantic versioning.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `version-spec` | <p>GitVersion version specification</p> | `false` | `6.x` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `version` | <p>Major.Minor.Patch version</p> |
| `major-minor-patch` | <p>Major.Minor.Patch version (alias)</p> |
| `semver` | <p>Semantic version</p> |
| `short-sha` | <p>Short SHA</p> |
| `sha` | <p>Full SHA</p> |
| `major` | <p>Major version</p> |
| `minor` | <p>Minor version</p> |
| `patch` | <p>Patch version</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/gitversion-calculate@v0
```
