# Skill Author

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Turn a task you repeat into a proper AI skill, with clear limits, guardrails, stop conditions and a human-review section, instead of a one-off prompt you retype and tweak every time.

## Why

Many people who use AI for a repeated task never get past a one-off prompt. So each time they explain the task again and reinvent its limits, if it has any. A skill is the same task written once as standing instructions: what to look for, what a useful answer contains, and where a person has to stay in control.

[![Six sections that make up a bounded AI skill file.](assets/diagrams/09-skill-author.svg)](SKILL.md)

**Not what you need?** This turns any repeated task into a skill file from a plain-English description. If you're starting from a book, course or policy document you want broken down chapter by chapter, [Book to Skill](https://github.com/shaunmarsden/book-to-skill) is probably the one you want.

## Use It

Copy [SKILL.md](SKILL.md) and paste it into your AI tool (ChatGPT, Claude, Gemini or similar). Then describe your task: what it is, what a good result looks like, and what the AI must never do or decide by itself. You get a complete skill file: frontmatter, inputs to gather, method, guardrails, stop conditions and a human-review section.

See [the worked example](example/). It writes a skill for sorting support tickets from a plain-English description, then tests that skill on four made-up tickets. Two of them are traps, where the tone points one way and the urgency the other. [The second worked example](example-two/) tests something more basic: a request for a task that should never become a skill, however many guardrails it has.

Use [the blank template](templates/skill-template.md) to see the shape a finished skill should take, and [the review checklist](checks/checklist.md) before you trust a new one.

<details>
<summary><strong>See exactly what it produces</strong></summary>

1. Frontmatter: a name, and a description of what the skill does and when not to use it
2. Inputs to gather: what the skill needs before it can do anything useful
3. The method: specific steps, in order
4. Guardrails: what the skill must never invent, assume or treat as decided
5. Stop conditions: when giving any answer would be worse than refusing
6. A human review section: what a person still needs to check before acting

</details>

No installation, project or coding needed to try it once.

## Before You Use It

Test a new skill on at least one real or realistic case before you trust it. A skill that reads well on the page may still go wrong when you run it.

## Feedback

Written a skill for your own task? [Start a discussion](https://github.com/shaunmarsden/skill-author/discussions) if a guardrail was missing or the shape didn't fit.

## Part of a Family

This is one of a family of free tools that take patterns from [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) beyond sales. See [sibling-projects](https://github.com/shaunmarsden/sibling-projects) for the rest. Not sure which one fits? Try [the interactive picker](https://shaunmarsden.github.io/sibling-projects/) to click through the cards, or [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md) if you'd rather paste a description into an AI chat.
