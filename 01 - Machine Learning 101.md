# Machine Learning 101

**Learning goal:** Understand the foundational technology behind modern AI - from traditional ML to deep learning to LLMs.

---

# What is Machine Learning?

## Simple Definition

**Machine Learning (ML)** is a way of teaching computers to make decisions or predictions by showing them examples, rather than explicitly programming every rule.

## The Key Difference

**Traditional Programming:**
- Humans write explicit rules
- Computer follows those rules exactly
- Same input always produces same output
- Example: "If temperature < 68°F, turn on heater"

**Machine Learning:**
- Humans provide examples (data)
- Computer finds patterns in the examples
- Computer creates its own rules based on patterns
- Example: Show the computer 10,000 photos labeled "cat" or "dog" - it learns to tell them apart without you writing rules for whiskers, ears, etc.

> 💡 **The Breakthrough:** Instead of telling computers HOW to do something step-by-step, we show them EXAMPLES and let them figure out the pattern.

## Real-World Analogy

**Traditional Programming** is like teaching someone to cook by giving them a recipe with exact measurements and steps.

**Machine Learning** is like teaching someone to cook by having them taste 1,000 different dishes and learn what "good" tastes like, then letting them create their own recipes.

---

# The Learning Process

## How Machines "Learn"

Machine learning isn't magic - it's sophisticated pattern recognition and statistical analysis. Here's what actually happens:

## Step 1: Collect Training Data

Gather examples of what you want the machine to learn.

**Example:** To build a spam email detector, collect 100,000 emails labeled as "spam" or "not spam"

## Step 2: Extract Features

**Features** are measurable characteristics that help make predictions.

**Example for spam detection:**
- Number of exclamation marks
- Presence of words like "FREE" or "URGENT"
- Sender's email domain
- Length of email
- Number of links

## Step 3: Train the Model

The algorithm analyzes the training data to find patterns that connect features to outcomes.

**What's happening:** The model adjusts internal parameters (weights) to minimize errors in its predictions.

**Analogy:** Like a student studying for an exam - they review examples, test themselves, see what they got wrong, and adjust their understanding.

## Step 4: Evaluate Performance

Test the model on NEW data it hasn't seen before to see how well it learned.

**Example:** After training on 80,000 emails, test it on the remaining 20,000 to see if it correctly identifies spam.

## Step 5: Deploy and Monitor

Use the model in the real world and continue monitoring its performance.

**Important:** Models can degrade over time if patterns change (spam tactics evolve, language shifts, etc.)

> ⚙️ **Key Insight:** The model never "understands" what spam is. It has learned statistical patterns that correlate with spam vs. non-spam based on the examples it saw.

---

# Types of Machine Learning

## 1. Supervised Learning

### What It Is

Learning from labeled examples - you show the algorithm the input AND the correct answer.

**Analogy:** Like studying with an answer key - you see the question and the correct answer.

### How It Works

1. Provide data with labels (inputs + correct outputs)
2. Algorithm learns the relationship between inputs and outputs
3. Can then predict outputs for new, unseen inputs

### Common Tasks

**Classification:** Categorizing things into groups
- Is this email spam or not spam?
- Is this image a cat, dog, or bird?
- Will this customer churn or stay?

**Regression:** Predicting numerical values
- What will this house sell for?
- How many products will we sell next month?
- What will the temperature be tomorrow?

### Real-World Examples

- **Netflix recommendations** - Learning from what you watched and rated
- **Credit score predictions** - Learning from historical loan data
- **Medical diagnosis** - Learning from labeled patient cases
- **Voice recognition** - Learning from audio paired with transcripts

### Tools & Platforms

- **Scikit-learn** - Python library for traditional supervised learning
- **XGBoost** - Popular for competitions and business applications
- **Amazon SageMaker** - Cloud platform for building ML models
- **Google AutoML** - Automated ML for non-experts

---

## 2. Unsupervised Learning

### What It Is

Learning from unlabeled data - you show the algorithm inputs WITHOUT telling it the correct answer. It finds hidden patterns on its own.

**Analogy:** Like sorting a huge pile of mixed items without instructions - you notice some items are similar and group them.

### How It Works

1. Provide data without labels (just inputs)
2. Algorithm finds structure, patterns, or groupings
3. Discovers relationships humans might not have noticed

### Common Tasks

