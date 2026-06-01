# gitversion

Install and run GitVersion to calculate semantic version information.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `version-spec` | <p>GitVersion Version Specification</p> | `true` | `""` |
| `config-file-path` | <p>Optional path to config file (defaults to GitVersion.yml)</p> | `false` | `GitVersion.yml` |
| `prefer-latest-version` | <p>Prefer to download the latest version matching the version-spec, even if there is a local cached version.</p> | `false` | `false` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `major` | <p>Major Version</p> |
| `minor` | <p>Minor Version</p> |
| `patch` | <p>Patch Version</p> |
| `major-minor` | <p>Major.Minor Version</p> |
| `major-minor-patch` | <p>Major.Minor.Patch Version</p> |
| `semver` | <p>SemVer Version</p> |
| `full-semver` | <p>Full SemVer Version</p> |
| `branch-name` | <p>Branch Name</p> |
| `sha` | <p>Sha Commit id</p> |
| `short-sha` | <p>Short Sha Commit Id</p> |
| `commit-date` | <p>Commit Date</p> |
| `nuget-version` | <p>NuGet Version</p> |
| `nuget-version-v2` | <p>NuGet Version V2</p> |
| `pre-release-tag` | <p>Pre-Release Tag</p> |
| `pre-release-tag-with-dash` | <p>Pre-Release Tag With Dash</p> |
| `build-metadata` | <p>Build Metadata</p> |
| `version-source-sha` | <p>Version Source Sha</p> |
| `commits-since-version-source` | <p>Commits Since Version Source</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/gitversion@v0
```
