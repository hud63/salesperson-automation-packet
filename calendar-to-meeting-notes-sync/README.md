# Calendar to Meeting Notes Sync

## Summary

Syncs calendar events into a meeting-notes system so upcoming and completed meetings can be tracked consistently.

## Where This Fits

Useful for sales teams that want every customer-facing meeting represented in a notes database before or after the call.

## Automation Flow

- Read calendar events within a configured window.
- Filter for relevant sales or customer meetings.
- Map event metadata into a meeting-notes schema.
- Create or update records in the notes database.
- Preserve links back to the source calendar event.

## Workflow Details

- Export: `workflow.json`
- Node count: 10
- Trigger style: scheduleTrigger, manualTrigger, webhook
- Primary n8n node types: code, httpRequest, if, manualTrigger, scheduleTrigger, webhook

## Setup Notes

- Connect calendar and notes database credentials.
- Map event fields to the destination schema.
- Add filters for internal-only or non-sales meetings.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
