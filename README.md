# Skill Author

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Turn a task you repeat into a reusable AI instruction file, with clear limits, reasons to stop and checks for a person before acting.

**Start here:** [Copy the skill into any AI chat](SKILL.md), then describe the task you want it to help you write instructions for. See [Use It](#use-it) for the template to paste alongside it.

## Why

If you keep writing the same prompt, a skill lets you save the instructions in one place: what to look for, what a useful answer contains and where a person has to stay in control.

[![Six sections that make up a bounded AI skill file.](assets/diagrams/09-skill-author.svg)](SKILL.md)

**Not what you need?** This helps write a skill file from a plain-English task description. It is for tasks that are suitable to hand to AI, not every repeated task. If you're starting from a book, course or policy document you want broken down chapter by chapter, [Book to Skill](https://github.com/shaunmarsden/book-to-skill) is probably the one you want.

## Use It

Copy [SKILL.md](SKILL.md) and paste it into any AI chat. Copy [the blank template](templates/skill-template.md) into the same chat too: the skill links to it for the exact layout, but pasting a link doesn't supply the file's contents.

Then describe your task: what it is, what a good result looks like and what the AI must never do or decide by itself. The requested output has a name and description, inputs to gather, steps to follow, limits, reasons to stop and a human-review section.

Use [the review checklist](checks/checklist.md) before you trust a new skill.

## Examples and evidence

- [Support-ticket triage](example/): a generated skill and four made-up tickets, including two where tone and urgency point opposite ways. The review also records an unclear category and a missing urgency.
- [An unsafe task](example-two/): an illustrative refusal to write a skill for a decision that should stay with a person.
- [Reviewing someone else's skill](example-three/): a checklist review of an external skill, with six reported runs on made-up search results.

The first two examples don't record the model or how the outputs were produced. They are illustrations, not logged model tests. The third reports six runs on one model without tools, but doesn't include the raw replies or identify the model. I can't verify its run totals from files in this repo. None of these examples establishes that the tool behaves reliably across AI products or real tasks.

<details>
<summary><strong>See exactly what it produces</strong></summary>

1. A name and description at the top of the file, including when not to use it
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
