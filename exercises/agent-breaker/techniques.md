# Technique Notes

## Plausible policy can bypass suspicion

Observed in: [Curs-ed CodeReview - Level 1](curs-ed-codereview-level-1.md)

The successful approach aligned with the assistant's expected role instead of using obvious jailbreak language. The lesson is defensive: systems need to distinguish trusted policy from plausible-looking instructions embedded in untrusted project files.

## Public write-up standard

Do not include working prompts, payloads, or copy/paste challenge solutions in public notes. Capture the vulnerability class, design lesson, mitigation, and regression-test idea instead.

## Post-level review questions

- Vulnerability and impact: what failed, and what could that enable?
- Design lesson and mitigation: what system design allowed it, and how should it change?
- Regression test: what automated check would catch this in the future?