**Clustering:** Grouping similar things together
- Customer segmentation (finding groups of similar customers)
- Document organization (grouping related articles)
- Anomaly detection (finding outliers)

**Dimensionality Reduction:** Simplifying complex data
- Compressing images
- Visualizing high-dimensional data
- Removing redundant features

**Association:** Finding items that occur together
- Market basket analysis ("people who bought X also bought Y")
- Recommendation systems

### Real-World Examples

- **Customer segmentation** - Grouping customers by behavior without predefined categories
- **Fraud detection** - Finding unusual patterns that might indicate fraud
- **Genomics** - Discovering relationships between genes
- **Topic modeling** - Automatically discovering themes in document collections

### Tools & Platforms

- **Scikit-learn** - Clustering, PCA, and more
- **TensorFlow** - Deep learning approaches to unsupervised learning
- **DBSCAN** - Density-based clustering algorithm

---

## 3. Reinforcement Learning

### What It Is

Learning by trial and error - the algorithm takes actions and learns from rewards or penalties.

**Analogy:** Like training a dog - it tries different behaviors, and you give treats for good behavior and corrections for bad behavior.

### How It Works

1. Agent (the learner) exists in an environment
2. Agent takes actions
3. Environment provides feedback (rewards or penalties)
4. Agent learns which actions lead to the best long-term rewards

### Key Difference

Unlike supervised learning (where you show correct answers), reinforcement learning figures out the best actions through experience.

### Real-World Examples

- **Game playing AI** - AlphaGo, chess engines, video game bots
- **Robotics** - Teaching robots to walk, grasp objects, navigate
- **Autonomous vehicles** - Learning optimal driving strategies
- **Resource optimization** - Data center cooling, traffic light timing
- **Finance** - Algorithmic trading strategies

### Tools & Platforms

- **OpenAI Gym** - Environment for developing RL algorithms
- **Ray RLlib** - Scalable reinforcement learning
- **Unity ML-Agents** - RL for game development

---

# Traditional ML vs. Deep Learning vs. LLMs

Understanding the evolution helps clarify where different technologies fit.

## Traditional Machine Learning

### Characteristics

- Requires humans to manually select features
- Works well with structured, tabular data
- Models are relatively simple and interpretable
- Needs less data and computing power
- Faster to train

### Common Algorithms

- **Decision Trees** - Series of yes/no questions
- **Random Forests** - Many decision trees voting together
- **Support Vector Machines (SVM)** - Finding boundaries between categories
- **Linear/Logistic Regression** - Drawing lines to separate or predict
- **K-Means Clustering** - Grouping similar items

### Best For

- Structured data (spreadsheets, databases)
- Problems where you can identify relevant features
- Situations requiring model interpretability
- Smaller datasets (thousands to millions of examples)

### Real-World Tools

- **Scikit-learn** - Most popular Python library for traditional ML
- **R (caret, mlr)** - Statistical computing for ML
- **H2O.ai** - Enterprise ML platform
- **WEKA** - Java-based ML workbench

---

## Deep Learning

### What It Is

A subset of machine learning using artificial neural networks with multiple layers. Inspired by how the human brain processes information.

### Key Innovation

**Automatic feature learning** - Instead of humans selecting features, the neural network learns which features matter through its layers.

**Example:**
- Traditional ML for image recognition: You manually define features (edges, corners, colors)
- Deep Learning: Show images, the network automatically learns to detect edges in layer 1, shapes in layer 2, objects in layer 3

### Characteristics

- Multiple layers of artificial neurons
- Learns features automatically from raw data
- Excels at unstructured data (images, audio, text)
- Requires massive amounts of data
- Needs significant computing power (GPUs)
- Less interpretable ("black box")

### Common Architectures

- **Convolutional Neural Networks (CNNs)** - For images and video
- **Recurrent Neural Networks (RNNs)** - For sequences (time series, text)
- **Transformers** - Modern architecture for language (foundation of LLMs)
- **Generative Adversarial Networks (GANs)** - For generating new data

### Best For

- Unstructured data (images, audio, text, video)
- Complex patterns humans can't easily define
- Large datasets (millions to billions of examples)
- Tasks requiring human-like perception

### Real-World Tools

- **TensorFlow** - Google's deep learning framework
- **PyTorch** - Facebook's deep learning framework (popular in research)
- **Keras** - High-level API, easy to use
- **Fast.ai** - Making deep learning more accessible

