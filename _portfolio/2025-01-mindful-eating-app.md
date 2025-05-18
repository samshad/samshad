---
title: "AI-Powered Mindful Eating App"
excerpt: "A personalized mobile app leveraging fine-tuned LLMs (Llama 3) and a FastAPI backend to deliver AI-driven dietary suggestions and promote mindful eating habits."
collection: portfolio
github_link: https://github.com/samshad/mindful-eating-backend
---

This project involved the end-to-end development of a personalized mindful eating mobile application.

**Key Contributions & Features:**
*   **Application Stack:** React Native (Expo) for the mobile front-end, FastAPI (Python) for the backend, PostgreSQL for data storage, and Ollama/UnslothAI for LLM integration.
*   **LLM Fine-Tuning:**
    *   Fine-tuned two Meta Llama 3.2 (3B) models using LoRA adapters on Google Colab (T4 GPUs).
    *   One LLM predicts Big Five personality traits from user questionnaire data.
    *   A second LLM generates context-aware eating tips, achieving ~88% user-rated relevance in pilot tests.
*   **Dataset Curation:** Authored and curated a novel dataset of 1500 domain-expert-inspired mindful eating tips, mapped across 10 eating behaviors and 5 personality traits, refined with ChatGPT-4, and validated by a dietitian and psychologist.
*   **Backend Development:** Developed a robust FastAPI backend with RESTful APIs for user authentication, profile management (demographics, dietary preferences, personality traits), goal setting, food logging (image & text), and real-time LLM interaction.
*   **Full-Stack Implementation:** Implemented a user-friendly React Native mobile interface enabling seamless data input, personalized feedback delivery, and direct chat support via the fine-tuned LLM.
*   **Personality Classifier:** Built a Big Five personality classifier trained on 2,467 essays using the Symanto NLP API.

**Technologies Used:** Python, FastAPI, PostgreSQL, React Native, Expo, Ollama, UnslothAI, LoRA, Google Colab, Symanto NLP API, Docker, EC2.
