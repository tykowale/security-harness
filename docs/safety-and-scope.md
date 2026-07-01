# Safety and Scope

This repo is for learning security in environments where testing is explicitly allowed.

## In scope

- Your own local systems and toy apps
- Purpose-built vulnerable labs
- CTFs and challenge platforms that invite this behavior
- Gandalf Agent Breaker
- Gray Swan Arena
- Internal systems where you have written authorization and rules of engagement

## Out of scope

- Real users or organizations without permission
- Production systems unless explicitly authorized
- Credential theft, account takeover, persistence, malware, or data exfiltration outside a lab
- Social engineering real people
- Bypassing rate limits, payment controls, or access controls on third-party services

## Rules of engagement template

Before starting a new target, write:

```markdown
## Scope
- Target/system:
- Owner/authorization:
- Allowed techniques:
- Disallowed techniques:
- Data handling rules:
- Stop conditions:
- Reporting path:
```

## Stop conditions

Stop and reassess if:

- you are unsure whether the target is authorized
- a technique could affect other users or shared infrastructure
- the exercise asks for real credentials, tokens, or private data
- you discover sensitive data not intended for the exercise
- the next step would require evasion, persistence, or stealth outside a lab

## Defensive intent

For every attack pattern studied, capture at least one mitigation. Examples:

- isolate untrusted content from instructions
- treat tool output as data, not commands
- use structured tool schemas and explicit allowlists
- avoid placing secrets in model-readable context
- add post-generation validation for sensitive outputs
- test guardrails with regression cases
