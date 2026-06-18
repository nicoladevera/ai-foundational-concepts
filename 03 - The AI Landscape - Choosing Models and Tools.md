# The AI Landscape: Choosing Models and Tools

Last updated: June 2026

**Learning goal:** Navigate the current AI ecosystem without getting trapped by hype, stale recommendations, or provider marketing.

---

# How to Read This Page

This chapter is intentionally more time-sensitive than the rest of the repo.

Use it for:
- a current snapshot of the market
- rough provider positioning
- practical selection guidance

Do not treat it as timeless:
- model availability changes
- product names change
- pricing changes
- benchmark leadership changes

For current decisions, always confirm against the provider's official docs.

---

# The Current State of the Market

As of June 2026, the frontier has a few clear patterns:

- Closed frontier models from OpenAI, Anthropic, and Google dominate general-purpose cloud usage
- Open-weight families from Meta, Mistral, and others remain important for self-hosting, privacy, and custom deployment
- Tool use now matters as much as raw model quality for many real workloads
- Multimodal capability is no longer niche; text-plus-image is normal, and audio/video support is expanding quickly
- Product availability differs by surface: API, web app, enterprise plan, and coding-agent product often expose different models or limits

The right question is usually not:
- "Which model is best?"

It is:
- "Which model and interface fit this workflow, budget, and risk profile?"

---

# The Main Provider Buckets

## 1. Frontier General-Purpose Cloud Models

These are the default starting point for most teams that want strong quality with minimal infrastructure.

### OpenAI

Current positioning:
- Strong flagship for complex reasoning, coding, professional workflows, and computer use
- Strong small-model tier for cost-sensitive coding, tool use, and subagent patterns
- Broadest mainstream ecosystem across ChatGPT, API, and coding products

Useful June 2026 reference points:
- `gpt-5.5` is OpenAI's flagship for reasoning, coding, agentic workflows, and computer use
- `gpt-5.5-pro` is the higher-accuracy premium option for the hardest work
- `gpt-5.4-mini` and `gpt-5.4-nano` are the smaller cost and latency tiers
- `chat-latest` is the API alias for OpenAI's current Instant chat model, which was updated to GPT-5.5 Instant in May 2026

What OpenAI is especially strong at:
- coding workflows
- tool-heavy agent systems
- computer use
- document and spreadsheet-style knowledge work
- long-context API workflows, including up to 1M tokens for GPT-5.5

Important caveat:
- ChatGPT and API availability are not the same. For example, GPT-4o and several older ChatGPT models were retired from ChatGPT on February 13, 2026, while remaining available in the API.
- GPT-5.5 is positioned above GPT-5.4 on capability and token efficiency, but it is also more expensive. Use the smaller GPT-5.4 tiers when latency or cost matters more than maximum quality.
- `chat-latest` can change as OpenAI updates ChatGPT's default Instant model, so prefer pinned model IDs such as `gpt-5.5` or smaller tier models for production systems that need predictable behavior.

### Anthropic

Current positioning:
- Strong for long-horizon coding, document-heavy work, agentic execution, and instruction-following
- Especially strong when large context and stable behavior matter

Useful June 2026 reference points:
- Claude Fable 5 is Anthropic's most capable widely released model, built for the hardest reasoning, coding, vision, and long-horizon agentic work
- Claude Opus 4.8 is the current Opus-tier flagship and a practical premium default for complex reasoning, coding agents, and high-autonomy work
- Claude Sonnet 4.6 is the default Sonnet-tier recommendation for many users
- Claude Haiku 4.5 remains the fast, lower-cost tier
- Claude Mythos 5 has Fable-class capabilities but is limited-access through Project Glasswing and should not be treated as a normal production recommendation

What Anthropic is especially strong at:
- long-context reasoning
- coding agents
- instruction adherence
- vision-heavy knowledge work
- enterprise document workflows

