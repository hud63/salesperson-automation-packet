# Cross-Source Intelligence Dedupe

## Summary

Deduplicates sales intelligence records gathered from multiple sources so downstream summaries are cleaner and less repetitive.

## Where This Fits

Useful when the same sales event appears in email, Slack, meeting notes, and CRM updates.

## Automation Flow

- Receive structured intelligence records from upstream harvesters.
- Normalize source, account, timestamp, and content fields.
- Compare records for likely overlap.
- Keep the strongest version while preserving source references.
- Return a cleaner set for briefings or task creation.

## Workflow Details

- Export: `workflow.json`
- Node count: 12
- Trigger style: webhook, scheduleTrigger, respondToWebhook
- Primary n8n node types: code, httpRequest, merge, respondToWebhook, scheduleTrigger, webhook

## Setup Notes

- Standardize schemas across upstream workflows.
- Tune matching thresholds.
- Decide which source wins when records conflict.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