---

## Large Language Models (LLMs)

### What They Are

**LLMs are a specific application of deep learning**, trained on massive amounts of text using the Transformer architecture.

> 🔗 **Connection to ML:** LLMs represent the current cutting edge of machine learning, combining:
> - **Supervised learning** (predicting next words)
> - **Unsupervised learning** (finding patterns in text)
> - **Deep learning** (neural networks with billions of parameters)
> - **Reinforcement learning** (often fine-tuned with human feedback - RLHF)

### Key Characteristics

- Trained on billions of text examples from the internet
- Billions to trillions of parameters (model weights)
- Can generate human-like text
- Transfer learning - one model, many tasks
- Emergent abilities appear at large scale

### How They Fit in the ML Landscape

**Traditional ML:** Predict house prices from square footage, bedrooms, location

**Deep Learning (CNNs):** Recognize objects in images

**Deep Learning (RNNs):** Translate sentences between languages

**LLMs (Transformers):** Generate human-like text, answer questions, write code, summarize documents, and much more - all from one model

### The Innovation

Previous ML required training a separate model for each task. LLMs can perform hundreds of different tasks using the same model, often with just instructions (prompts).

### Examples

- **GPT-5.2** (OpenAI) - Latest model powering ChatGPT, 400k context (released December 2025)
- **GPT-5.2-Codex** (OpenAI) - Agentic coding model, 56.4% SWE-bench Pro (released December 2025)
- **GPT-5.1** (OpenAI) - Previous flagship with adaptive reasoning (released November 2025)
- **Claude Opus 4.5** (Anthropic) - Best coding model, powers Claude Code (released November 2025)
- **Gemini 3 Pro** (Google) - Highest performing multimodal LLM (released November 2025)
- **Llama 4** (Meta) - Open-source multimodal LLM

> 📚 **Learn More:** For a deeper dive into how LLMs work, see [02 - LLMs 101](./02%20-%20LLMs%20101.md).

---

# Comparison Table

| **Aspect** | **Traditional ML** | **Deep Learning** | **LLMs** |
|---|---|---|---|
| **Feature Engineering** | Manual (humans select features) | Automatic (learns features) | Automatic (learns language patterns) |
| **Data Needs** | Thousands to millions | Millions to billions | Billions of text examples |
| **Computing Power** | Low (CPU is fine) | High (needs GPUs) | Extremely high (clusters of GPUs) |
| **Training Time** | Minutes to hours | Hours to days | Weeks to months |
| **Interpretability** | High (can see decision rules) | Low (black box) | Very low (emergent behaviors) |
| **Best Data Type** | Structured (tables) | Unstructured (images, audio, text) | Text (also multimodal) |
| **Example Use Cases** | Fraud detection, price prediction | Image recognition, speech-to-text | Writing, coding, reasoning, conversation |
| **Cost** | $ (Low) | $$ (Medium) | $$$ (Very High) |
| **Specialization** | One task per model | One task per model | Many tasks from one model |

---

# Key ML Concepts Explained

## Training Data

**Definition:** The examples used to teach the machine learning model.

**Quality matters more than quantity:** A model trained on biased, incomplete, or incorrect data will make biased, incomplete, or incorrect predictions.

**The Data Quality Rule:** "Garbage in, garbage out"

**Example:** If you train a hiring model on historical data where most engineers hired were men, it may learn to favor male candidates - perpetuating bias.

## Features

**Definition:** Measurable characteristics used to make predictions.

**Example - Predicting House Prices:**
- Features: Square footage, number of bedrooms, location, age, school district
- Target: Sale price

**In traditional ML:** Humans select features
**In deep learning:** The model learns which features matter

## Model

**Definition:** The mathematical representation of patterns learned from data.

**Analogy:** Like a formula or recipe that takes inputs and produces outputs based on learned patterns.

**Example:** A spam filter model takes email characteristics as input and outputs "spam" or "not spam"

## Parameters (Model Weights)

**Definition:** The internal values the model learns during training that determine how it makes predictions.

**More parameters ≈ more capacity to learn complex patterns** (but also requires more data and computing)

**Scale:**
- Traditional ML: Hundreds to thousands of parameters
- Deep Learning: Millions to billions of parameters
- LLMs: Billions to trillions of parameters (GPT-4 has ~1.7 trillion; newer models like GPT-5.2, GPT-5.1, Claude Opus 4.5, and Gemini 3 Pro have undisclosed parameter counts)

