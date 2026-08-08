# Explain Until Clear

[English](README.md)

这是一个双语 Codex Skill，用于通过互动逐步弄懂复杂或陌生的主题。它会先依据现有材料建立事实基础，
每次只解释一个概念，并在继续之前确认用户是否真正理解。它不仅适用于代码，也适用于系统、论文、
数学、产品、商业以及其他领域。

## 推荐开启 Plan 模式

开始较长的学习会话前，推荐先在 Codex 中开启 **Plan 模式**。Plan 模式有利于把会话保持在只读调查、
提问和解释上，避免过早进入实现。没有开启 Plan 模式时，这个 Skill 也可以正常使用。

## 工作方式

1. 检查可用材料，找到用户眼下真正困惑的位置。
2. 在内部整理知识依赖关系，但不一次性倾倒完整大纲。
3. 先用直白语言讲解当前最小且有用的概念，必要时再补充精确机制和具体例子。
4. 每次只进行一个自适应理解检查，然后等待用户回应。
5. 根据回应决定继续、回退到前置概念，还是换一种讲法。

理解检查先采用自然的询问。当概念很关键，或用户的回答暴露出不确定时，Codex 可以请用户做简短
复述、举例、预测结果或回答一个单选问题。整个过程应当像共同讨论，而不是考试。

## 安装

克隆本仓库，然后安装任意一种语言版本，也可以同时安装：

```bash
mkdir -p ~/.codex/skills
cp -R explain-until-clear ~/.codex/skills/
cp -R explain-until-clear-zh ~/.codex/skills/
```

安装后新建一个 Codex 会话，使 Codex 重新发现这些 Skill。

## 使用

中文版：

```text
使用 $explain-until-clear-zh。我想弄懂这个项目的 Docker 是什么逻辑。请先查看相关材料，
每次只解释一个概念，确认我理解后再继续。
```

英文版：

```text
Use $explain-until-clear. I want to understand how this project's Docker setup works.
Inspect the relevant sources first, then teach me one concept at a time and check my
understanding before continuing.
```

这个 Skill 同样适用于非代码主题：

```text
使用 $explain-until-clear-zh 帮我弄懂统计显著性。从我已经知道的内容开始，每次只使用一个
具体例子；当前概念没有讲清楚之前，不要进入下一个概念。
```
