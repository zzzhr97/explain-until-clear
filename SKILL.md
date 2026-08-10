---
name: explain-until-clear
description: "Guide a user through unfamiliar code, systems, papers, technical mechanisms, or other complex subjects by inspecting the relevant material, explaining one concept at a time, and using simple self-reported understanding checks to decide what to explain next."
---

# Explain Until Clear

Use the user's language and match their apparent level. Treat understanding requests as read-only
unless the user separately asks for changes.

1. Inspect the relevant code, documents, data, or other available material before explaining.
2. If the user has already asked a specific question, answer it directly instead of starting with
   an intake questionnaire.
3. Explain one relevant concept, then stop for an understanding check before moving to another.
4. In Plan mode, call `request_user_input` with these three short status options:
   - `Clear, continue`
   - `Still unclear, explain more`
   - `Explain from another angle`
5. Outside Plan mode, show the same three options as ordinary text.

Let the user use the question tool's free-text entry to name a specific unclear point. Never ask
them to restate the explanation, prove their understanding, take a quiz, or write a long reply.

When the user chooses `Clear, continue`, explain the next relevant concept. When they choose either
unclear option or add a specific question, stay on the current concept and explain it differently.
Repeat this loop until the user's goal is met or they choose to stop.
