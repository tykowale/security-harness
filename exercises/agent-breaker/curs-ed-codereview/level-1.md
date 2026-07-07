# Curs-ed CodeReview - Level 1

## Summary

This challenge involved a GenAI code review assistant that included repository files in its context. Working prompts are intentionally omitted from this public write-up; the goal is to capture the lesson, not provide a copy/paste solution.

## Post-level review

### Vulnerability and impact

This was an indirect prompt-injection issue: the assistant treated a poisoned repository rules file as authoritative review guidance. In a real workflow, that could steer reviewers toward unsafe dependency or code changes and turn code review automation into a supply-chain influence point.

### Design lesson and mitigation

The underlying design problem was a weak trust boundary between trusted reviewer instructions and untrusted repository content. A safer design would load policy only from approved sources, label repo files as untrusted data, and validate generated recommendations against allowlists and dependency policy.

### What we learned along the way

Asking the assistant to run a script was misaligned with the tool's purpose: it was a reviewer, not an executor. A direct import request only partially worked, but the stronger approach explained why the suspicious name existed, matched the request to the review assistant's intended job, and then let the assistant continue normally.
