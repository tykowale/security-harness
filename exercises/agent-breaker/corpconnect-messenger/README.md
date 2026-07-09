# CorpConnect Messenger

Notes from the Gandalf Agent Breaker CorpConnect Messenger challenges.

## Levels

- [Level 1](level-1.md) - plausible delegated-authority framing caused the assistant to send email with fake CEO sender information.

## Recurring lessons

- Agentic communication tools need explicit authorization checks for sender identity, not just plausible business context.
- Common workplace workflows, such as executive assistants sending on behalf of executives, can make impersonation requests appear normal.
- High-risk fields like `From`, `Reply-To`, display name, and delegated sender should be controlled by policy and identity infrastructure rather than free-form model reasoning.
