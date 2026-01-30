---
title: "Project XLR8"
summary: "A high-throughput RAG ingestion engine utilizing Golang worker pools and custom rate limiting."
date: "Jan 20 2026"
draft: false
tags:
- Golang
- Concurrency
- Vector DB
- System Design
---

![XLR8 Pipeline Architecture](https://placehold.co/600x400?text=XLR8+Architecture)
## The Problem
Building a RAG (Retrieval-Augmented Generation) pipeline is easy; scaling it to ingest **100,000+ documents** is hard. Naive Python scripts often crash due to Out-Of-Memory (OOM) errors or get banned by upstream APIs for hitting rate limits (429 Too Many Requests).

## The Solution
I engineered **XLR8** (Accelerate), a highly concurrent ingestion engine in Golang designed to saturate network bandwidth without breaking API quotas.

- **Architecture:** Implemented a **Fan-Out/Fan-In Worker Pool** pattern to process documents in parallel while maintaining constant memory usage.
- **Traffic Control:** Built a custom **Token Bucket Rate Limiter** to strictly adhere to API quotas (e.g., 500 RPM) regardless of concurrency levels.
- **Observability:** Integrated a TUI (Terminal UI) using **Bubble Tea** to visualize throughput (docs/sec) and error rates in real-time.

### Key Metrics
- **Throughput:** Capable of processing 10,000+ documents without memory spikes.
- **Reliability:** Zero "429 Too Many Requests" errors due to strict rate limiting.
- **Tech Stack:** Golang, Weaviate (Vector DB), Bubble Tea, OpenAI API.

### Links
- [GitHub Repository](https://github.com/yourusername/xlr8)