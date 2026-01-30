---
title: "Project Heimdall"
summary: "A Zero-Trust SQL Gateway for LLMs preventing data destruction."
date: "Jan 15 2026"
draft: false
tags:
- Golang
- Security
- AI
- MCP
---

<!-- ![Heimdall Architecture](https://placehold.co/600x400?text=Heimdall+Architecture) -->

## The Problem
LLMs often hallucinate destructive SQL commands (`DROP TABLE`). Connecting them directly to production databases is a massive security risk.

## The Solution
I built a custom **MCP Server** in Golang that acts as a secure middleware "Gatekeeper".

- **Technology:** Golang, PostgreSQL, AST Parsing (`xwb1989/sqlparser`).
- **Key Feature:** It parses the SQL Abstract Syntax Tree to strictly block any non-SELECT statements before they touch the DB.

![Heimdall Architecture](./heimdall-architecture.png)

### Key Metrics
- **0%** Data Loss incidents in testing.
- **<10ms** parsing latency overhead.
- **Protocol:** Implemented full Model Context Protocol (MCP) compliance.

### Links
- [GitHub Repository](https://github.com/AnubhavMadhav/Project-Heimdall)