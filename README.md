# Skill Author

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Turn a repeated task into a proper, bounded AI skill, real guardrails, stop conditions and a human-review section, instead of a one-off prompt you retype and refine every time.

## Why

Most people using AI for a repeated task never get past a one-off prompt, which means every use re-explains the task and re-invents whatever boundaries it has, if it has any at all. A skill is the same task turned into a standing set of instructions: what to look for, what a useful answer contains, and where a person has to stay in control, written once and reused.

[![Six sections that make up a bounded AI skill file.](assets/diagrams/09-skill-author.svg)](SKILL.md)

## Use It

Copy [SKILL.md](SKILL.md) and paste it into your AI tool (ChatGPT, Claude, Gemini, or similar), then describe your own repeated task: what it is, what a good result looks like, and what the AI must never do or decide on its own. It produces a complete skill file: frontmatter, gathered inputs, method, guardrails, stop conditions, and a human-review section.

See [the worked example](example/): authoring a support-ticket triage skill from a plain-English task description, then self-testing the actual generated skill against four fictional tickets built with two deliberate tone-versus-urgency traps in opposite directions. [The second worked example](example-two/) tests something more fundamental: a request specifically asking for a task that should never become a skill at all, no matter how it is guardrailed.

Use [the blank template](templates/skill-template.md) to see the exact shape a finished skill should take, and [the review checklist](checks/checklist.md) before trusting a newly authored one.

<details>
<summary><strong>See exactly what it produces</strong></summary>

1. Frontmatter: a name and a description stating what the skill does and when not to use it
2. Gathered inputs: what the skill needs supplied before it can do anything useful
3. The method: specific, ordered steps
4. Guardrails: what the skill must never invent, assume, or treat as decided
5. Stop conditions: when producing an output at all would be worse than refusing
6. A human review section: what still needs a person to check before acting

</details>

No installation, project, or coding required to try it once.

## Before You Use It

Test a newly authored skill against at least one real or realistic case before trusting it. A skill that reads well on the page is not the same as one that behaves correctly when it is actually run.

## Licence

MIT.

## Feedback

Authored a skill for your own task? [Start a discussion](https://github.com/shaunmarsden/skill-author/discussions) if a guardrail was missing or the generated shape did not fit.

## Part of a Family

This is one of a family of free tools generalising [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) patterns beyond sales. See [sibling-projects](https://github.com/shaunmarsden/sibling-projects) for the rest, or use [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md) if you are not sure which one actually fits.
