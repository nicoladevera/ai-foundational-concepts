# Machine Learning 101

**Learning goal:** Understand the foundational technology behind modern AI, from traditional ML to deep learning to LLMs.

---

# What is Machine Learning?

## Simple Definition

**Machine Learning (ML)** is a way of teaching computers to make decisions or predictions by showing them examples, rather than explicitly programming every rule.

## The Key Difference

**Traditional programming:**
- Humans write explicit rules
- Computers follow those rules exactly
- The same input usually produces the same output

**Machine learning:**
- Humans provide data and examples
- The system finds patterns in those examples
- The model learns rules statistically rather than by hand-written logic

Example:
- Traditional programming: "If temperature < 68 F, turn on heater"
- Machine learning: Show a system many labeled photos of cats and dogs so it learns the visual patterns itself

Key idea:
- Instead of telling computers exactly how to solve a task, we let them learn from examples.

## Real-World Analogy

Traditional programming is like following a recipe with exact steps.

Machine learning is like learning to cook by tasting many dishes, noticing patterns, and gradually building intuition about what works.

---

# The Learning Process

## Step 1: Collect Training Data

Gather examples of the task you want the model to learn.

Example:
- To build a spam detector, collect emails labeled as spam or not spam.

## Step 2: Represent the Input

The system needs measurable input features or representations.

Example for spam detection:
- Number of links
- Suspicious phrases
- Sender domain
- Length
- Message structure

In older ML systems, humans usually designed these features manually. In deep learning systems, the model often learns useful representations on its own.

## Step 3: Train the Model

The algorithm adjusts internal parameters to reduce prediction errors.

What is happening:
- The model makes guesses
- It compares those guesses to the correct answers
- It adjusts its internal weights to do better next time

## Step 4: Evaluate Performance

Test the model on new data it has not seen before.

This is how you check whether it learned a useful pattern instead of just memorizing the training set.

## Step 5: Deploy and Monitor

Real-world data changes over time. Models can drift, degrade, or fail in new situations, so monitoring matters.

Key insight:
- A model does not understand a task the way a human does. It learns patterns that correlate with useful outputs.

---

# Types of Machine Learning

## 1. Supervised Learning

### What It Is

Learning from labeled examples where the input and the correct answer are both provided.

### Common Tasks

**Classification**
- Spam vs not spam
- Fraud vs legitimate transaction
- Customer churn vs retention

**Regression**
- House price prediction
- Sales forecasting
- Demand forecasting

### Real-World Examples

- Credit risk prediction
- Medical diagnosis support
- Ad click prediction
- Speech recognition systems trained from audio and transcripts

### Common Tools

- Scikit-learn
- XGBoost
- Cloud platforms such as SageMaker or Vertex AI

---

## 2. Unsupervised Learning

### What It Is

Learning from unlabeled data to discover structure or patterns.

### Common Tasks

**Clustering**
- Customer segmentation
- Topic grouping
- Outlier detection

**Dimensionality reduction**
- Compressing or visualizing complex data
- Reducing redundant information

### Real-World Examples

- Fraud anomaly detection
- Product grouping
- Topic discovery in document collections
- Genomics pattern discovery

### Common Tools

- Scikit-learn
- TensorFlow or PyTorch for neural approaches
- Algorithms such as PCA, DBSCAN, and K-means

---

## 3. Reinforcement Learning

### What It Is

Learning by taking actions, receiving feedback, and improving over time.

### How It Works

- An agent acts in an environment
- It receives rewards or penalties
- It learns which actions improve long-term outcomes

### Real-World Examples

- Game-playing systems
- Robotics
- Traffic or energy optimization
- Some decision-making components in complex AI systems

### Common Tools

- Gym-style environments
- RLlib
- Unity ML-Agents

---

# Traditional ML vs. Deep Learning vs. LLMs

## Traditional Machine Learning

### Characteristics

- Usually works best on structured data
- Often requires manual feature engineering
- Often easier to interpret
- Usually cheaper to train and run

