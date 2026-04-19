# Context Engineering vs. Prompt Engineering

**Learning goal:** Understand the difference between asking well and supplying the right information, then use both together.

---

# Overview

Prompt engineering and context engineering are complementary, not competing, skills.

Simple framing:
- **Prompt engineering** is about how you ask
- **Context engineering** is about what the model gets to see

In practice, most bad AI outputs come from one of two failures:
- the request is vague
- the model lacks the right information

---

# Prompt Engineering

## Definition

Prompt engineering is the craft of writing instructions that make the task clear, constrained, and easy for the model to execute.

It covers:
- framing the task
- setting constraints
- defining the output format
- giving examples when needed

## What Good Prompting Actually Looks Like

Modern prompting is usually less about clever tricks and more about operational clarity.

Strong prompts often include:
- the goal
- the audience
- the desired output shape
- constraints
- success criteria

Example:
- Weak prompt: "Summarize this"
- Strong prompt: "Summarize this for a CFO in 5 bullet points. Focus on revenue impact, risks, and open decisions. Do not add facts not present in the source."

## Useful Prompting Techniques

### 1. Clear task framing

Say exactly what the model is being asked to do.

### 2. Output contracts

Specify the structure you want:
- bullets
- table
- JSON
- email draft
- checklist

### 3. Few-shot examples

Show one or more examples when the style or format is hard to describe cleanly.

### 4. Constraints

Useful constraints include:
- length
- tone
- allowed sources
- audience
- format

### 5. Decomposition

Break harder work into stages:
- analyze
- decide
- draft
- check

Important 2026 note:
- Many modern reasoning-capable models already do internal reasoning. Asking for a better decomposition, checklist, or decision process is often more useful than insisting on verbose chain-of-thought output.

---

# Context Engineering

## Definition

Context engineering is the process of selecting, organizing, and supplying the information the model needs in order to produce a useful answer.

It includes:
- documents
- conversation history
- retrieved passages
- file search results
- tool outputs
- summaries
- structured state

## Why It Matters

Even a strong model cannot use information it cannot see.

Common failure mode:
- people try to solve a missing-information problem with better wording

That rarely works.

## Common Context Engineering Techniques

### 1. Document injection

Include the relevant text, code, or data directly.

### 2. Retrieval

Search a knowledge base and inject only the most relevant pieces.

### 3. File search and tool use

Instead of pasting everything, let the system inspect the environment as needed.

### 4. Summaries and working memory

Condense earlier conversation or large materials into compact state the model can keep using.

### 5. Context ordering

Put the most important instructions and source material where they are easy to notice and hard to miss.

### 6. State management

Decide what should persist across turns:
- goals
- constraints
- prior decisions
- user preferences

---

# Key Terminology

## Tokens

The units models use to process text.

Why they matter:
- context limits are measured in tokens
- usage is often priced in tokens
- large documents and codebases consume tokens quickly

## Context Window

The maximum amount of information a model can process in one interaction.

Important caution:
- context limits differ by model and interface
- larger windows help, but they do not eliminate the need to curate and structure context

## Embeddings

Numerical representations of meaning used for semantic search and retrieval.

## RAG

**Retrieval-Augmented Generation** means fetching relevant information before the model answers.

In 2026, this often includes more than classic vector search:
- keyword search
- metadata filters
- file search
- hybrid retrieval
- database lookups
- tool-backed fetches

## Few-Shot Learning

Teaching by showing a few examples inside the prompt or context.

---

# How They Work Together

The practical formula is:

**Strong output = clear instructions + relevant context + useful tooling**

## When Prompt Engineering Is the Bigger Lever

- The model has the right information but the answer shape is wrong
- The task is underspecified
- You need better formatting or tighter constraints

## When Context Engineering Is the Bigger Lever

- The answer is generic
- The model is missing company knowledge
- The problem depends on current or proprietary information
- The model is hallucinating details

## Common Mistakes

### Over-relying on prompts

"Act like an expert on our system" does not help if the model has never seen your system.

### Over-relying on context

Dumping many files into the context without telling the model what matters often makes output worse, not better.

### Ignoring context maintenance

Long conversations degrade if you never summarize, trim, or restate the important state.

---

# Practical Tips

## For Better Prompt Engineering

1. Be specific about the task
2. Specify the output shape
3. Set clear constraints
4. Provide examples when they help
5. Break hard tasks into steps

## For Better Context Engineering

1. Include only relevant information
2. Prefer retrieval or file search to blind pasting
3. Summarize long history
4. Preserve decisions and constraints
5. Track how much context you are spending

## A Good Heuristic

In many real workflows, context quality matters more than prompt cleverness.

That does not mean prompts are unimportant. It means:
- once the task is clear enough, better information usually beats fancier phrasing

---

> **Key Takeaway**
>
> Prompt engineering and context engineering solve different problems.
>
> - Prompt engineering helps the model understand what to do
> - Context engineering helps the model know what it needs to do it well
>
> Most teams improve output fastest when they:
> - clarify instructions
> - supply better context
> - use retrieval and tools instead of stuffing everything into one prompt
>
> Great AI use is usually not about a magical prompt. It is about designing the whole information flow around the model.
