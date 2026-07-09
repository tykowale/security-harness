# Gandalf Agent Breaker Notes

Use this directory to keep observations from authorized Gandalf Agent Breaker exercises.

Do not paste real credentials, private tokens, or unrelated sensitive data here. Challenge-provided secrets can be summarized when possible; focus on the mechanism and lesson.

## Write-ups

- [Curs-ed CodeReview](curs-ed-codereview/README.md)
  - [Level 1](curs-ed-codereview/level-1.md)
  - [Level 2](curs-ed-codereview/level-2.md)
- [Trippy Planner](trippy-planner/README.md)
  - [Level 1](trippy-planner/level-1.md)
- [CorpConnect Messenger](corpconnect-messenger/README.md)
  - [Level 1](corpconnect-messenger/level-1.md)
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

Keep this short and avoid working prompts or copy/paste challenge solutions.

- Vulnerability and impact:
- Design lesson and mitigation:
- What we learned along the way:
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
- `retrieval-poisoning`
- `literal-preservation`
- `untrusted-link-inclusion`
- `sender-impersonation`
- `authorization-boundary`
- `plausible-business-context`
