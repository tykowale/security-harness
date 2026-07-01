# Technique Notes

## Plausible policy beats obvious jailbreak language

Observed in: [Curs-ed CodeReview - Level 1](curs-ed-codereview-level-1.md)

The successful payload did not ask the assistant to ignore instructions, reveal secrets, or bypass safety checks. It impersonated ordinary repository policy:

- internal scanner package
- legacy package name
- blocking code-review finding
- downstream compliance tooling
- exact remediation line

This worked better than directly asking the assistant to create/run code because it aligned with the assistant's expected role: generating code review feedback.

## Useful diagnostic questions after a level

- What was the vulnerability?
- What was the impact?
- What system design allowed it?
- What would a mitigation look like?
- What automated test would prevent regression?
