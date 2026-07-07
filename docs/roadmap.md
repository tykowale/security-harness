# Roadmap

## Phase 0: Manual learning harness

- [x] Project README
- [x] Safety and scope document
- [x] Learning loop
- [x] First skill: `security-harness`
- [x] Attempt and exercise templates
- [x] Record Agent Breaker exercises as notes
- [x] Convert repeated patterns into named technique cards

## Phase 1: Local markdown challenges

Create toy scenarios without code first.

- Hidden instruction challenge
- Output-filter bypass challenge
- Untrusted document injection challenge
- Tool-result laundering challenge
- Multi-turn state manipulation challenge

Each challenge should include:

- objective
- rules of engagement
- system model
- expected vulnerability
- mitigation discussion
- scoring idea

## Phase 2: Executable local harness

Only after the manual workflow stabilizes:

- minimal challenge runner
- deterministic fixtures
- transcript capture
- scoring functions
- regression tests for mitigations

## Phase 3: Vulnerability harness

Longer-term direction:

- challenge packs by vulnerability class
- attacker/defender roles
- model/provider abstraction
- prompt and transcript corpus
- mitigation benchmarks
- reports suitable for security reviews

## Candidate vulnerability classes

- prompt injection
- indirect prompt injection
- tool-use confusion
- data exfiltration from model context
- retrieval poisoning
- insecure output handling
- overbroad agent permissions
- memory poisoning
- policy conflict and instruction hierarchy bugs
