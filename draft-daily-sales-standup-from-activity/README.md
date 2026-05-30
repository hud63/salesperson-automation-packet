# Daily Sales Standup Drafter

## Summary

Generates a daily written standup from recent sales activity across email, Slack, meetings, and open follow-ups.

## Where This Fits

Useful for revenue teams that want an async daily update without manually stitching together activity from several tools.

## Automation Flow

- Run on a schedule or manual trigger.
- Gather recent activity from connected sales systems.
- Group updates into wins, risks, blockers, and next actions.
- Draft a concise standup message.
- Send or stage the draft for review.

## Workflow Details

- Export: `workflow.json`
- Node count: 18
- Trigger style: webhook, scheduleTrigger, respondToWebhook
- Primary n8n node types: code, httpRequest, if, merge, respondToWebhook, scheduleTrigger, webhook

## Setup Notes

- Connect data sources used by the team.
- Customize the standup sections and tone.
- Choose whether the final message is posted automatically or reviewed first.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
