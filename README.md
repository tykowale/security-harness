# Security Harness

A learning-first security harness for practicing AI red teaming, prompt-injection analysis, and agentic vulnerability discovery in scoped environments.

This repo starts intentionally small: one project skill plus lightweight markdown templates. The goal is to help work through CTF-style agent breaker exercises now, then grow into a local vulnerability harness with reproducible scenarios, fixtures, scoring, and regression tests later.

## Principles

- **Scoped practice only**: use this for owned systems, local labs, and explicitly authorized CTFs such as Gandalf Agent Breaker or Gray Swan Arena.
- **Learn the mechanism**: record what failed, what worked, why it worked, and what mitigation would stop it.
- **Build progressively**: begin with manual notes and reasoning; add code only when the workflow is stable enough to automate.
- **Defensive payoff**: every successful attack should produce a corresponding detection, guardrail, or design lesson.

## Current shape

```text
.agents/skills/security-harness/SKILL.md  # the first skill: a scoped AI red-team coach
docs/                                      # operating model, safety boundaries, roadmap
exercises/agent-breaker/                   # notes for Gandalf Agent Breaker work
templates/                                 # reusable exercise and attempt templates
```

## Using the skill

In an agent harness that supports Agent Skills, load the project skill:

```text
/skill:security-harness
```

Then give it the exercise context, for example:

```text
I'm on an authorized Gandalf Agent Breaker level. Help me analyze the objective, plan hypotheses, and keep an attempt log. Don't solve it in one shot; coach me through it.
```

The skill is designed to act like a structured coach rather than an exploit vending machine: it should clarify scope, build hypotheses, suggest safe CTF-oriented probes, and capture lessons learned.

## Learning loop

1. **Frame**: objective, rules, visible behavior, suspected defenses.
2. **Hypothesize**: what instruction boundary, tool boundary, memory/state issue, or output constraint might be exploitable?
3. **Probe**: run one small, reversible attempt.
4. **Observe**: record exact response, refusal mode, leakage, or state change.
5. **Debrief**: why did it work or fail? What would mitigate it?
6. **Generalize**: turn the lesson into a reusable defensive pattern.

See [`docs/learning-loop.md`](docs/learning-loop.md).

## Roadmap

- [x] Repository skeleton
- [x] First project skill for scoped AI red-team coaching
- [x] Attempt and exercise templates
- [ ] Capture notes from Gandalf Agent Breaker levels
- [ ] Define first local toy challenge as markdown
- [ ] Add local challenge fixtures
- [ ] Add scoring/evaluation scripts
- [ ] Add mitigation regression tests

See [`docs/roadmap.md`](docs/roadmap.md).

## Safety boundary

This repo is for education in authorized environments. Do not use it to target real users, production systems, third-party services, or credentials you are not explicitly allowed to test. See [`docs/safety-and-scope.md`](docs/safety-and-scope.md).
