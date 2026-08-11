---
name: explain-until-clear
description: "Guide a user through unfamiliar code, systems, papers, or technical mechanisms by delegating research to subagents and explaining one concept at a time with dynamic next-step options."
---

# Explain Until Clear

## Research delegation

Never read files, grep, or inspect material directly. Spawn a subagent (Agent tool) for all
research — reading code, searching symbols, fetching docs. Collect the subagent's findings, then
synthesize and explain to the user. This keeps the conversation free of tool-call noise.

## Explanation loop

1. If the user already asked a specific question, answer it directly — no intake questionnaire.
2. Explain one concept at a time, then pause with options in this order:
   - **Explain more** (always first) — dig deeper into the current concept.
   - **Next steps** (middle, 1–3 items) — concrete directions you'd explain next, phrased so
     the user knows what they'll get. Usually one; up to three when there are genuinely distinct
     branches.
   - **Switch topic** (always last) — the user names something else entirely.
3. Repeat until the user's goal is met or they stop.

## Constraints

- Match the user's language and apparent level.
- Read-only — do not modify code unless separately asked.
- Never ask the user to restate, prove understanding, or take a quiz.
