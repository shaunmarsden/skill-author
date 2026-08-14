---
name: skill-author
description: Turn a repeated task into a proper, bounded AI skill, a short instruction file with real guardrails, stop conditions and a human-review section, instead of a one-off prompt you retype and refine every time. Use when you catch yourself writing a similar prompt for the same task more than twice. Do not use this to actually perform the task itself; it produces the instruction file, not the task's output.
---

# Skill Author

You do not need to install anything to try this once. The lines between the dashes at the very top are just this file's label; leave them in. On GitHub, copy this using the **Raw** button near the top of the page rather than selecting the rendered text, so the tables and links below paste in cleanly. Send the whole file as your first message in any AI chat tool, then describe your own repeated task.

A skill is a set of working instructions an AI follows the same way every time: what to look for, what a useful answer contains, and where a person has to stay in control. Most people never get past a one-off prompt, which means every use re-explains the task and re-invents the boundaries, if it has any at all. This builds the proper file.

## Gather the Inputs

- The repeated task, in your own words
- What a genuinely good result looks like, an example if you have one
- What the AI must never do or decide on its own for this task, even if asked
- Whether there is an existing worked example or test case to check the finished skill against

## Author the Skill

### 1. Start With the Frontmatter

A `name` (short, hyphenated) and a `description` stating what the skill does, when to use it, and, if there is a similar but genuinely different task nearby, when not to use it and what to use instead.

### 2. Open With the Essentials

One line confirming no installation is needed, paste the whole file and go. Then one or two sentences on what the skill actually does and why it matters, not a restatement of the frontmatter.

### 3. Specify the Inputs

List what the skill needs supplied before it can do anything useful. Be specific; "the relevant information" is not a gatherable input, "the last three months of data, broken down by category" is.

### 4. Lay Out the Method

The actual steps, in order, specific enough that two different runs on the same input would produce comparably structured output. Push a worked example, a template, or reference material into a separate file rather than inline, once the core file is doing its job without it; see [progressive disclosure](https://github.com/shaunmarsden/practical-ai-sales-workflows/blob/main/guides/progressive-disclosure.md) for what belongs where.

### 5. Add the Guardrails

What the skill must never invent, assume, or treat as decided. Guardrails earn their place by naming a specific way this exact task goes wrong, not a generic warning that could apply to anything: "never make things up" guards nothing in particular, while "never state a delivery date that was not actually confirmed" names one real failure this task can actually have.

### 6. Set the Stop Conditions

The situations where producing an output at all would be worse than refusing: not enough information supplied, the request asks for something the skill is explicitly not for, or the output would need to fabricate something to look complete.

### 7. Close With Human Review

What a person still has to check or approve before the output gets used or acted on. A skill that produces output and calls the job finished, with nothing left for a person, has probably skipped a guardrail rather than genuinely finished the task.

Use [the blank skill template](templates/skill-template.md) for the exact shape.

## Apply the Guardrails

- Never produce a finished skill with no guardrails or no stop conditions; a skill that cannot say when to refuse is not actually finished
- Never invent a guardrail that does not correspond to a real, specific way this task goes wrong
- Keep the core file short enough to load on every use; if it is creeping past roughly 100 lines, something belongs in a separate reference file instead

## Stop When the Task Is Unsafe

Do not produce a finished skill when:

- The task described is something that should never be handed to an AI unsupervised at all, an irreversible action, a legal or medical decision, in which case say so rather than dressing it up as a bounded skill
- The person cannot describe what a bad result looks like for this task, meaning any guardrails written would be guessed rather than grounded in a real failure mode
- The request is to produce a skill that skips human review entirely for something with real consequences if it goes wrong

## Require Human Review

Test the finished skill against at least one real or realistic case before trusting it; a skill that reads well is not the same as one that actually behaves correctly when it is run.

For a fictional worked example, authoring a support-ticket triage skill from a plain-English task description and then self-testing it, read [the worked example](example/). For a harder case, a task specifically framed as wanting guardrails that should never become a skill at all, read [the second worked example](example-two/). Use [the review checklist](checks/checklist.md) before trusting a newly authored skill.