## Training vs. Inference

**Training:** The process of learning from data (happens once or periodically)
- Expensive (time, computing, data)
- Happens on powerful servers

**Inference:** Using the trained model to make predictions (happens constantly)
- Relatively cheap
- Can happen on less powerful hardware
- What you're doing when you use ChatGPT

## Overfitting vs. Underfitting

**Overfitting:** Model memorizes training data but fails on new data
- Like a student who memorizes practice test answers but doesn't understand concepts
- Solution: More data, simpler model, regularization

**Underfitting:** Model is too simple to capture patterns
- Like using a straight line to describe a curved relationship
- Solution: More complex model, better features

**The Goal:** Generalization - performing well on new, unseen data

## Accuracy vs. Precision vs. Recall

Common metrics for evaluating classification models:

**Accuracy:** What percentage of predictions were correct overall?
- Simple but can be misleading with imbalanced data

**Precision:** Of the items predicted as positive, how many actually were?
- "When the model says yes, how often is it right?"

**Recall:** Of all the actual positive items, how many did we find?
- "How many of the real positives did we catch?"

**Example - Email Spam Filter:**
- High precision: Few legitimate emails marked as spam (low false positives)
- High recall: Catches most spam emails (low false negatives)
- Trade-off: Being too aggressive catches more spam but blocks legitimate emails

## Fine-Tuning

**Definition:** Taking a pre-trained model and training it further on specialized data for a specific task.

**Why it works:** The model already learned general patterns, now you're teaching it domain-specific knowledge.

**Analogy:** A doctor (general medical training) doing a residency in cardiology (specialization)

**Example:** Taking GPT-5.2 and fine-tuning it on legal documents to create a legal research assistant

**Benefit:** Much faster and cheaper than training from scratch

## Transfer Learning

**Definition:** Using knowledge learned from one task to help with a different but related task.

**Example:** A model trained to recognize objects in photos can be fine-tuned to recognize medical conditions in X-rays

**This is why LLMs are so powerful:** They learn general language understanding, then can be adapted to countless specific tasks

---

# Real-World ML Applications by Industry

## Healthcare

**Supervised Learning:**
- Disease diagnosis from medical images
- Predicting patient readmission risk
- Drug discovery and development

**Unsupervised Learning:**
- Finding patient subgroups with similar conditions
- Anomaly detection in vital signs monitoring

**Tools:** IBM Watson Health, PathAI, Tempus

## Finance

**Supervised Learning:**
- Credit scoring and loan approval
- Fraud detection
- Stock price prediction

**Unsupervised Learning:**
- Customer segmentation for marketing
- Unusual transaction detection

**Reinforcement Learning:**
- Algorithmic trading

**Tools:** Kensho, DataRobot, Numerai

## Retail & E-Commerce

**Supervised Learning:**
- Demand forecasting
- Price optimization
- Customer churn prediction

**Unsupervised Learning:**
- Product recommendations
- Market basket analysis

**Tools:** Amazon Personalize, Google Analytics, Dynamic Yield

## Manufacturing

**Supervised Learning:**
- Predictive maintenance (predicting equipment failure)
- Quality control and defect detection

**Unsupervised Learning:**
- Anomaly detection in sensor data

**Tools:** GE Predix, Sight Machine, Uptake

## Marketing

**Supervised Learning:**
- Customer lifetime value prediction
- Ad click-through rate prediction
- Lead scoring

**Unsupervised Learning:**
- Customer segmentation
- Campaign performance analysis

**Tools:** HubSpot, Salesforce Einstein, Adobe Sensei

## Transportation

**Supervised Learning:**
- Route optimization
- Demand prediction (Uber, Lyft)

**Reinforcement Learning:**
- Autonomous vehicle navigation

**Tools:** Waymo, Tesla Autopilot, Mobileye

---

# How ML Connects to Other AI Concepts

## ML → LLMs

Large Language Models are a specific application of machine learning, specifically deep learning with Transformers.

**What LLMs learned:** Patterns in billions of text examples

**How they use it:** Generate human-like text, answer questions, write code

Read more in [02 - LLMs 101](./02%20-%20LLMs%20101.md)

## ML → Embeddings

