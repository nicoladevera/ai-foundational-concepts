# Multimodal AI: Beyond Text

**Learning goal:** Understand AI that works across images, audio, video, and combinations - expanding beyond text-only applications.

---

# What is Multimodal AI?

## Definition
**Multimodal AI** refers to systems that can understand and/or generate multiple types of content: text, images, audio, video, and combinations thereof.

## The Evolution

**Early AI (pre-2020):**
- Separate models for each modality
- Text model, image model, audio model - no connection

**Modern Multimodal AI (2020+):**
- Single model understands multiple types
- Can combine modalities (describe images, generate images from text)
- Unified understanding across formats

> 🌐 **Why this matters:** Humans naturally work across modalities - we read text, look at images, listen to audio, watch videos. Multimodal AI brings AI closer to how humans actually process information.

---

# The Modalities

## Text
Text-based AI (LLMs) covered in [02 - LLMs 101](./02%20-%20LLMs%20101.md).

## Images
1. **Image Generation** (text → image)
2. **Image Understanding** (image → text/analysis)

## Audio
1. **Speech-to-Text** (audio → text)
2. **Text-to-Speech** (text → audio)
3. **Music generation** (text/audio → audio)

## Video
1. **Video Understanding** (analyze/describe video)
2. **Video Generation** (text → video)

## Combined
Models that natively handle multiple modalities simultaneously

---

# Image Generation

## What It Is
AI that creates images from text descriptions ("text-to-image").

**Example:** "A serene mountain lake at sunset, realistic photography" → AI generates unique image

## Major Tools (December 2025)

### GPT Image 1.5 (OpenAI)
**Strengths:**
- Latest flagship image generation model (released December 16, 2025)
- 4x faster image generation than previous model
- Improved editing capabilities - changes only what you ask while maintaining consistency
- Better text rendering - handles denser and smaller text
- Keeps lighting, composition, and details consistent across edits
- Adheres to user intent more reliably
- Integrated creation space in ChatGPT with preset styles

**Best For:** Fast generation, precise editing, complex instructions, marketing materials, images with text
**Pricing:** ChatGPT Plus $20/month, available via API

### DALL-E 3 (OpenAI - Previous Model)
**Strengths:**
- Excellent at understanding complex prompts
- High quality, photorealistic outputs
- Easy via ChatGPT interface

**Best For:** Complex instructions, marketing materials
**Pricing:** ChatGPT Plus $20/month, API ~$0.04-0.12 per image

---

### Midjourney V7
**Strengths:**
- Industry-leading artistic quality and photorealism
- 25% faster than V6
- Enhanced personalization
- Full web interface (no longer Discord-only)

**Best For:** Professional artistic work, concept art, social media, cinematic imagery
**Pricing:** $10-60/month

---

### Stable Diffusion SDXL
**Strengths:**
- Open-source and free
- Run locally for privacy
- Highly customizable
- Full control over generation

**Best For:** Privacy projects, high-volume generation, custom fine-tuning, developers
**Pricing:** Free (pay for compute: ~$0.50-5/hour)

---

### Adobe Firefly
**Strengths:**
- Trained only on licensed content (copyright safe)
- Integrated into Adobe products
- Commercial use friendly

**Best For:** Commercial/enterprise use, Adobe users, copyright-conscious projects

---

> 🎨 **Choosing image generators:**
> - **Need speed & precision?** → GPT Image 1.5 (4x faster)
> - **Want artistic quality?** → Midjourney
> - **Need control/privacy?** → Stable Diffusion
> - **Corporate/commercial?** → Adobe Firefly

---

# Image Understanding

## What It Is
AI that can "see" and analyze images - describing content, answering questions, detecting objects.

## Major Tools (October 2025)

### GPT-4o/GPT-5.2 Vision (OpenAI)
**Capabilities:**
- Natively multimodal: text, images, and audio inputs
- Describe image content in detail
- Answer questions about images
- Advanced OCR (read text in images)
- Analyze charts, diagrams, screenshots
- GPT-5.2: 400k token context window, halved error rates in graph reasoning

**Best For:** General-purpose image analysis, multimodal applications, processing extensive visual documentation

---

### Gemini 3 Flash / Gemini 3 Pro Vision (Google)
**Capabilities:**
- Gemini 3 Flash: Latest default model (released December 17, 2025), 78% SWE-bench Verified
- Gemini 3 Pro: Flagship model (released November 18, 2025), "Best model in the world for multimodal understanding"
- Achieved 1501 Elo on LMArena (first model to surpass 1500)
- Natively multimodal: text, images, audio, and video
- 1M token context window (~11 hours audio or 1 hour video)
- Gemini 3 Flash: 90.4% on GPQA Diamond, 81.2% on MMMU-Pro
- Advanced visual reasoning with code execution capabilities
- Enhanced reasoning with Gemini 3 Deep Think mode
- Record benchmark scores across multiple tests

