# slack-notification

Send a Slack notification with a payload and optionally update an existing message.

<!-- action-docs-inputs source="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `channel-id` | <p>Slack channel ID to post or update the message in.</p> | `true` | `""` |
| `slack-bot-token` | <p>Slack bot token used to authenticate with the Slack Web API.</p> | `true` | `""` |
| `payload` | <p>Slack message payload as a JSON object. The channel (and ts, when updating) are merged in automatically.</p> | `true` | `""` |
| `update-ts` | <p>Timestamp of an existing message to update. When set, the message is updated via chat.update instead of posted.</p> | `false` | `""` |
<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `ts` | <p>Timestamp of the posted or updated Slack message.</p> |
| `channel-id` | <p>Channel ID returned by the Slack Web API.</p> |
<!-- action-docs-outputs source="action.yml" -->

## Usage

```yaml
- uses: elioetibr/composite-actions/slack-notification@v0
```