### Common Algorithms

- Decision trees
- Random forests
- Gradient boosting
- Linear and logistic regression
- Support vector machines

### Best For

- Tabular business data
- Smaller datasets
- Problems where interpretability matters

---

## Deep Learning

### What It Is

A subset of machine learning based on neural networks with many layers.

### Key Innovation

Deep learning systems often learn representations automatically instead of depending on hand-designed features.

Example:
- Older image pipelines might manually detect edges and shapes
- Deep learning systems learn useful visual patterns directly from training data

### Characteristics

- Strong on images, audio, text, and other unstructured data
- Usually needs much more data and compute
- Often harder to interpret
- Enables many modern perception systems

### Common Tools

- PyTorch
- TensorFlow
- Keras

---

## Large Language Models (LLMs)

### What They Are

LLMs are a specific application of deep learning, usually based on the transformer architecture, trained on massive amounts of text and often extended to images, audio, or tools.

### Key Characteristics

- Trained on very large datasets
- Use many learned parameters
- Can perform many tasks from the same base model
- Benefit from instruction tuning, tool use, and post-training

### How They Fit in the ML Landscape

**Traditional ML**
- Predicts one kind of outcome from structured inputs

**Deep learning**
- Learns powerful representations for tasks like speech or vision

**LLMs**
- General-purpose language interfaces that can write, summarize, answer questions, generate code, and coordinate tool use

### Examples

- Closed frontier model families from OpenAI, Anthropic, and Google
- Open-weight families such as Llama and Mistral
- Specialized code, vision, audio, and agent-focused models

Learn more:
- See [02 - LLMs 101](<./02 - LLMs 101.md>)

---

# Comparison Table

| **Aspect** | **Traditional ML** | **Deep Learning** | **LLMs** |
|---|---|---|---|
| **Feature Engineering** | Often manual | Often learned automatically | Learned automatically |
| **Best Data Type** | Structured tables | Unstructured data | Text first, increasingly multimodal |
| **Typical Scope** | One task | Usually one domain or capability | Many tasks through one interface |
| **Compute Needs** | Low to medium | High | Very high |
| **Interpretability** | Higher | Lower | Very low |
| **Examples** | Fraud scoring, forecasting | Vision, speech, OCR | Chat, writing, coding, agents |

---

# Key ML Concepts Explained

## Training Data

The examples used to teach the model.

Quality matters as much as quantity:
- Biased data creates biased outputs
- Incomplete data creates blind spots
- Poor labels create noisy models

## Features

Measurable characteristics used to make predictions.

Example for house prices:
- Square footage
- Bedrooms
- Age
- Location

## Model

The mathematical representation of what the system has learned from data.

## Parameters

The internal weights a model learns during training.

Broadly:
- Traditional ML models may use hundreds to millions of parameters
- Deep learning models may use millions to billions
- Frontier LLMs often use extremely large parameter counts, though exact numbers are frequently undisclosed

More parameters usually mean more capacity, but not automatically better results.

## Training vs. Inference

**Training**
- Learning from data
- Expensive and infrequent

**Inference**
- Using the trained model
- What happens when someone actually uses the system

## Overfitting vs. Underfitting

**Overfitting**
- Model memorizes training data and fails on new examples

**Underfitting**
- Model is too simple to capture useful patterns

---

# Why This Matters

Understanding ML helps you place modern AI systems in context.

- Not all AI is an LLM
- Not all problems need deep learning
- Simpler systems are often cheaper, easier to test, and more reliable

Good AI decisions usually start with the question:
- What kind of problem am I solving, and what kind of model actually fits it?

---

> **Key Takeaway**
>
> Machine learning is the broad discipline of learning from examples.
>
> - Traditional ML is often best for structured prediction problems
> - Deep learning is strong for perception and unstructured data
> - LLMs are one powerful branch of deep learning, not the whole field
>
> If you understand the difference between these layers, you can think more clearly about what modern AI can do, what it cannot do, and which tool belongs where.
