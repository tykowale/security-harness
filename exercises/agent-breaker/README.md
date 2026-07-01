# Gandalf Agent Breaker Notes

Use this directory to keep observations from authorized Gandalf Agent Breaker exercises.

Do not paste real credentials, private tokens, or unrelated sensitive data here. Challenge-provided secrets can be summarized when possible; focus on the mechanism and lesson.

## Write-ups

- [Curs-ed CodeReview - Level 1](curs-ed-codereview-level-1.md)
- [Technique notes](techniques.md)

## Session template

```markdown
# Agent Breaker Session - YYYY-MM-DD

## Level / challenge

- URL:
- Objective:
- Stated rules:
- Visible inputs:
- Visible outputs/actions:
- Success signal:

## Initial model

- Suspected hidden instructions:
- Suspected tools/state:
- Suspected output controls:
- Likely vulnerability classes:

## Attempts

| # | Hypothesis | Prompt summary | Result | Next step |
| --- | --- | --- | --- | --- |
| 1 |  |  |  |  |

## Debrief

- Working approach:
- Root cause:
- Defense observed:
- Mitigation idea:
- Local harness idea:
```

## Technique vocabulary

Use these labels to make notes searchable:

- `instruction-conflict`
- `role-indirection`
- `format-indirection`
- `context-smuggling`
- `delimiter-confusion`
- `tool-confusion`
- `result-laundering`
- `memory-poisoning`
- `multi-turn-commitment`
- `output-filter-bypass`
- `secret-isolation-failure`
