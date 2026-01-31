---
title: "AI-Powered Mindful Eating Companion"
excerpt: "I developed a personalized mobile app that uses fine-tuned AI (Llama 3) and a smart FastAPI backend to offer insightful dietary suggestions and help users build healthier, more mindful eating habits."
collection: portfolio
# github_link: https://github.com/samshad/mindful-eating-backend
---

**The Engineering Challenge:**
To move beyond generic diet apps by architecting a context-aware system that adapts to user personality. The goal was to prove that lightweight, fine-tuned LLMs could deliver hyper-personalized health advice effectively on consumer hardware.

**Core Architecture:**
* **Mobile:** React Native (Expo) for cross-platform deployment.
* **Backend:** High-concurrency **FastAPI** microservice handling logic and **PostgreSQL** for relational data integrity.
* **AI Engine:** **Meta Llama 3.2 (3B)** fine-tuned via **LoRA/UnslothAI** to optimize inference on T4 GPUs.

**Key Technical Implementations:**
* **Dual-Model Fine-Tuning Strategy:** I fine-tuned two distinct models. One predicts **Big-5 Personality Traits** from user text, and the second generates context-aware eating tips based on those traits.
* **High-Quality Dataset Construction:** Solved the "garbage-in, garbage-out" problem by constructing a proprietary dataset of **1,500 expert-verified tips**. These were mapped to 10 specific eating behaviors and validated by a registered dietitian and psychologist to ensure safety and accuracy.
* **Hybrid NLP Integration:** Integrated **Symanto NLP API** for psychographic text analysis on 2,400+ essays to benchmark and augment the local model's personality prediction capabilities.
* **Full-Stack Optimization:** Built a seamless pipeline allowing multi-modal logging (text & photo) with real-time AI inference, achieving **~88% user-rated relevance** in pilot testing.

**What This Solved:**
* **Personalization at Scale:** Bridged the gap between static rule-based apps and expensive human coaching.
* **Cost-Effective AI:** Demonstrated that quantized, smaller models (3B) can outperform larger generic models when fine-tuned on high-quality domain data.

**Tech Stack:** Python, FastAPI, React Native, PostgreSQL, Llama 3.2, LoRA, UnslothAI, Docker, AWS EC2.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/mindful-eating-backend)

### System Architecture:

<p align="center">
  <img src="/images/system-design/system-architecture.webp"
       alt="System Architecture" width="70%">
  <br>
  <em>Figure: A look under the hood – the system architecture of the AI-Powered Mindful Eating Companion.</em>
</p>
