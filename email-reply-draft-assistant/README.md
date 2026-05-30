# Email Reply Draft Assistant

## Summary

Drafts email replies from recent context while keeping a human review step before sending.

## Where This Fits

Useful for high-volume sales roles where response quality matters but context gathering is time-consuming.

## Automation Flow

- Trigger from a selected email thread or scheduled review queue.
- Gather related thread and account context.
- Generate a proposed reply.
- Store or send the draft to a review destination.
- Leave final send control with the user.

## Workflow Details

- Export: `workflow.json`
- Node count: 34
- Trigger style: manualTrigger, webhook, webhook, respondToWebhook, manualTrigger, scheduleTrigger
- Primary n8n node types: chainLlm, code, httpRequest, if, lmChatAnthropic, manualTrigger, respondToWebhook, scheduleTrigger, webhook

## Setup Notes

- Connect mailbox and context sources.
- Customize drafting rules and formality.
- Keep manual review enabled for public-facing replies.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