**Embeddings** are vector representations of data (text, images) that capture semantic meaning - a key ML technique.

**How they're created:** Neural networks trained to place similar items close together in vector space

**Why they matter:** Enable semantic search, recommendations, and RAG (Retrieval-Augmented Generation)

## ML → AI Agents

AI Agents use ML models (often LLMs) as their "brain" to make decisions and take actions.

**The ML component:** The model that understands language and generates responses

**The agent component:** The system that decides which tools to use and when

Read about [07 - Automation, AI Workflows, and AI Agents](./07%20-%20Automation,%20AI%20Workflows,%20and%20AI%20Agents.md)

## ML → Fine-Tuning

Fine-tuning is a machine learning technique where you take a pre-trained model and continue training it on specialized data.

**Example:** Fine-tuning GPT-5.1 on your company's documentation to create a company-specific assistant

## ML → Context Engineering

While context engineering is about what information you provide to an LLM, it's informed by understanding how ML models process information.

**ML insight:** Models can only work with data they can "see" (context window)

**Application:** Strategic selection of relevant information to include

Read about [04 - Context Engineering vs Prompt Engineering](./04%20-%20Context%20Engineering%20vs%20Prompt%20Engineering.md)

---

# Important Limitations & Considerations

## 1. Data Quality and Bias

**The Problem:** ML models learn from data. If the data is biased, the model will be biased.

**Examples:**
- Facial recognition systems trained mostly on white faces perform poorly on darker skin tones
- Hiring algorithms trained on historical data can perpetuate gender or racial bias
- Language models trained on internet text can reflect societal biases and stereotypes

**What to do:**
- Audit training data for representativeness
- Test models across different demographic groups
- Use diverse teams when building ML systems
- Implement bias detection and mitigation techniques

## 2. The "Black Box" Problem

**The Problem:** Complex ML models (especially deep learning) are difficult to interpret.

**Why it matters:** Hard to understand WHY a model made a specific decision

**Example:** A loan is denied by an ML model, but the bank can't explain exactly why (regulatory/ethical issue)

**What to do:**
- Use interpretable models when possible (decision trees, linear regression)
- Employ explainability techniques (SHAP, LIME) for complex models
- Don't use black box models for high-stakes decisions without human oversight

## 3. Data Requirements

**The Problem:** Good ML requires lots of high-quality labeled data, which is expensive and time-consuming to collect.

**Scale needed:**
- Traditional ML: Thousands to millions of examples
- Deep Learning: Millions to billions of examples

**What to do:**
- Consider if you have enough data before starting
- Use transfer learning and pre-trained models when possible
- Explore data augmentation techniques
- Consider if traditional programming would work just as well

## 4. Overfitting and Generalization

**The Problem:** Models that perform great on training data but fail on new data.

**Why it happens:** Model memorized training examples instead of learning general patterns

**What to do:**
- Always test on separate test data
- Use cross-validation
- Regularization techniques
- Collect more diverse training data

## 5. Concept Drift

**The Problem:** The world changes, but your model was trained on old data.

**Example:** A fraud detection model trained in 2020 may not catch 2025 fraud tactics

**What to do:**
- Monitor model performance over time
- Retrain models periodically on fresh data
- Set up alerts when accuracy drops
- Consider online learning (continuous updates)

## 6. Computational Costs

**The Problem:** Training large ML models requires significant computing resources and energy.

**Scale:**
- Training GPT-3 cost an estimated $4-12 million in computing
- Large models have substantial carbon footprints

**What to do:**
- Consider if you need to train from scratch or can use existing models
- Use efficient architectures
- Take advantage of transfer learning
- Consider environmental impact

## 7. Adversarial Attacks

**The Problem:** Small, intentional changes to input can fool ML models.

**Example:** Adding specific stickers to a stop sign can make a self-driving car misclassify it

**What to do:**
- Test models with adversarial examples
- Use robust training techniques
- Implement monitoring and safety checks
- Don't rely solely on ML for critical safety systems

---

# Getting Started with ML

## For Non-Technical Users

**No-Code Platforms:**
- **Google AutoML** - Automated ML with minimal coding
- **Microsoft Azure ML Studio** - Visual interface for ML
- **Amazon SageMaker Canvas** - No-code ML for business analysts
- **Obviously AI** - Build ML models from spreadsheets
- **DataRobot** - Enterprise automated ML

