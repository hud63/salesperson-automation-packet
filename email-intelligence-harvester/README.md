# Email Intelligence Harvester

## Summary

Collects recent sales email activity, extracts useful context, and prepares structured intelligence for downstream briefing and drafting workflows.

## Where This Fits

Useful for account executives, founders, and customer-facing operators who need email context summarized into sales-ready signals.

## Automation Flow

- Search or retrieve relevant email messages.
- Filter for sales context and recent customer activity.
- Normalize sender, recipient, subject, date, and thread metadata.
- Extract signals such as asks, objections, next steps, and account context.
- Store or forward structured records for later automation.

## Workflow Details

- Export: `workflow.json`
- Node count: 15
- Trigger style: webhook, scheduleTrigger, respondToWebhook
- Primary n8n node types: code, httpRequest, merge, respondToWebhook, scheduleTrigger, splitOut, webhook

## Setup Notes

- Connect a mailbox credential.
- Replace mailbox search scopes and storage destinations.
- Review filtering rules before using with production email.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
