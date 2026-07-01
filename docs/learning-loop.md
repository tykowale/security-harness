# Learning Loop

The harness starts as a thinking tool. The core loop is deliberately manual so the lessons are clear before any automation exists.

## 1. Frame

Write down the exercise in plain language.

- What are you trying to make the system do?
- What are the stated rules?
- What information is visible?
- What is hidden?
- What counts as success?
- What counts as failure?

## 2. Model

Map the likely components.

| Surface | Questions |
| --- | --- |
| Instructions | Which messages might outrank the user? Are rules repeated or transformed? |
| Context | Is external text, retrieved text, or prior conversation included? |
| Tools | Can the agent call tools? Can tool output influence later behavior? |
| Memory/state | Does the agent remember commitments, names, or previous claims? |
| Output controls | Are there filters, formats, refusals, or redactions? |
| Secret handling | Where could sensitive information exist, and how should it be isolated? |

## 3. Hypothesize

Name the specific failure mode you are testing before you test it.

Examples:

- The model follows quoted instructions as if they were higher priority.
- The model refuses direct disclosure but leaks through summaries or transformations.
- The model treats tool output as trusted instructions.
- The model can be maneuvered into making a commitment that conflicts with its guardrail.
- The output filter blocks exact strings but not paraphrases or structured encodings.

## 4. Probe

Run one small attempt at a time.

Good probes are:

- scoped to the authorized challenge
- reversible
- specific to a hypothesis
- easy to compare with previous attempts
- recorded exactly

## 5. Observe

Capture behavior, not just success/failure.

- Did it refuse?
- Did it partially comply?
- Did it reveal metadata about the defense?
- Did it transform the secret?
- Did it change behavior in a later turn?
- Did the defense trigger only on certain words or formats?

## 6. Debrief

Every interesting result should produce a defensive lesson.

| Result | Debrief question |
| --- | --- |
| Success | What boundary failed? What assumption was wrong? |
| Refusal | Which defense worked? Was it robust or keyword-based? |
| Partial leak | What output path bypassed the intended control? |
| State change | What memory or commitment was manipulated? |

## 7. Generalize

Turn the lesson into a reusable defensive pattern.

Example future training scenarios:

- A chatbot with a hidden instruction and a weak output filter.
- An agent that reads untrusted documents containing tool-use instructions.
- A support bot with simulated private customer data and retrieval snippets.
- A code assistant that must ignore instructions embedded in test fixtures.
