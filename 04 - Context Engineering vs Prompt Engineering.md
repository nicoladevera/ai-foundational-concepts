# Context Engineering vs. Prompt Engineering

**Learning goal:** Master both what information to provide (context) and how to ask (prompts) for optimal AI results.

---

# Overview

Prompt Engineering and Context Engineering are two complementary approaches to getting better results from AI systems. Think of them as the "how" and "what" of AI communication.

---

# Prompt Engineering

## Definition

**Prompt Engineering** is the art and science of crafting instructions, questions, and conversation structure to guide an AI toward producing better, more accurate, and more useful responses.

It's about **how you ask** - the words, structure, tone, and techniques you use in your request.

## How It Works

LLMs (Large Language Models) are prediction engines. They generate responses token-by-token based on patterns learned during training. Prompt engineering exploits this by:

1. **Framing the task clearly** - Reducing ambiguity so the model predicts the right type of response
2. **Providing structure** - Guiding the model's generation process with templates or formats
3. **Setting constraints** - Narrowing the prediction space to more relevant outputs
4. **Priming behavior** - Using psychological techniques that influence how the model "thinks"

> 🧠 **The psychology of prompts:** LLMs respond to prompting techniques that mirror human psychology. Asking someone to "think step-by-step" helps humans solve problems better - and it works the same way for LLMs. Role-playing ("you are an expert") primes both humans and LLMs to draw on relevant knowledge.

## Key Techniques

### 1. Zero-Shot Prompting
Asking the AI to perform a task without any examples.
**Example:** "Summarize this article in 3 bullet points."

### 2. Few-Shot Prompting
Providing 1-3 examples before asking the AI to perform the task.

### 3. Chain-of-Thought (CoT)
Asking the AI to explain its reasoning step-by-step.
**Example:** "Let's think step-by-step: First, identify the problem. Second, list possible solutions. Third, evaluate each option."

### 4. Role Prompting
Assigning the AI a specific persona or expertise.
**Example:** "You are a senior product manager with 10 years of experience in fintech. Analyze this product strategy."

### 5. Output Formatting
Specifying exactly how you want the response structured.
**Example:** "Provide your answer in JSON format with keys: problem, solution, impact."

### 6. Constraint Setting
Defining boundaries for the response.
**Example:** "Answer in 50 words or less. Use only information from the provided document."

---

# Context Engineering

## Definition

**Context Engineering** is the strategic selection, organization, and delivery of background information that an AI system uses to inform its responses.

It's about **what information you provide** - the data, documents, examples, and knowledge you feed into the AI's context window.

## How It Works

LLMs have a **context window** - a limited amount of text they can "see" and process at once (measured in tokens). Context engineering is about:

1. **Selecting relevant information** - Choosing what to include in the limited context space
2. **Organizing information strategically** - Placing important details where the AI is most likely to use them
3. **Managing context size** - Balancing comprehensiveness with token limits
4. **Maintaining continuity** - Ensuring the AI has the right background across a conversation

## Key Techniques

### 1. Document Injection
Providing relevant documents, code, or data directly in your prompt.

### 2. Conversation History Management
Deciding which parts of previous messages to keep or discard.

### 3. RAG (Retrieval-Augmented Generation)
Automatically fetching and including relevant documents from a knowledge base.

**How RAG works:**
- Your question is converted into an embedding (numerical representation)
- A search finds documents with similar embeddings (semantically related content)
- Those documents are injected into the context before the AI responds
- The AI answers based on the retrieved information

> 🔍 **Why RAG is powerful:** It solves the knowledge cutoff and hallucination problems simultaneously. Instead of the LLM making up answers from its training data, RAG ensures it's responding based on YOUR specific, current documents. This is how you can chat with your company's knowledge base, documentation, or proprietary data.

### 4. Semantic Chunking
Breaking large documents into smaller, meaningful pieces that fit in the context window.

### 5. Contextual Priming
Providing background information that shapes how the AI interprets your request.

---

# Key Terminology Explained

## Tokens
**Definition:** The basic units LLMs use to process text. Roughly 3-4 characters per token, or about 0.75 words.

**Why it matters:**
- Context windows are measured in tokens (e.g., 200,000 tokens)
- API costs are calculated per token
- Understanding tokens helps you manage what fits in context

