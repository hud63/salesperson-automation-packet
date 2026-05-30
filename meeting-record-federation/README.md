# Meeting Record Federation

## Summary

Accepts a webhook request, queries two meeting-note sources, and pairs likely duplicate meeting records across systems using timestamp windows and title-token matching.

## Where This Fits

Useful for sales teams that capture meeting notes in more than one system, such as a CRM notes database plus a call recording or meeting intelligence tool.

## Automation Flow

- Receive date range or lookback window by webhook.
- Query two meeting-note repositories.
- Normalize titles, attendees, companies, dates, links, and source URLs.
- Collapse same-source duplicates, then pair likely cross-source duplicates.
- Return paired, rejected, and unpaired records as JSON.

## Workflow Details

- Export: `workflow.json`
- Node count: 7
- Trigger style: webhook, respondToWebhook
- Primary n8n node types: code, httpRequest, merge, respondToWebhook, webhook

## Setup Notes

- Connect Notion or another meeting-notes database.
- Replace source database IDs and credentials.
- Adjust pairing windows and stopword lists for the target sales process.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
