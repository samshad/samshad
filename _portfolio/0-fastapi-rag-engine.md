---
title: "Production-Grade Multi-Tenant FastAPI RAG Engine"
excerpt: "I engineered a fully asynchronous, multi-tenant Retrieval-Augmented Generation (RAG) REST API from scratch — featuring JWT authentication, OTP-based email verification, and 100% test coverage (468 tests). Built with FastAPI, Neon Serverless Postgres (pgvector), and Ollama for real-time, context-aware AI streaming."
collection: portfolio
# github_link: https://github.com/samshad/fastapi-ollama-rag
---

**The Engineering Challenge:**
To build a production-grade, multi-tenant RAG system with full user isolation, secure authentication, and a highly concurrent pipeline — all without relying on heavy abstraction layers like LangChain. The goal was to prove that first-principles engineering with raw async Python, strict data contracts, and real database testing yields a faster, more maintainable, and fully verifiable AI backend.

**Core Architecture:**
* **API Layer:** High-concurrency **FastAPI** with async Python, OAuth2 Password Bearer JWT authentication, and OTP-based email verification via **aiosmtplib**.
* **Vector Database:** **Neon Serverless PostgreSQL 16** with the **pgvector** extension and **asyncpg** raw SQL for optimized binary bulk data transfers — no ORM overhead.
* **AI/LLM Engine:** **Ollama** orchestrating 1024-dimensional embeddings (**mxbai-embed-large**) and real-time text generation (**deepseek-r1:8b**) via **httpx**.
* **Multi-Tenancy:** Every document, vector, and query is scoped to an authenticated `user_id` — strict database-level isolation.

**Key Technical Implementations:**
* **Secure Authentication & Multi-Tenancy:** Implemented a complete auth system with JWT access tokens (PyJWT), bcrypt password hashing, and OTP-based email verification for both registration and password reset flows — all fully async.
* **Zero-Blocking Document Ingestion:** Offloaded CPU-bound **PyMuPDF** C-extension execution to background thread pools (**asyncio.to_thread**), safeguarding the event loop and ensuring the server remains responsive during massive file uploads.
* **Pure Python Semantic Chunking:** Engineered a custom O(N) sliding-window text chunker that smartly snaps to natural punctuation boundaries, preserving semantic meaning without the overhead of third-party ML orchestration libraries.
* **Cryptographic Deduplication:** Implemented SHA-256 fingerprinting on incoming document byte streams to instantly reject duplicate files, saving massive GPU embedding compute and preventing vector database bloat.
* **Lightning-Fast Vector Search & Streaming:** Leveraged HNSW indexing and cosine distance (`<=>`) in Postgres for millisecond retrieval. Retrieved chunks are compiled into a grounded system prompt, and the LLM response is streamed token-by-token directly to the client via FastAPI's **StreamingResponse**.
* **Enterprise Observability:** **structlog** JSON logging with rotating file handler, asynchronously piped into **Better Stack** for real-time cloud log aggregation and querying.
* **Exhaustive Test Suite:** **468 tests** across unit, integration, and API route layers achieving **100% line coverage**. Integration tests run against real ephemeral **pgvector** containers in CI — no mocking SQL.
* **CI/CD Pipeline:** GitHub Actions enforcing Ruff lint + format gates before running the full test suite against a real database.

**What This Solved:**
* **Framework Bloat:** Eliminated the overhead, latency, and unpredictability of high-level wrappers (LangChain/LlamaIndex) to gain total, deterministic control over the execution flow.
* **AI Infrastructure Latency:** Drastically reduced perceived user latency from ~15 seconds down to sub-second levels via asynchronous HTTP streaming and highly optimized database connection pooling.
* **Security & Isolation:** Full ownership of auth flows (no vendor lock-in), with per-user data isolation ensuring no cross-tenant data leakage.
* **Confidence in Production:** 100% test coverage with real database integration tests eliminates entire classes of bugs that mocked tests would miss.

**Tech Stack:** Python 3.12+, FastAPI, Uvicorn, PostgreSQL 16 (Neon), pgvector, asyncpg, Ollama, httpx, PyJWT, bcrypt, aiosmtplib, PyMuPDF, Pydantic v2, Docker, GitHub Actions, structlog, Better Stack.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/fastapi-ollama-rag)
[![CI](https://github.com/samshad/fastapi-ollama-rag/actions/workflows/ci.yml/badge.svg)](https://github.com/samshad/fastapi-ollama-rag/actions/workflows/ci.yml)

### System Architecture:

<p align="center">
  <img src="https://raw.githubusercontent.com/samshad/fastapi-ollama-rag/main/docs/architecture.svg"
       alt="System Architecture Diagram" width="100%">
  <br>
  <em>Figure: System architecture of the Production-Grade Multi-Tenant FastAPI RAG Engine.</em>
</p>
