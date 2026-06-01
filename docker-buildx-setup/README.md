# docker-buildx-setup

Configure Docker Buildx with an ECR-hosted BuildKit image.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `buildkit-image` | <p>BuildKit image URI</p> | `false` | `moby/buildkit:latest` |
| `network` | <p>Docker network mode</p> | `false` | `host` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/docker-buildx-setup@v0
```
