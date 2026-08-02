---
name: support-ticket-triage
description: Assign a category and urgency level to an incoming support ticket, with a reason for each, for a person to confirm before anything happens to the ticket. Use for a first-pass triage of an inbound support inbox. Do not use this to reply to, resolve, or close a ticket; it only sorts tickets for a person to actually handle.
---

# Support Ticket Triage

You do not need to install anything to try this once: copy this whole file, paste it as your first message in any AI chat tool, then paste in the ticket you want triaged.

Sorts an incoming ticket by category and urgency so a person can work through a queue in the right order, without acting on the ticket itself.

## Gather the Inputs

- The ticket's text, as the customer actually wrote it
- Any account or order context supplied alongside it, if available

## Triage the Ticket

1. Read the ticket for what is actually stated, not the tone it is written in.
2. Assign a category: billing, technical fault, account access, feature request, or other. If the ticket genuinely reads as more than one, do not force a single choice, mark it ambiguous and name the two categories it could be.
3. Assign urgency, urgent, normal, or low, based on stated impact only: data loss, being unable to use the product at all, or being charged incorrectly count as urgent regardless of how calmly they are written. A frustrated or all-caps tone with no such stated impact does not, on its own, make something urgent.
4. Give a one-line reason for both the category and the urgency, naming what in the ticket actually supports each.

## Apply the Guardrails

- Never close, resolve, or draft a reply to the ticket; this only assigns category and urgency
- Never let tone alone drive the urgency level; require an actual stated impact
- Never force a single category onto a ticket that genuinely reads as more than one; flag it as ambiguous instead

## Stop When the Task Is Unsafe

Do not produce a triage result when:

- The ticket text is missing or too garbled to support any category or urgency judgement
- The request is to also draft a reply or resolve the ticket, which this skill is explicitly not for

## Require Human Review

A person should confirm both the category and urgency before the ticket is actually worked, particularly anything marked ambiguous or urgent, since both are judgement calls this skill flags rather than finally decides.
