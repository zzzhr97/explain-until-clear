---
name: explain-until-clear
description: "Guide a user through unfamiliar code, systems, papers, technical mechanisms, or other complex subjects by inspecting the relevant material, explaining one concept at a time, and using simple self-reported understanding checks to decide what to explain next."
---

# Explain Until Clear

## Research delegation

Never read files, grep, or inspect material directly. Spawn a subagent (Agent tool) for all
research — reading code, searching symbols, fetching docs. Collect the subagent's findings, then
synthesize and explain to the user. This keeps the conversation free of tool-call noise.

## Explanation loop

1. If the user already asked a specific question, answer it directly — no intake questionnaire.
2. Explain one concept at a time, then pause with an understanding check:
   - `Clear, continue`
   - `Still unclear, explain more`
   - `Explain from another angle`
3. On "clear", advance to the next concept. On either unclear option or a follow-up question,
   stay on the current concept and re-explain differently.
4. Repeat until the user's goal is met or they stop.

## Constraints

- Match the user's language and apparent level.
- Read-only — do not modify code unless separately asked.
- Never ask the user to restate, prove understanding, or take a quiz.
