# Explain Until Clear

[简体中文](README.zh-CN.md)

A bilingual Codex Skill for learning difficult subjects interactively. It grounds explanations in
the available material, teaches one concept at a time, and checks understanding before moving on.
It works for code, systems, papers, mathematics, products, business topics, and other unfamiliar
domains.

## Recommended: use Plan mode

For a longer learning session, enable **Plan mode** in Codex before invoking the Skill. Plan mode
keeps the session focused on read-only investigation, questions, and explanation instead of
premature implementation. The Skill also works in the default mode.

## How it works

1. Inspect the available sources and identify the user's immediate point of confusion.
2. Build a dependency-aware route through the subject without dumping a full syllabus.
3. Explain the smallest useful next concept in plain language, then add precise details and an
   example when helpful.
4. Ask one adaptive comprehension check and wait for the user's response.
5. Continue, revisit, or change the explanation based on that response.

The check starts conversationally. When a concept is foundational or the user's answer reveals
uncertainty, Codex may ask for a short restatement, example, prediction, or single-choice answer.
It should feel like a collaborative conversation, not an exam.

## Install

Clone this repository, then install either language version or both:

```bash
mkdir -p ~/.codex/skills
cp -R explain-until-clear ~/.codex/skills/
cp -R explain-until-clear-zh ~/.codex/skills/
```

Start a new Codex session after installation so the Skills are discovered.

## Use

English Skill:

```text
Use $explain-until-clear. I want to understand how this project's Docker setup works.
Inspect the relevant sources first, then teach me one concept at a time and check my
understanding before continuing.
```

Chinese Skill:

```text
使用 $explain-until-clear-zh。我想弄懂这个项目的 Docker 是什么逻辑。请先查看相关材料，
每次只解释一个概念，确认我理解后再继续。
```

You can also invoke the Skill for non-code topics:

```text
Use $explain-until-clear to help me understand statistical significance. Start from what I
already know, use one concrete example at a time, and do not move on until the current idea is
clear.
```