**Best For:** Complex multimodal tasks requiring highest performance, long video analysis, unified processing, agentic workflows

---

### Claude Opus 4.6 / Claude 4 Vision (Anthropic)
**Capabilities:**
- Claude Opus 4.6: Latest flagship with 1M token context window and 128k output (released February 5, 2026)
- Adaptive thinking feature (first for Anthropic)
- 68.8% on ARC AGI 2 reasoning benchmark
- 65.4% on Terminal-Bench, 72.7% on OSWorld
- Image understanding and analysis
- Strong at technical diagrams and code
- Extended thinking mode for reasoning

**Best For:** Technical document analysis, massive codebases (1M context), code-related visual tasks, complex reasoning

---

# Audio AI

## Speech-to-Text (STT)

### Major Tools
**OpenAI Whisper**
- State-of-the-art accuracy
- 99 languages
- Handles accents, background noise
- Open-source (can run locally)
- Pricing: ~$0.006 per minute

**Google Speech-to-Text**
- Real-time streaming
- 125+ languages
- Pricing: ~$0.006-0.024 per minute

**Assembly AI**
- Excellent accuracy
- Speaker diarization (who said what)
- Best for podcasts, meetings

---

## Text-to-Speech (TTS)

### Major Tools (December 2025)

**ElevenLabs V3** - Industry Leader
- Most expressive model (voices that sigh, whisper, laugh)
- 29 languages with emotion
- Voice cloning with customization
- Best for professional content creation
- Pricing: $5-330/month

**Fish Audio 4B**
- Ranked #1 on TTS-Arena leaderboard
- Best AI text-to-speech available
- Emerging as top competitor

**OpenAI TTS**
- Two models: TTS and TTS HD
- Real-time streaming
- Easy API integration
- Pricing: ~$15 per million characters

---

## Music Generation

**Suno**
- Generate full songs from text prompts
- Vocals, instruments, arrangement

**Udio**
- Similar to Suno
- High-quality music generation

**Stable Audio**
- Open-source option
- Sound effects and music

---

# Video AI

## Video Understanding

### Gemini 3 Flash / Gemini 3 Pro / Gemini 2.5 Pro
- Analyze entire videos (up to 1 hour)
- Answer questions about content
- Find specific moments
- Summarize long videos
- Gemini 3 Flash: Default model (released December 17, 2025), 3x faster than 2.5 Pro with frontier-level performance
- Gemini 3 Pro offers enhanced multimodal understanding (1501 LMArena Elo)

**Example:** Upload meeting recording, ask "What were the action items?", get timestamped list

---

## Video Generation (December 2025)

### Sora 2.0 (OpenAI)
- Sets standard for photorealism
- 4K support added August 2025
- 5-minute processing time
- Best for premium content
- Pricing: $200/month (Pro subscribers)
- Limitation: Slower than competitors

### Runway Gen-3/Gen-4
- September 2025: Added "Motion Brush"
- August 2025: Multi-shot generation
- Most comprehensive creative toolkit
- Best for professionals needing control
- Pricing: $15+/month

### Pika Labs 2.5
- 30-second generation time (fastest)
- Best value proposition
- Best for creators just starting
- Pricing: $10/month

### Veo 2 (Google DeepMind)
- Most realistic outputs alongside Sora
- Competes on quality

---

### Current Limitations (December 2025)
Video generation has matured but still has constraints:
- **Length:** Most generate 10-60 second clips
- **Processing time:** 30 seconds (Pika) to 5 minutes (Sora)
- **Cost:** $10-200/month
- **Quality variation:** Output depends on prompt and model

**Major 2025 Improvements:**
- Multi-shot generation with consistent styling
- Motion control tools
- Better photorealism
- 4K resolution support
- Faster generation times

---

# Combined Multimodal Models

## GPT-5.3-Codex & GPT-5.2 (OpenAI)
**Modalities:** Text + Images + Audio (natively multimodal)

**Capabilities:**
- GPT-5.3-Codex: Latest flagship agentic coding model (released February 5, 2026)
- 77.3% on Terminal-Bench 2.0, 64.7% on OSWorld-Verified
- 25% faster with combined coding + reasoning + professional knowledge
- First OpenAI model that helped build itself
- Natively processes text, images, and voice together
- GPT-5.2: 400,000 token context window (3.1x larger than GPT-5.1)
- Chat with images in context
- Analyze and reason about images
- Halved error rates in multimodal tasks (graph reasoning, interface navigation)
- 38% fewer hallucinations than previous generation
- More natural interaction across modalities

**Best For:** Agentic coding workflows, general-purpose multimodal applications, processing large volumes of visual + text content

---

## Gemini 3 Flash / Gemini 3 Pro (Google)
**Modalities:** Text + Images + Video + Audio (all natively)