> 💰 **Cost and capacity trade-offs:** Every character you include uses tokens. A 10-page document might use 7,500 tokens. If your context window is 200,000 tokens, you could include ~26 such documents. But API costs scale with tokens used, so including unnecessary context wastes money.

## Context Window
**Definition:** The maximum amount of text (in tokens) an LLM can process in a single interaction.

**Analogy:** Like RAM for your conversation - everything the AI can "remember" at once.

**Example:** Claude's 200,000 token window ≈ 150,000 words ≈ a 500-page book

> 📚 **The expansion revolution:** Context windows have exploded in recent years. GPT-3 (2020) had 4,000 tokens. Claude (2025) has 200,000 tokens - a 50x increase. This fundamentally changes what's possible.

## Embeddings
**Definition:** Mathematical representations (vectors) of text that capture semantic meaning.

**Why useful:** Enables semantic search - finding information by meaning, not just keyword matching.

> 🧒 **The magic of meaning:** Embeddings let computers understand that "I'm hungry" and "I need food" mean similar things, even though they share no words. This powers RAG, recommendation systems, and semantic search.

## RAG (Retrieval-Augmented Generation)
**Definition:** A technique that combines information retrieval with LLM generation.

## Few-Shot Learning
**Definition:** Teaching an AI how to perform a task by showing it a few examples (typically 1-5) within the prompt.

## Chain-of-Thought (CoT)
**Definition:** A prompting technique that asks the AI to show its reasoning process step-by-step before reaching a conclusion.

---

# How They Work Together

Prompt Engineering and Context Engineering are not either/or - they complement each other:

## The Formula
**Great AI Output = Strong Prompt × Relevant Context**

## When to Prioritize Each

**Prioritize Prompt Engineering when:**
- The task is well-defined but you're not getting the right format
- You need to change *how* the AI approaches the problem
- The AI has enough information but isn't using it effectively

**Prioritize Context Engineering when:**
- The AI lacks specific knowledge it needs
- Responses are too generic or filled with assumptions
- You need answers grounded in specific documents or data
- The AI is hallucinating details

## Common Mistakes

### Over-relying on Prompts
"Act as an expert on our codebase" doesn't work if you haven't provided any code.

### Over-relying on Context
Dumping 50 files into context without clear instructions on what to do with them.

### Ignoring Token Limits
Providing so much context that there's no room left for the response.

---

# Practical Tips

## For Better Prompt Engineering:
1. **Be specific** - Vague prompts get vague responses
2. **Use examples** - Show, don't just tell
3. **Set constraints** - Length, format, tone, sources
4. **Think step-by-step** - Break complex tasks into stages
5. **Iterate** - Refine your prompts based on what works

## For Better Context Engineering:
1. **Be selective** - More isn't always better; relevant is better
2. **Organize strategically** - Put critical info early and late (recency bias)
3. **Use summaries** - Condense lengthy background info
4. **Track token usage** - Know how much space you're using
5. **Update context** - Remove outdated info as conversations evolve

## The 80/20 Rule

**20% of your effort should go to:**
- Clear, specific instructions (prompt)
- Defining the output format (prompt)

**80% of your effort should go to:**
- Finding and organizing relevant information (context)
- Ensuring the AI has what it needs to succeed (context)

Great context can compensate for mediocre prompts. But great prompts can't compensate for missing context.

---

> 🎯 **Key Takeaway**
>
> Mastering AI interactions requires both prompt engineering (HOW you ask) and context engineering (WHAT information you provide):
>
> - **Prompt Engineering:** Craft clear instructions, use examples, set constraints, define output formats
> - **Context Engineering:** Select relevant information, organize strategically, manage token limits, use RAG when needed
> - **The Formula:** Great AI Output = Strong Prompt × Relevant Context
> - **Priority Rule:** 80% of effort on context (ensuring AI has what it needs), 20% on prompts (clear instructions)
>
> Key techniques to master:
> - **Few-shot prompting** - Show examples of what you want
> - **Chain-of-thought** - Ask AI to reason step-by-step
> - **RAG** - Automatically retrieve and inject relevant documents
> - **Strategic organization** - Place critical info where AI will notice it
>
> Remember: An AI can only be as good as the information it can see. Great context with mediocre prompts beats great prompts with missing context every time.
