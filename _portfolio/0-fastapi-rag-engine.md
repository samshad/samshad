---
title: "Production-Grade FastAPI RAG Engine"
excerpt: "I engineered a fully asynchronous Retrieval-Augmented Generation (RAG) REST API from scratch. Bypassing bloated frameworks, it leverages FastAPI, Neon Serverless Postgres (pgvector), and Ollama models to deliver real-time, context-aware AI streaming with enterprise observability."
collection: portfolio
# github_link: https://github.com/samshad/fastapi-ollama-rag
---

**The Engineering Challenge:**
To build a highly concurrent RAG pipeline that doesn't block the main event loop during massive PDF parsing, while completely avoiding heavy, opaque abstraction layers like LangChain. The goal was to prove that relying on raw performance, strict data contracts, and first-principles engineering yields a faster, more maintainable AI backend.

**Core Architecture:**
* **API Layer:** High-concurrency **FastAPI** leveraging async Python for zero-blocking HTTP I/O.
* **Vector Database:** **Neon Serverless PostgreSQL** with the `pgvector` extension and `asyncpg` for optimized binary bulk data transfers.
* **AI/LLM Engine:** **Ollama** orchestrating 1024-dimensional embeddings (`mxbai-embed-large`) and real-time text generation (`deepseek-r1:8b` / `Llama 3.2`).



**Key Technical Implementations:**
* **Zero-Blocking Document Ingestion:** Offloaded CPU-bound `PyMuPDF` C-extension execution to background thread pools (`asyncio.to_thread`), safeguarding the event loop and ensuring the server remains responsive during massive file uploads.
* **Pure Python Semantic Chunking:** Engineered a custom $O(N)$ sliding-window text chunker that smartly snaps to natural punctuation boundaries, preserving semantic meaning without the overhead of third-party ML orchestration libraries.
* **Cryptographic Deduplication:** Implemented SHA-256 fingerprinting on incoming document byte streams to instantly reject duplicate files, saving massive GPU embedding compute and preventing vector database bloat.
* **Lightning-Fast Vector Search & Streaming:** Leveraged HNSW indexing and cosine distance (`<=>`) in Postgres for millisecond retrieval. The LLM's grounded response is streamed token-by-token directly to the client via FastAPI's `StreamingResponse`.
* **Enterprise Observability:** Replaced standard Python text logging with `structlog` for strictly typed JSON telemetry, asynchronously piped into **Better Stack** for real-time cloud log aggregation and querying.

**What This Solved:**
* **Framework Bloat:** Eliminated the overhead, latency, and unpredictability of high-level wrappers (LangChain/LlamaIndex) to gain total, deterministic control over the execution flow.
* **AI Infrastructure Latency:** Drastically reduced perceived user latency from ~15 seconds down to sub-second levels via asynchronous HTTP streaming and highly optimized database connection pooling.

**Tech Stack:** Python 3.12, FastAPI, PostgreSQL (Neon), pgvector, asyncpg, Ollama, PyMuPDF, Docker, structlog, Better Stack.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/fastapi-ollama-rag)
