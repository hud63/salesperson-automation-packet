# Salesperson Automation Packet

This packet is a proof of concept for a salesperson automation system built in n8n. The workflows show how a revenue operator can collect context from email, Slack, calendar, and meeting notes, turn that context into structured intelligence, deduplicate overlapping signals, and generate practical daily outputs.

## How the Packet Fits Together

The packet has four layers:

- **Source harvesters** collect sales context from email, Slack, calendar, and meeting records.
- **Normalization and deduplication** converts messy source data into cleaner structured records.
- **Reasoning workflows** classify closure status, identify next steps, and prepare useful summaries.
- **Output workflows** generate daily briefings, standup drafts, and email draft assistance for human review.

## Workflow Map

| Workflow | Export | Role in the packet |
| :--- | :--- | :--- |
| [Match duplicate meeting notes across tools](meeting-record-federation/) | [`workflow.json`](meeting-record-federation/workflow.json) | Accepts a webhook request, queries two meeting-note sources, and pairs likely duplicate meeting records across systems using timestamp windows and title-token matching. |
| [Turn sales emails into structured follow-up signals](email-intelligence-harvester/) | [`workflow.json`](email-intelligence-harvester/workflow.json) | Collects recent sales email activity, extracts useful context, and prepares structured intelligence for downstream briefing and drafting workflows. |
| [Draft a daily sales standup from recent activity](daily-sales-standup-drafter/) | [`workflow.json`](daily-sales-standup-drafter/workflow.json) | Generates a daily written standup from recent sales activity across email, Slack, meetings, and open follow-ups. |
| [Find conversations that are ready to close out](sales-thread-closure-detector/) | [`workflow.json`](sales-thread-closure-detector/workflow.json) | Reviews recent sales conversations and detects threads that appear resolved, stalled, or ready to close out. |
| [Extract sales context from internal messages](slack-intelligence-harvester/) | [`workflow.json`](slack-intelligence-harvester/workflow.json) | Collects useful sales context from Slack conversations and turns it into structured signals for briefs, standups, and follow-up workflows. |
| [Convert meeting notes into action items](meeting-intelligence-harvester/) | [`workflow.json`](meeting-intelligence-harvester/workflow.json) | Processes meeting records into structured sales intelligence, including follow-ups, decisions, risks, and account context. |
| [Generate a morning sales briefing](daily-sales-briefing/) | [`workflow.json`](daily-sales-briefing/workflow.json) | Builds a daily briefing from sales activity so a user can start the day with context, risks, and recommended follow-ups. |
| [Remove duplicate signals across sources](cross-source-intelligence-dedupe/) | [`workflow.json`](cross-source-intelligence-dedupe/workflow.json) | Deduplicates sales intelligence records gathered from multiple sources so downstream summaries are cleaner and less repetitive. |
| [Prepare reviewed reply drafts from thread context](email-reply-draft-assistant/) | [`workflow.json`](email-reply-draft-assistant/workflow.json) | Drafts email replies from recent context while keeping a human review step before sending. |
| [Create meeting-note records from calendar events](calendar-to-meeting-notes-sync/) | [`workflow.json`](calendar-to-meeting-notes-sync/workflow.json) | Syncs calendar events into a meeting-notes system so upcoming and completed meetings can be tracked consistently. |

## Suggested Operating Model

A typical implementation would run the calendar and meeting syncs continuously, run source harvesters on a schedule, deduplicate the combined intelligence, then generate a morning briefing and async standup. Email drafting should stay human-reviewed, especially for customer-facing communication.

## Import Notes

- Replace every placeholder credential before activating a workflow.
- Replace placeholder database, channel, calendar, and mailbox IDs with resources from the target environment.
- Review prompts, filters, and retention settings before using production customer data.
- Keep drafts and summaries in review mode until the outputs are consistently accurate.

## Disclaimer

These workflows are proof-of-concept examples, not a turnkey production package. They are intended to demonstrate an automation architecture for sales productivity and should be reviewed for security, privacy, and data handling requirements before deployment.
