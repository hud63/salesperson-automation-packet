# Sales Thread Closure Detector

## Summary

Reviews recent sales conversations and detects threads that appear resolved, stalled, or ready to close out.

## Where This Fits

Useful for teams managing many parallel customer or prospect conversations where follow-up hygiene matters.

## Automation Flow

- Collect recent communication records.
- Identify threads with clear outcomes or no remaining ask.
- Classify closure status and rationale.
- Emit structured status updates for downstream tasks or summaries.
- Optionally notify a channel or update a tracking system.

## Workflow Details

- Export: `workflow.json`
- Node count: 15
- Trigger style: webhook, scheduleTrigger, respondToWebhook
- Primary n8n node types: code, httpRequest, merge, respondToWebhook, scheduleTrigger, webhook

## Setup Notes

- Define closure criteria for the sales motion.
- Connect communication sources.
- Route status outputs to a CRM, task tracker, or review queue.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
