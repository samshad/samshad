---
title: "AI-Powered Mindful Eating App"
excerpt: "A personalized mobile app leveraging fine-tuned LLMs (Llama 3) and a FastAPI backend to deliver AI-driven dietary suggestions and promote mindful eating habits."
collection: portfolio
# github_link: https://github.com/samshad/mindful-eating-backend
---

This project involved the end-to-end development of a personalized mindful eating mobile application.

**Key Contributions & Features:**
* **Application Stack:** React Native (Expo) for the mobile front-end, FastAPI (Python) for the backend, PostgreSQL for data storage, and Ollama/UnslothAI for LLM integration.
* **LLM Fine-Tuning:**
  * Fine-tuned two Meta Llama 3.2 (3B) models with LoRA adapters on Google Colab (T4 GPUs).
  * One model predicts Big Five personality traits from user questionnaires.
  * The second model generates context-aware mindful eating tips (~88% user-rated relevance in pilot tests).
* **Dataset Curation:** Created a dataset of 1,500 expert-inspired mindful eating tips, mapped across 10 eating behaviors and 5 personality traits, refined with ChatGPT-4, and validated by a registered dietitian and psychologist.
* **Backend Development:** Built a robust FastAPI backend with REST APIs covering:
  * User authentication & profile management (demographics, preferences, traits)
  * Goal setting & food logging (image + text input)
  * Real-time interaction with the fine-tuned LLM
* **Full-Stack Implementation:** Developed a mobile interface with seamless input flows, personalized feedback delivery, and integrated AI chat support.
* **Personality Classifier:** Trained a Big Five classifier on 2,467 essays using the Symanto NLP API.

**Technologies Used:** Python, FastAPI, PostgreSQL, React Native, Expo, Ollama, UnslothAI, LoRA, Google Colab, Symanto NLP API, Docker, EC2.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/mindful-eating-backend)

### System Architecture:
<figure style="text-align: center;">
  <img src="https://raw.githubusercontent.com/samshad/mindful-eating-backend/refs/heads/master/assets/system-architecture.png" alt="System Architecture" width="100%">
  <figcaption style="font-style: italic; margin-top: 6px;">Figure: System Architecture of the AI-Powered Mindful Eating App</figcaption>
</figure>
