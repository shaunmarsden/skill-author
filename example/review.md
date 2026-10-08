# Review: Did Skill Author Do Its Job?

I checked [the generated skill](generated-skill.md) against what [SKILL.md](../SKILL.md) requires of a finished skill. Then I checked how that skill behaved in [the self-test](self-test.md).

## Checking the Generated Skill Against Its Own Requirements

- **Real guardrails, not generic ones.** All three name a specific way this task goes wrong: tone driving urgency, forcing one category on a ticket that fits two, and drifting into replying to or resolving tickets. None is a vague "be careful" that could apply to any skill.
- **Real stop conditions.** Both name a concrete situation, not just "if unsure." One exists to stop the skill quietly growing into a bigger task it was never meant to cover (drafting replies).
- **A human review section that does something.** It names the two outputs to check (category and urgency) and says why, rather than a blanket "a human should review this."
- **Short enough to load every time.** Under 40 lines, with no supporting files needed yet. Nothing had to move into a separate reference file.

## Checking the Behaviour Against the Two Deliberate Traps

- **Ticket 1** was written calmly but said the whole team had lost access. The skill's guardrail (urgency needs a stated impact, not a tone) held. It marked the ticket urgent because of the impact, despite the calm wording. That's the harder direction: most triage mistakes go the other way and downgrade a real emergency because it was written calmly.
- **Ticket 2** was written angrily but only described a colour preference. The same guardrail held the other way: the heated tone didn't make it urgent.
- **Ticket 3** fits two categories. The guardrail against forcing one category held. The skill flagged the ticket as ambiguous rather than picking one to look decisive. But the triage gave no urgency, and the skill asks for one on every ticket. A double charge is also one of the impacts the skill names as urgent. So the flag was right and the triage was incomplete.

## What Still Needs a Human Check

- Four made-up tickets is a small test. As with every tool in this family, it shows the skill can behave correctly, not that it will across a real, messier inbox.
- Real tickets are often less clean than these four. A mixed-signal ticket (calm tone, no stated impact, but a plausible reason to worry anyway) would be a harder test to try before trusting this on a real queue.

## Verdict

Skill Author produced a skill with real, specific guardrails, and they held in both directions of the tone trap it was built to test. The self-test is small, but it covered the two mistakes this task is most likely to make (tone pushing urgency up and tone pushing it down), plus false precision on category.