Important caveat:
- Fable 5 has a 1M-token context window, up to 128k output tokens, and premium pricing at $10 per million input tokens and $50 per million output tokens.
- Fable 5 includes safety classifiers that can decline requests. In the Messages API, these return `stop_reason: "refusal"` as a successful HTTP 200 response, so integrations should explicitly handle refusal and fallback behavior.
- Opus 4.8 is often the cleaner Claude default when a team wants premium capability without Fable 5's special refusal handling, fallback design, or 30-day data-retention limitation.

### Google

Current positioning:
- Strong multimodal stack
- Strong value tiers
- Tight integration with Google products and developer tools

Useful June 2026 reference points:
- Gemini 3.1 Pro for harder reasoning-heavy tasks
- Gemini 3.5 Flash (`gemini-3.5-flash`) for stable, high-capability agentic, coding, and multimodal work where speed matters
- Gemini 3 Flash for high capability with speed
- Gemini 3.1 Flash-Lite for low-cost, high-volume workloads
- Nano Banana 2 for fast image generation and editing

What Google is especially strong at:
- multimodal workflows
- cost-effective high-volume deployments
- audio and live voice experiences
- integration with Workspace-adjacent and Google-native workflows

---

## 2. Open-Weight and Self-Hosted Options

These matter when privacy, customization, or volume economics outweigh absolute frontier performance.

### Meta (Llama Family)

Current positioning:
- Major open-weight family for self-hosting and customization
- Llama 4 introduced native multimodality and mixture-of-experts designs into the family

Useful June 2026 reference points:
- Llama 4 Scout
- Llama 4 Maverick

What Meta is especially strong at:
- self-hosted deployments
- ecosystem support
- fine-tuning and customization
- long-context experimentation

Important wording:
- Llama 4 is better described as **open-weight under the Llama Community License**, not as traditional open-source software.

### Mistral

Current positioning:
- Strong European vendor with both hosted and open-weight offerings
- Good fit for teams that want a mix of performance, deployment flexibility, and EU alignment

Useful June 2026 reference points from current docs:
- Mistral Large 3
- Mistral Medium 3.1
- Mistral Small 4
- Devstral 2
- Magistral Medium 1.2 and Magistral Small 1.2

What Mistral is especially strong at:
- open-weight multimodal options
- code-agent focused offerings
- EU-based vendor preference
- teams that want more deployment choice than the biggest U.S. platforms provide

---

# A Better Way to Compare Models

## Compare by Workflow, Not by Hype

### Best starting point for hard, general-purpose work

- OpenAI GPT-5.5
- Anthropic Claude Fable 5
- Anthropic Claude Opus 4.8
- Google Gemini 3.1 Pro

Use this bucket when:
- the task is high value
- quality matters more than cost
- you are still learning what "good" looks like

### Best for fast, lower-cost production routing

- OpenAI GPT-5.4 mini or nano
- Claude Haiku 4.5
- Gemini 3.5 Flash when you need stronger quality while staying below flagship-tier spend
- Gemini 3.1 Flash-Lite

Use this bucket when:
- latency matters
- you expect high request volume
- you want smaller models handling simpler sub-tasks

### Best for coding-heavy and agent workflows

- GPT-5.5
- GPT-5.4 mini for cheaper support work
- Claude Fable 5 for the hardest long-running work
- Claude Opus 4.8 for premium Claude coding and agent workflows
- Claude Sonnet 4.6
- Devstral 2 if you want an open-weight-oriented code-agent option

### Best for multimodal input

- Gemini 3.1 Pro
- Gemini 3.5 Flash
- Gemini 3 Flash
- GPT-5.5
- Claude Fable 5 or Opus 4.8 for image-plus-document heavy work

### Best for self-hosting and privacy-sensitive deployments

- Llama 4 family
- Mistral open-weight families

Use this bucket when:
- you need infrastructure control
- you need custom fine-tuning or deployment
- your economics favor running models yourself

---

# Cost Tiers

Exact pricing changes often, so think in tiers first.

## Premium Frontier Tier

- GPT-5.5
- GPT-5.5 Pro
- Claude Fable 5
- Claude Opus 4.8
- Gemini 3.1 Pro

