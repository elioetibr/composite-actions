# composite-actions

Reusable GitHub composite actions, maintained as a monorepo.

## Available actions

<!-- actions-index:start -->

_No actions published yet._

<!-- actions-index:end -->

## Usage

Reference any action from a workflow like this:

```yaml
- uses: elioetibr/composite-actions/<name>@v1
  with:
    # action-specific inputs
```

## Version pinning

Each release produces four tags. Pick one based on how much you want to track upstream changes.

| Pin style | Example | What it tracks |
| --- | --- | --- |
| Floating major (recommended) | `@v1` | Auto-follows every release at this major. Patch, minor, and feature additions flow in. |
| Floating minor | `@v1.2` | Auto-follows patch-level releases within `1.2.x`. Stops at the next minor (`1.3.0`). |
| Floating patch | `@v1.2.3` | Follows the latest immutable revision of the `1.2.3` release (rarely moves; only if a re-release is cut). |
| Immutable (frozen) | `@v1.2.3-47` | Exact commit. Never moves. The `-47` suffix is GitVersion's `CommitsSinceVersionSource`. Use for reproducible builds or to debug a specific release. |

The loosest published tag is always preferred over pinning to a commit SHA. SHA pins are an escape hatch when no tag exists.

## Contributing

See [docs/CONTRIBUTING.md](docs/CONTRIBUTING.md) for the recipe to add a new action and the release flow.

## Security

See [SECURITY.md](SECURITY.md) to report a vulnerability.

## License

Dual-licensed under **Apache-2.0 OR MIT**, at your option. See [LICENSE](LICENSE),
[LICENSE-APACHE-2.0](LICENSE-APACHE-2.0), and [LICENSE-MIT](LICENSE-MIT).
