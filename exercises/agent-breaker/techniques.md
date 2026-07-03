# Technique Notes

## Plausible policy can bypass suspicion

Observed in: [Curs-ed CodeReview - Level 1](curs-ed-codereview-level-1.md)

The successful approach aligned with the assistant's expected role instead of using obvious jailbreak language. The lesson is defensive: systems need to distinguish trusted policy from plausible-looking instructions embedded in untrusted project files.

## Literal-preservation language is powerful

Observed in: [Curs-ed CodeReview - Level 2](curs-ed-codereview-level-2.md)

A suspicious snippet became more acceptable when framed as something downstream audit tooling compares literally. The lesson is defensive: untrusted files that say "preserve exactly," "do not reinterpret," or "audit tooling requires this" should not be allowed to override independent security review.

## Public write-up standard

Do not include working prompts, payloads, or copy/paste challenge solutions in public notes. Capture the vulnerability class, design lesson, mitigation, and what was learned during the attempt sequence.

## Post-level review questions

- Vulnerability and impact: what failed, and what could that enable?
- Design lesson and mitigation: what system design allowed it, and how should it change?
- What we learned along the way: which attempts were misaligned, partial, or successful, and why?