Best when:
- request volume is modest
- task value is high
- errors are expensive

## Mid-Tier Workhorses

- Claude Sonnet 4.6
- Gemini 3.5 Flash
- Gemini 3 Flash
- Mistral Medium 3.1

Best when:
- you want strong quality but not maximum spend

## High-Volume / Cost-Efficient Tier

- GPT-5.4 mini
- GPT-5.4 nano
- Claude Haiku 4.5
- Gemini 3.1 Flash-Lite
- smaller open-weight deployments

Best when:
- volume is high
- latency matters
- you are comfortable with model routing

---

# Deployment Choices: Closed vs Open-Weight

## Closed Models

Examples:
- OpenAI
- Anthropic
- Google

Advantages:
- easiest to start
- strongest managed tooling
- usually best frontier quality
- no infrastructure burden

Tradeoffs:
- ongoing API cost
- less deployment control
- more vendor dependence

## Open-Weight Models

Examples:
- Llama family
- many Mistral models

Advantages:
- more control
- self-hosting possible
- easier fine-tuning and customization
- can make sense economically at scale

Tradeoffs:
- infrastructure complexity
- weaker out-of-the-box tooling
- often behind the closed frontier on absolute capability

Rule of thumb:
- Start with closed models unless privacy, cost structure, or deployment control clearly push you elsewhere.

---

# Practical Decision Framework

## Question 1: What is the task?

- Hard reasoning, coding, or professional work: start with a frontier flagship
- High-volume support, routing, or extraction: start with a smaller cheap model
- Image, audio, or multimodal workflows: favor Google or OpenAI, then test against Anthropic if document-heavy
- Self-hosted internal systems: start with Llama or Mistral families

## Question 2: What matters most?

- Best quality: use a flagship
- Best speed and cost: use a smaller tier
- Best privacy and control: use open-weight
- Best tool and agent ecosystem: lean OpenAI or Anthropic

## Question 3: Where will the system run?

- Browser app
- API-backed product
- coding agent
- internal workflow tool
- on-prem or private cloud

This matters because the same provider may expose different models and limits in each place.

## Question 4: How expensive are mistakes?

- High stakes: start with a stronger model, add retrieval, structured outputs, and evaluations
- Medium stakes: consider routing by difficulty
- Low stakes: optimize for cost and latency first

---

# Quick Reference

**I want to...**

Build a customer-support assistant:
- Start with Claude Sonnet 4.6, GPT-5.4 mini, or Gemini 3.1 Flash-Lite depending on quality and cost targets

Build a coding assistant:
- Start with GPT-5.5, Claude Fable 5, or Claude Opus 4.8, then use smaller models for sub-tasks if needed

Work across huge documents or large codebases:
- Start with GPT-5.5, Claude Fable 5, Claude Opus 4.8, or Sonnet 4.6 depending on budget, context needs, and operational constraints

Handle highly sensitive internal data:
- Consider open-weight deployment, private cloud, or enterprise contracts with strict data controls; do not assume Fable 5 fits zero-data-retention requirements

Build multimodal features:
- Start with Gemini 3.1 Pro, Gemini 3.5 Flash, or GPT-5.5, then compare against Claude Fable 5 or Opus 4.8 for image-plus-document tasks

Optimize cost at scale:
- Route simple tasks to GPT-5.4 nano, GPT-5.4 mini, Claude Haiku 4.5, or Gemini 3.1 Flash-Lite

Prototype quickly:
- Start with the strongest closed model you can justify, then optimize once you understand the task

---

> **Key Takeaway**
>
> Choosing an AI model is mostly a workflow decision, not a leaderboard decision.
>
> Start by matching the model to:
> - task difficulty
> - latency needs
> - budget
> - privacy constraints
> - deployment model
>
> In June 2026, a practical default looks like this:
> - flagship closed model for hard work
> - smaller cheaper model for routine work
> - open-weight model only when control or economics clearly justify it
>
> The best system is usually not one model. It is a routing strategy, an interface, and a verification loop built around the model.
