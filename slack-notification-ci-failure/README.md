# slack-notification-ci-failure

Send a Slack notification when a CI workflow fails.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `channel-id` | <p>Slack channel ID to post the failure notification in.</p> | `true` | `""` |
| `slack-bot-token` | <p>Slack bot token used to authenticate with the Slack Web API.</p> | `true` | `""` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `ts` | <p>Timestamp of the posted Slack message.</p> |
| `channel-id` | <p>Channel ID returned by the Slack Web API.</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/slack-notification-ci-failure@v0
```