**Key Innovation:** Highest performing multimodal models (1501 LMArena Elo, first to surpass 1500)

**Capabilities:**
- Gemini 3 Flash: Default model (released December 17, 2025), frontier intelligence built for speed
- Gemini 3 Pro: "Best model in the world for multimodal understanding" (released November 18, 2025)
- Only models handling ALL major modalities natively together
- 1M token context window (11 hours audio or 1 hour video)
- Gemini 3 Flash: 78% SWE-bench Verified, 90.4% GPQA Diamond, 81.2% MMMU-Pro
- 3x faster than 2.5 Pro while outperforming it
- Advanced visual reasoning with code execution capabilities
- Enhanced reasoning with Gemini 3 Deep Think mode
- Record benchmark scores across multiple tests
- True multimodal understanding
- Highly competitive pricing: Gemini 3 Pro $2/$12, Gemini 3 Flash $0.50/$3.00 per million tokens

**Best For:** Complex multimodal tasks requiring highest performance, video understanding, unified processing, cost-conscious deployments, fast agentic workflows

---

## Claude Opus 4.6 (Anthropic)
**Modalities:** Text + Images

**Capabilities:**
- 1M token context window, 128k output (released February 5, 2026)
- Adaptive thinking (first for Anthropic)
- 68.8% on ARC AGI 2, 65.4% on Terminal-Bench, 72.7% on OSWorld
- Extended thinking mode
- Strong at technical content
- Agent teams for parallel task execution

**Best For:** Massive codebases (1M context), technical document analysis, complex reasoning tasks, code-related visual tasks

---

## Llama 4 (Meta)
**Modalities:** Text + Images + Video (multimodal)

**Significance:** Open-source model with multimodal support

---

## Why Multimodal Matters

**Single interface for all content types:**
- Don't switch between tools
- Natural conversations mixing modalities
- Context persists across different content

**Richer understanding:**
- Combine text with visual content
- Explain images with words
- Analyze relationships between modalities

**New applications:**
- Accessibility (describe images for blind users)
- Education (explain diagrams, charts)
- Healthcare (analyze medical images + records)
- Customer service (understand product photos + questions)

> 🤝 **The future is multimodal:** Just as humans combine sight, sound, and text, AI is moving toward models that naturally handle all modalities. Single-modality models will become specialized tools, while multimodal models become the default.

---

# Comparison Table (February 2026)

| **Modality** | **Task** | **Best Tools (2026)** | **Maturity** | **Cost** |
|---|---|---|---|---|
| **Text** | Generation, analysis | GPT-5.3-Codex, Claude Opus 4.6, Gemini 3 Flash/Pro | Very Mature | $ |
| **Image** | Generation | GPT Image 1.5, Midjourney V7, SDXL | Very Mature | $ - $$ |
| **Image** | Understanding | Gemini 3 Flash/Pro, GPT-5.3-Codex, Claude Opus 4.6 | Very Mature | $ |
| **Audio** | Speech-to-Text | Whisper, Google STT | Very Mature | $ |
| **Audio** | Text-to-Speech | ElevenLabs V3, Fish Audio 4B, OpenAI | Very Mature | $ - $$ |
| **Audio** | Music Generation | Suno, Udio, Stable Audio | Mature | $$ |
| **Video** | Understanding | Gemini 3 Flash, Gemini 3 Pro | Mature | $ |
| **Video** | Generation | Sora 2.0, Runway Gen-3/4, Pika 2.5, Veo 2 | Maturing | $$ - $$$ |
| **Combined** | Multi-input/output | GPT-5.3-Codex, Claude Opus 4.6, Gemini 3 Flash, Gemini 3 Pro, Llama 4 | Very Mature | $ - $$ |

> 📈 **February 2026 Progress:** Every modality continues maturing rapidly. February 5, 2026 brought major releases: Anthropic's Claude Opus 4.6 extends context to 1M tokens with adaptive thinking, while OpenAI's GPT-5.3-Codex sets new industry highs with 77.3% Terminal-Bench. Image generation remains production-ready with GPT Image 1.5's 4x speed. Google's Gemini 3 Flash combines frontier-level performance (78% SWE-bench, 90.4% GPQA Diamond) with 3x speed at competitive pricing. Combined multimodal models now feature unprecedented context windows (1M tokens), adaptive reasoning, and agentic capabilities.

---

# Practical Applications

## E-Commerce
- Generate product images (DALL-E, Midjourney)
- Visual search ("Find products like this image")
- Customer service (identify products from photos)

## Healthcare
- Analyze medical imaging
- Accessibility (describe documents for visually impaired)
- Transcribe doctor-patient conversations

## Education
- Generate image descriptions for blind students
- TTS for reading assignments
- Real-time lecture transcription
- Create custom illustrations