**Best for:** Business analysts, product managers, marketers who want to use ML without programming

## For Beginners with Some Technical Background

**Learning Paths:**
1. **Andrew Ng's ML Course** (Coursera) - Classic introduction
2. **Fast.ai** - Practical deep learning for coders
3. **Google ML Crash Course** - Free, interactive learning
4. **Kaggle Learn** - Hands-on micro-courses

**Tools to start with:**
- **Scikit-learn** - Traditional ML in Python (easiest to start)
- **Keras** - User-friendly deep learning
- **Google Colab** - Free cloud notebooks with GPUs

## For Technical Practitioners

**Frameworks:**
- **TensorFlow** - Industry standard, Google's framework
- **PyTorch** - Research favorite, growing in industry
- **Scikit-learn** - Traditional ML algorithms
- **XGBoost/LightGBM** - Gradient boosting for tabular data

**Resources:**
- **Papers with Code** - Latest research with implementations
- **Kaggle Competitions** - Practice on real datasets
- **MLOps tools** - MLflow, Weights & Biases, Neptune.ai

---

# Common Misconceptions

## "AI and ML are the same thing"

❌ **False.** ML is a subset of AI.

- **AI (Artificial Intelligence):** Broad field of making computers do things that would require intelligence if done by humans
- **ML (Machine Learning):** Specific approach to AI that learns from data
- **Other AI approaches:** Rule-based systems, expert systems, search algorithms

## "You need a PhD to do ML"

❌ **False.** While research requires deep expertise, many practical ML applications are accessible to developers and analysts.

**Modern tools make ML more accessible:**
- No-code platforms for business users
- High-level libraries (Keras, FastAI) for developers
- Pre-trained models for common tasks
- Cloud services handle infrastructure

## "More data always makes models better"

❌ **Partially false.** Data quality matters more than quantity.

- 10,000 high-quality, representative examples > 1,000,000 biased, noisy examples
- Beyond a certain point, more data has diminishing returns
- "Big data" without good data practices is just "big garbage"

## "ML models are objective because they're mathematical"

❌ **False.** ML models reflect biases in their training data and design choices.

- Training data reflects human biases
- Feature selection involves human judgment
- Evaluation metrics embody value choices
- Deployment decisions have ethical implications

## "Once trained, an ML model works forever"

❌ **False.** Models degrade over time as the world changes (concept drift).

**Reality:** Models need monitoring, maintenance, and periodic retraining

## "Deep learning is always better than traditional ML"

❌ **False.** Different tools for different jobs.

**Use traditional ML when:**
- You have structured/tabular data
- You need interpretability
- You have limited data
- You need fast training

**Use deep learning when:**
- You have unstructured data (images, text, audio)
- You have lots of data
- You need state-of-the-art performance
- Interpretability is less critical

---

# Quick Reference: Which ML Approach?

**I want to...**

📊 **...predict house prices from features** → Traditional ML (Regression)

📧 **...classify emails as spam or not spam** → Traditional ML (Classification) or Deep Learning

👥 **...group customers by behavior** → Traditional ML (Clustering - Unsupervised)

🖼️ **...recognize objects in images** → Deep Learning (CNNs)

🗣️ **...convert speech to text** → Deep Learning (RNNs or Transformers)

✍️ **...generate human-like text** → LLMs (Transformers)

🤖 **...train a robot to navigate** → Reinforcement Learning

💳 **...detect fraudulent transactions** → Traditional ML or Deep Learning (Anomaly Detection)

🎬 **...recommend movies to users** → Traditional ML (Collaborative Filtering) or Deep Learning

📈 **...forecast sales for next quarter** → Traditional ML (Time Series) or Deep Learning (RNNs)

---

> 🎯 **Key Takeaway**
>
> Machine Learning is the foundation that powers modern AI:
> - **Traditional ML** excels at structured data and interpretable decisions
> - **Deep Learning** excels at unstructured data and complex patterns
> - **LLMs** are a specific application of deep learning for language tasks
>
> Understanding ML fundamentals helps you:
> - Choose the right approach for your problem
> - Understand what's possible (and what's not)
> - Recognize limitations and risks
> - Have informed conversations about AI technology
>
> The key is matching the tool to the task - sometimes simple automation is best, sometimes traditional ML, sometimes deep learning, and sometimes cutting-edge LLMs.
