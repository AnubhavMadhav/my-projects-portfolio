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
Using large models like GPT-4 for every user query is financially inefficient and slow. A simple "Hello" or "What is 2+2?" does not require a $20/month model.

## The Solution
I built **Project Omnitrix**, a smart middleware that dynamically routes traffic to the "Right Model for the Job."

- **Reflex Layer (Zero Latency):** Uses the **Aho-Corasick** algorithm to instantly resolve static intents (greetings, blocked words) with **0ms latency**, bypassing LLMs entirely.
- **The Brain (Classifier):** Uses a lightweight model (**Phi-3 Mini**) to classify complex prompts into intent buckets (Coding, Creative, Math).
- **Business Engine:** Integrated **Rulio** (Rule Engine) to route Premium users to high-tier models (Llama-3-70B) and Free users to cost-effective ones (DeepSeek-V2-Lite).

### Key Features
- **Cost Optimization:** Drastically reduces API bills by offloading simple queries to smaller models.
- **Resiliency:** Implemented the **Circuit Breaker** pattern to automatically fallback to robust models if the primary provider fails.
- **Tech Stack:** Golang, Gin, Rulio, Ollama, Groq Cloud.

### Links
- [GitHub Repository](https://github.com/yourusername/omnitrix)