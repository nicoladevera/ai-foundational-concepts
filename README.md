# AI Foundational Concepts

Last updated: April 2026

These pages are designed to build from first principles to practical implementation. Most chapters are intentionally evergreen. The most time-sensitive material lives in:

- [03 - The AI Landscape - Choosing Models and Tools](<./03 - The AI Landscape - Choosing Models and Tools.md>)
- [08 - Multimodal AI - Beyond Text](<./08 - Multimodal AI - Beyond Text.md>)

## Pages in this Section

- [01 - Machine Learning 101](<./01 - Machine Learning 101.md>)
- [02 - LLMs 101](<./02 - LLMs 101.md>)
- [03 - The AI Landscape - Choosing Models and Tools](<./03 - The AI Landscape - Choosing Models and Tools.md>)
- [04 - Context Engineering vs Prompt Engineering](<./04 - Context Engineering vs Prompt Engineering.md>)
- [05 - Customizing AI - Fine-Tuning vs RAG vs Prompt Engineering](<./05 - Customizing AI - Fine-Tuning vs RAG vs Prompt Engineering.md>)
- [06 - CLI Agents vs Chat-Based AI Performance](<./06 - CLI Agents vs Chat-Based AI Performance.md>)
- [07 - Automation, AI Workflows, and AI Agents](<./07 - Automation, AI Workflows, and AI Agents.md>)
- [08 - Multimodal AI - Beyond Text](<./08 - Multimodal AI - Beyond Text.md>)

---

# Your Learning Journey

## Foundation Layer: Understanding AI

### 1. Machine Learning 101

Start here if you are new to AI or want the base mental model.

What you'll learn:
- What machine learning is
- How supervised, unsupervised, and reinforcement learning differ
- How traditional ML, deep learning, and LLMs fit together

Sets up:
- Everything else in this repo

### 2. LLMs 101

Read after Machine Learning 101.

What you'll learn:
- What LLMs are
- Why tokens, context windows, hallucinations, and cutoffs matter
- Why tool use changes what models can do in practice

Sets up:
- The specific AI systems most people interact with today

Key connection:
- ML explains the foundation. This page explains the language-model layer built on top of it.

### 3. The AI Landscape: Choosing Models and Tools

Read after LLMs 101.

What you'll learn:
- How to think about the current provider landscape
- How to choose by task, latency, cost, privacy, and deployment model
- Which parts of the market change quickly and which do not

Sets up:
- Practical model and tool selection

Key connection:
- Once you know what LLMs are, this chapter helps you decide which kinds of systems to use and when.

---

## Application Layer: Using AI Effectively

### 4. Context Engineering vs. Prompt Engineering

Read after The AI Landscape.

What you'll learn:
- The difference between asking well and supplying the right information
- Why context quality usually matters more than prompt cleverness
- How retrieval, summaries, file search, and output contracts fit together

Sets up:
- Baseline AI usage skills for almost every workflow

### 5. Customizing AI: Fine-Tuning vs. RAG vs. Prompt Engineering

Read after Context Engineering vs. Prompt Engineering.

What you'll learn:
- How to adapt AI systems to your data and requirements
- When to use prompt design, retrieval, structured outputs, evals, and fine-tuning
- Why most teams should not start with fine-tuning

Sets up:
- More realistic production decision-making

Key connection:
- Page 4 teaches the core interaction patterns. This page shows how to make them work with your knowledge and constraints.

### 6. CLI Agents vs. Chat-Based AI Performance

Read after Customizing AI.

What you'll learn:
- Why tool-enabled agents often outperform plain chat on environment-bound work
- Where chat still shines
- How interface design changes actual productivity

Sets up:
- Better decisions about how you work with AI day to day

Key connection:
- This chapter is less about model quality and more about workflow architecture.

### 7. Automation, AI Workflows, and AI Agents

Read after CLI Agents vs. Chat-Based AI Performance.

What you'll learn:
- The difference between deterministic automation, AI-assisted workflows, and more autonomous agents
- How to match autonomy to task risk
- Why approvals, permissions, and observability matter

Sets up:
- Strategic thinking about what to build with AI

---

## Breadth Layer: Beyond Text

### 8. Multimodal AI: Beyond Text

Read after Automation, AI Workflows, and AI Agents.

What you'll learn:
- How modern AI systems work across text, images, audio, and video
- Which multimodal capabilities are mature versus still changing quickly
- How to choose tools by workflow fit rather than hype

Sets up:
- A broader view of current AI capabilities

---

## Quick Start Paths

### Path 1: "I'm completely new to AI"

Read in order:
1. Machine Learning 101
2. LLMs 101
3. The AI Landscape
4. Context vs Prompt Engineering
5. Customizing AI
6. CLI vs Chat
7. Automation, Workflows, and Agents
8. Multimodal AI

### Path 2: "I've used ChatGPT and want to get better"

Start with:
1. Context vs Prompt Engineering
2. Customizing AI
3. The AI Landscape

Then backfill:
- Machine Learning 101
- LLMs 101

### Path 3: "I need to choose AI tools for my company"

Start with:
1. The AI Landscape
2. Customizing AI
3. CLI vs Chat
4. Automation, Workflows, and Agents

Then backfill the foundations.

### Path 4: "I want to build AI applications"

Read:
1. Machine Learning 101
2. LLMs 101
3. Context vs Prompt Engineering
4. Customizing AI
5. CLI vs Chat
6. Automation, Workflows, and Agents

Optional:
- Multimodal AI if your product touches images, audio, or video

---

# The Learning Arc

```text
CONCEPTS
- Machine Learning 101
- LLMs 101

LANDSCAPE
- The AI Landscape

SKILLS
- Context vs Prompt Engineering
- Customizing AI

APPLICATIONS
- CLI vs Chat
- Automation, Workflows, and Agents

BREADTH
- Multimodal AI
```

## How These Pages Work Together

Machine learning explains the engine. LLMs explain the dominant application layer. The landscape chapter shows what is currently available. Context and customization teach how to use systems well. CLI vs chat explains why interfaces matter. Automation, workflows, and agents explain implementation patterns. Multimodal AI expands the picture beyond text.

Key principle:
- The foundations should remain useful even as providers and model names change.
- The market-facing pages are intentionally more dated and should be refreshed periodically.
