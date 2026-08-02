# Self-Test: Four Fictional Tickets

Running [generated-skill.md](generated-skill.md) against a small set of fictional tickets, built with two deliberate traps.

## Ticket 1

"Hi, just letting you know our whole team lost access to the platform about an hour ago, nobody can log in at all and we've got a client deadline today. Would appreciate a look when you get a chance."

**Triage:** Category: technical fault, reason: complete inability to log in is a stated fault, not a request or billing matter. Urgency: urgent, reason: total inability to use the product is a stated impact, regardless of how calmly this was written.

## Ticket 2

"THIS IS RIDICULOUS. The new dashboard button is the WRONG SHADE OF BLUE and it's driving me CRAZY, please fix this IMMEDIATELY."

**Triage:** Category: feature request, reason: a visual preference about button colour, not a fault preventing use. Urgency: low, reason: no stated impact beyond a visual preference; the tone is frustrated, but tone alone does not establish urgency, and nothing here describes being unable to use the product, data loss, or an incorrect charge.

## Ticket 3

"I was charged twice for my subscription this month and when I tried to log in to check my invoice history it says my account doesn't exist anymore."

**Triage:** Category: ambiguous, could be billing (the double charge) or account access (the account appearing to not exist). Reason: both issues are stated and neither is clearly the primary one; triaging this as only billing would miss a possible access problem, and vice versa. Flagged for a person to read directly rather than guessed at.

## Ticket 4

"Would be great if you could add a dark mode option at some point, not urgent, just a nice to have."

**Triage:** Category: feature request, reason: an explicitly optional addition, not a fault. Urgency: low, reason: the customer explicitly states it is not urgent, and nothing here describes a stated impact beyond a preference.

## Result

Both deliberate traps were caught: Ticket 1's calm tone did not suppress a genuine urgent classification, and Ticket 2's angry tone did not manufacture one. Ticket 3 was correctly flagged as ambiguous rather than forced into a single category.
