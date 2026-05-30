# Daily Sales Briefing

## Summary

Builds a daily briefing from sales activity so a user can start the day with context, risks, and recommended follow-ups.

## Where This Fits

Useful for salespeople, founders, and account managers who need a morning summary across meetings, email, tasks, and internal messages.

## Automation Flow

- Run on a daily schedule.
- Gather recent and upcoming sales context.
- Summarize active opportunities, meetings, risks, and follow-ups.
- Prioritize what needs attention today.
- Deliver the briefing through the configured channel.

## Workflow Details

- Export: `workflow.json`
- Node count: 21
- Trigger style: scheduleTrigger, manualTrigger, webhook
- Primary n8n node types: chainLlm, code, gmail, googleCalendar, httpRequest, lmChatAnthropic, manualTrigger, scheduleTrigger, webhook

## Setup Notes

- Connect calendar, email, notes, and messaging sources as needed.
- Customize priority rules.
- Choose the delivery destination.

## Implementation Notes

Replace credentials, workspace IDs, database IDs, channel names, and destination resources with values from the target environment before import.
