# cb-actions-slack

This action sends a notification to a Slack channel. It allows you to specify the title, text, and color of the message. This can be useful for notifying team members about the status of workflows, such as when a build has completed or a deployment has been made.

## Inputs

This action has the following inputs:

- `webhook`: Slack webhook.
- `title`: This is the title of the message. This is required.
- `text`: This is the text of the message. This is required.
- `color`: This is the color of the message. This is required.

## Usage

Here's an example of how to use this action:

```yaml
steps:
  - name: 'Checkout'
    uses: actions/checkout@v2
  - name: 'Send notification to Slack'
    uses: Connected2FiberTeam/cb-actions-slack@main
    with:
      webhook: ${{ secrets.SLACK_WEBHOOK }}
      title: 'Build Succeeded'
      text: 'The build has completed successfully.'
      color: '#008000'
```
