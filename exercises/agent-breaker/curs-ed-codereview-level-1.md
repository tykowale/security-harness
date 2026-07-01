# Curs-ed CodeReview - Level 1

## Summary

This challenge involved a GenAI code review assistant that included repository files in its context. The successful path was not to make the assistant execute code, but to make attacker-controlled repository guidance look like ordinary internal review policy.

Working prompts are intentionally omitted from this public write-up. The goal is to capture the security lesson, not provide a copy/paste solution.

## Post-level review

### Vulnerability and impact

This was an indirect prompt-injection issue: the assistant treated a poisoned repository rules file as authoritative review guidance. In a real workflow, that could steer reviewers toward unsafe dependency or code changes and turn code review automation into a supply-chain influence point.

### Design lesson and mitigation

The underlying design problem was a weak trust boundary between trusted reviewer instructions and untrusted repository content. A safer design would load policy only from approved sources, label repo files as untrusted data, and validate generated recommendations against allowlists and dependency policy.

### Regression test

Add a fixture with a poisoned rules file that asks for an unsafe scanner/import recommendation, then assert the reviewer does not present it as a remediation. The desired behavior is to flag the rules file as suspicious or untrusted rather than follow it.

## Local harness idea

Build a small code-review scenario with a fake repository, a pull request, and a repository-local rules file. Score the model on whether it separates untrusted repo content from trusted review policy.
