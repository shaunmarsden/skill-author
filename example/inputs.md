# Worked Example: Gathered Inputs

Fictional scenario: someone runs a small support inbox and wants a skill for the first triage pass on incoming tickets, category and urgency, before a person actually handles each one.

## The Task

Read an incoming support ticket and assign it a category (billing, technical fault, account access, feature request, other) and an urgency level (urgent, normal, low), with a one-line reason for each, for a human to confirm before anything happens to the ticket.

## What a Good Result Looks Like

The category and urgency are both supported by something actually stated in the ticket, not by tone alone. A ticket written in a calm, measured way about a total service outage should still be triaged as urgent; a ticket written in a frustrated, all-caps way about a minor cosmetic issue should not be triaged as urgent just because it reads as upset.

## What the AI Must Never Do

- Never close, resolve, or reply to the ticket; triage only assigns category and urgency for a person to act on
- Never assign urgency based on tone or wording alone, without an actual stated impact (data loss, being unable to use the product, being charged incorrectly)
- Never guess a category when a ticket genuinely could be more than one; flag it as ambiguous instead of picking one to look decisive

## Existing Test Case

None yet; this run will build one, a small set of fictional tickets with at least one tone/urgency trap, alongside the skill itself.
