---
title: "Project Omnitrix"
summary: "An intelligent API Gateway that routes user prompts to the most cost-effective LLM."
date: "Jan 28 2026"
draft: false
tags:
- Golang
- System Design
- FinOps
- LLM
---

![Omnitrix Routing Logic](https://placehold.co/600x400?text=Omnitrix+Routing+Logic)
## The Problem
Running every user query through high-end models (like GPT-4) is prohibitively expensive and slow. A simple "Hello" or "What is 2+2?" does not require a $20/month model.

## The Solution
I built **Project Omnitrix**, a Intent-Aware AI Gateway (smart middleware) that dynamically routes traffic to the "Right Model for the Job."

Technology: Golang, Gin, Aho-Corasick Algorithm, Ollama, Groq.


- **Reflex Layer (Zero Latency):** Uses the **Aho-Corasick** algorithm to instantly resolve static intents (greetings, blocked words) with **0ms latency**, bypassing LLMs entirely.
- **The Brain (Classifier):** Uses a lightweight model (**Phi-3 Mini**) to classify complex prompts into intent buckets (Coding, Creative, Math etc.).
- **Business Engine:** The Resolver Pattern automatically switches between providers based on the logic matrix. It decouples the intent from the execution.
- **Tiered Quality of Service:**
    - **Free Tier:** Routes to efficient local models (e.g., Gemma-2B, Phi-3).
    - **Premium Tier:** Routes to state-of-the-art cloud models (e.g., Llama-3-70B on Groq) for superior performance.

### Key Features
- **Cost Optimization:** Drastically reduces API bills by offloading simple queries to smaller models.
- **Resiliency:** Implemented the **Circuit Breaker** pattern to automatically fallback to robust models if the primary provider fails.
- **Tech Stack:** Golang, Gin, Aho-Corasick Algorithm, Ollama, Groq Cloud

### Links
- [GitHub Repository](https://github.com/AnubhavMadhav/Osmnitrix)