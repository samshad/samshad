---
title: "AI-Powered Mindful Eating App"
excerpt: "I developed a personalized mobile app that uses finely-tuned AI (Llama 3) and a smart FastAPI backend to offer insightful dietary suggestions and help users build healthier, more mindful eating habits."
collection: portfolio
# github_link: https://github.com/samshad/mindful-eating-backend
---

This project was a journey in creating a truly personalized mindful eating experience from the ground up. My goal was to blend cutting-edge AI with user-friendly design to make a real difference in how people approach their meals.

*   **The Tech Backbone:** I architected and built the entire system using React Native (Expo) for a smooth mobile experience, Python (FastAPI) for a speedy and reliable backend, PostgreSQL for robust data management, and integrated Ollama/UnslothAI for powerful on-device/local LLM capabilities.
*   **Smarter AI with Fine-Tuned LLMs:**
    *   I took two Meta Llama 3.2 (3B) models and customized them using LoRA adapters on Google Colab (T4 GPUs) – this was key to the app's intelligence.
    *   One model cleverly predicts a user's Big Five personality traits based on their questionnaire responses.
    *   The other model crafts context-aware mindful eating tips, which users found **highly relevant (around 88% in pilot tests!)**.
*   **Crafting a Unique Knowledge Base:** I meticulously curated a dataset of 1,500 mindful eating tips inspired by experts. These were carefully mapped across 10 eating behaviors and 5 personality types, then further refined with ChatGPT-4o, and validated by a registered dietitian and a psychologist to ensure quality and accuracy.
*   **Powerful & Efficient Backend:** I engineered a robust FastAPI backend with REST APIs that handle everything smoothly:
    *   Secure user sign-up, login, and profile management (including demographics, dietary preferences, and personality insights).
    *   Easy goal setting and food logging (users can even snap a photo or just type).
    *   Instant, intelligent responses from the fine-tuned AI.
*   **Full-Stack Design & Development:** I designed and developed the mobile app, ensuring an intuitive flow for users to input their information, receive personalized AI feedback, and even chat with the AI for support.
*   **Understanding Users Better:** To deepen personalization, I also trained a Big Five personality classifier using the Symanto NLP API on a dataset of 2,467 essays. This helps the app tailor advice even more effectively.

**What This Project Showcases:**

*   **End-to-End Development:** From concept to a fully functional application.
*   **Advanced AI/ML Skills:** Fine-tuning large language models (Llama 3, LoRA), dataset curation, and practical LLM integration.
*   **Full-Stack Proficiency:** Expertise across the front-end (React Native), backend (FastAPI, Python), database (PostgreSQL), and MLOps (Ollama, UnslothAI).
*   **User-Centric Design:** Focusing on creating a helpful, personalized, and engaging experience.
*   **Problem-Solving & Innovation:** Combining diverse technologies to build a novel solution for promoting healthier habits.

**Technologies I Mastered & Used:** Python, FastAPI, PostgreSQL, React Native, Expo, Ollama, UnslothAI, LoRA, LLM Fine-Tuning, Google Colab, Symanto NLP API, Docker, AWS EC2.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/mindful-eating-backend)

### System Architecture:

<p align="center">
  <img src="https://raw.githubusercontent.com/samshad/samshad/refs/heads/master/images/samshad/system-architecture.webp"
       alt="System Architecture" width="70%">
  <br>
  <em>Figure: A look under the hood – the system architecture of the AI-Powered Mindful Eating Companion.</em>
</p>