## Media & Entertainment
- Generate concept art
- Automatic transcription/subtitles
- Highlight generation
- Background music generation

---

# Future Trends

## 1. True Multimodal Native Models
**Current:** Most convert non-text to text, process, convert back
**Future:** Models that natively understand relationships between modalities

## 2. Real-Time Multimodal Interaction
**Current:** Process video/audio in batches
**Future:** Real-time processing and generation

## 3. Longer Video Generation
**Current:** 3-10 second clips
**Future:** Full-length videos with consistency

## 4. Personalized Multimodal Models
**Current:** One-size-fits-all
**Future:** Models that learn your visual preferences, voice, style

## 5. Cross-Modal Generation
**Current:** Limited (text→image)
**Future:** Any modality to any modality (Image→Music, Audio→Video)

---

# Quick Reference

**I want to...**

🖼️ **...generate images** → GPT Image 1.5 (4x faster, best editing), Midjourney (artistic), Stable Diffusion (control)

👁️ **...analyze images** → Gemini 3 Flash (fastest + frontier performance), GPT-5.3-Codex (agentic coding), Claude Opus 4.6 (1M context + technical)

🎤 **...transcribe audio** → Whisper (best accuracy), Google STT (real-time)

🔊 **...generate speech** → ElevenLabs (quality), Fish Audio 4B (#1 leaderboard), OpenAI TTS (balance)

🎵 **...create music** → Suno, Udio

🎬 **...generate video** → Sora 2.0 (premium), Runway (creative), Pika (value)

📹 **...analyze video** → Gemini 3 Flash (default, 3x faster), Gemini 3 Pro (highest performance)

🌍 **...work across modalities** → Gemini 3 Flash (best value + speed), Gemini 3 Pro (record benchmarks), Claude Opus 4.6 (1M context + adaptive thinking), GPT-5.3-Codex (agentic coding)

---

> 🎯 **Key Takeaway** (Updated February 2026)
>
> Multimodal AI reached new milestones in early 2026 with major releases on February 5:
>
> **Current State:**
> - **Text:** Very mature (GPT-5.3-Codex, Claude Opus 4.6, Gemini 3 Flash/Pro)
> - **Images:** Very mature for generation and understanding
> - **Audio:** Very mature for speech, mature for music
> - **Video:** Maturing rapidly - 2025-2026 brought massive improvements
> - **Combined:** Very mature (models now feature 1M context, adaptive thinking, agentic capabilities)
>
> **February 2026 Releases:**
> - **Claude Opus 4.6** (Feb 5): 1M token context, adaptive thinking, 68.8% ARC AGI 2, agent teams
> - **GPT-5.3-Codex** (Feb 5): 77.3% Terminal-Bench, 25% faster, first model that helped build itself
>
> **Practical Guidance:**
> - **For generation:**
>   - Images: GPT Image 1.5 (4x faster + precision), Midjourney V7 (artistic), SDXL (control)
>   - Voice: ElevenLabs V3 (best quality), Fish Audio 4B (#1 leaderboard)
>   - Video: Sora 2.0 (premium), Runway Gen-3/4 (creative), Pika 2.5 (value)
> - **For understanding:**
>   - Best value: Gemini 3 Flash (fastest + frontier performance + affordable)
>   - Best multimodal: Gemini 3 Pro (highest performance + all modalities + 1M context)
>   - Largest context: Claude Opus 4.6 (1M tokens + adaptive thinking)
>   - Best agentic coding: GPT-5.3-Codex (77.3% Terminal-Bench + 25% faster)
>   - Best reasoning: Claude Opus 4.6 (68.8% ARC AGI 2)
>
> **The February 2026 Reality:**
> Multimodal AI continues accelerating with February 5 releases. Claude Opus 4.6 extends context to 1 million tokens with adaptive thinking, enabling unprecedented analysis of massive codebases and documents. GPT-5.3-Codex sets new industry highs on agentic coding benchmarks (77.3% Terminal-Bench) while being 25% faster. Google's Gemini 3 Flash continues offering best value (78% SWE-bench, 90.4% GPQA Diamond) at 3x speed. These advances signal AI that seamlessly processes text, images, audio, and video with human-level reasoning and execution.
>
> **What's Next (2026 Trends):**
> - Even larger context windows (beyond 1M tokens)
> - Full-length video generation with perfect consistency
> - Real-time multimodal interaction becomes standard
> - Adaptive reasoning across all modalities
> - Even higher benchmark scores and more affordable pricing
>
> **Remember:** Every modality is production-ready. Gemini 3 Flash offers best value and speed, Claude Opus 4.6 for massive context and reasoning, GPT-5.3-Codex for agentic coding, Gemini 3 Pro for record multimodal performance, GPT Image 1.5 for fast image generation. Match the modality and tool to the task for optimal results.
