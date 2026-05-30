# Slack Intelligence Harvester

## Summary

Collects useful sales context from Slack conversations and turns it into structured signals for briefs, standups, and follow-up workflows.

## Where This Fits

Useful for organizations where deal context, customer asks, and internal decisions often happen in Slack.

## Automation Flow

- Search configured Slack channels or threads.
- Filter for sales-relevant messages.
- Normalize channel, author, timestamp, and permalink metadata.
- Extract asks, decisions, blockers, and account references.
- Store or pass structured intelligence to downstream workflows.

## Workflow Details

- Export: `workflow.json`
- Node count: 14
- Trigger style: webhook, scheduleTrigger, respondToWebhook
- Primary n8n node types: code, httpRequest, merge, respondToWebhook, scheduleTrigger, splitOut, webhook

## Setup Notes

- Connect a Slack credential with the right scopes.
- Choose channels and search windows.
- Tune filters to avoid capturing unrelated internal chatter.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
