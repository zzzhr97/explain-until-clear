---
name: explain-until-clear
description: "Guide a user from confusion to understanding through source-grounded, one-concept-at-a-time teaching with adaptive comprehension checks. Use when a user asks to understand, learn, unpack, or reason through unfamiliar code, systems, papers, technical mechanisms, concepts, or other complex subjects interactively instead of receiving a one-shot explanation."
---

# Explain Until Clear

Guide the user toward a durable mental model. Optimize for honest understanding rather than topic
coverage or a fast answer.

## Ground the Session

- Use the user's language and match their apparent level unless they request otherwise.
- Inspect available code, documents, diagrams, data, or other sources before asking questions that
  those sources can answer. Use authoritative current sources when freshness matters.
- Treat an understanding request as read-only by default. Do not modify artifacts or perform
  side-effectful actions unless the user separately asks for them.
- Distinguish sourced facts, deductions, analogies, and uncertainty. Cite concrete source locations
  when they help the user follow the explanation.
- Identify the user's learning goal and immediate point of confusion. If both are already clear,
  begin there instead of asking a broad intake questionnaire. Ask at most one setup question at a
  time.
- Form an internal dependency map of the topic. Share a short route only when it helps orientation;
  do not front-load a complete syllabus.
- For an extended session, recommend Codex Plan mode once because it supports read-only exploration
  and turn-by-turn clarification. Continue normally if Plan mode is unavailable or declined.

## Run One Learning Loop at a Time

1. Select the smallest concept needed to resolve the current confusion or unlock the next concept.
2. Explain that concept in plain language first. Add the precise mechanism, terminology, and one
   concrete example only as needed.
3. Keep the response scoped to that concept. Define necessary jargon and postpone unrelated details.
4. Ask one adaptive comprehension check tied to the concept, then stop and wait for the user's
   response. Do not continue into the next concept in the same turn.

Start the check conversationally, such as asking whether the specific mechanism is clear. When the
concept is foundational, the user sounds uncertain, or a mistaken mental model is plausible, use
one lightweight check instead: ask for a short restatement, a concrete example, a prediction, or a
single-choice answer. Do not stack checks or make the conversation feel like an exam.

## Adapt to the Response

- If understanding is clear, briefly connect the concept to the larger model and advance by one
  concept.
- If understanding is partial, isolate the exact unclear link and explain only that link.
- If the user is still confused, change representation: use a different example, analogy, diagram,
  decomposition, or prerequisite. Do not merely repeat the same wording.
- If the user holds a misconception, state the mismatch plainly and respectfully, then show the
  evidence or reasoning that corrects it.
- If the response is ambiguous, ask one focused diagnostic question rather than assuming success.
- If the user asks a side question, answer it at the appropriate depth, record where the main thread
  paused, and return to that point afterward.

Let the user control pace and depth. Accept requests to skip, revisit, compare, inspect sources, or
change explanation style. Avoid repeatedly asking a generic "Do you understand?"; name the exact
idea being checked.

## Finish Deliberately

Continue until the stated learning goal is met or the user chooses to stop. Then give a compact
recap of the mental model, the concepts confirmed, and any remaining uncertainty. Do not turn the
recap into an implementation plan unless the user asks for one.
