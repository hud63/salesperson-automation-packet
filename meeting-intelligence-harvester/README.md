# Meeting Intelligence Harvester

## Summary

Processes meeting records into structured sales intelligence, including follow-ups, decisions, risks, and account context.

## Where This Fits

Useful for teams that rely on customer calls, demos, and internal deal reviews as primary sources of truth.

## Automation Flow

- Retrieve recent meeting records or notes.
- Normalize meeting metadata and content.
- Extract follow-ups, decisions, stakeholders, and risk signals.
- Prepare records for deduplication and daily briefing.
- Store or forward structured output.

## Workflow Details

- Export: `workflow.json`
- Node count: 22
- Trigger style: webhook, scheduleTrigger, respondToWebhook
- Primary n8n node types: code, httpRequest, merge, respondToWebhook, scheduleTrigger, splitOut, switch, webhook

## Setup Notes

- Connect the meeting-notes or recording source.
- Map the expected meeting properties.
- Adjust extraction prompts for the team’s sales language.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
