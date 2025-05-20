---
title: "Resume ⇔ Job Matching Engine"
excerpt: "As a Junior Python Developer, I built an NLP-powered service that intelligently ranks resumes against job descriptions, using multi-class classification and named-entity extraction to streamline the recruitment process."
collection: portfolio
# github_link: https://github.com/samshad/resume-job-matching
---

During my time as a **Junior Python Developer at Smartbytes Ltd. (Bangladesh)**, I developed this project to tackle a common challenge: making the initial screening of resumes faster and more effective. My goal was to automate the tedious manual keyword searching and provide recruiters with a ranked list of the most suitable candidates.

**Key Contributions & What I Built:**

*   **Comprehensive End-to-End Data Pipeline:**
    *   I engineered a system to scrape and normalize over **15,000+** public resumes and job advertisements using Selenium and BeautifulSoup.
    *   This structured text data was then stored efficiently in PostgreSQL via SQLAlchemy, creating a reliable foundation for repeatable experiments and model training.
*   **Sophisticated Feature Engineering for Deeper Insights:**
    *   Leveraging **spaCy and NLTK**, I implemented Named Entity Recognition (NER) to extract key information like skills, educational background, locations, and years of experience from the text.
    *   I then generated TF-IDF vectors and engineered custom features such as "skill-overlap" and "seniority-gap" scores to capture more nuanced relationships between resumes and job descriptions.
*   **High-Performance Multi-Class Matching Model:**
    *   I rigorously benchmarked several models, including Logistic Regression and Random Forest. Ultimately, a **LinearSVC model proved most effective, boosting the macro-F1 score by approximately 40%** compared to the baseline.
    *   The model achieved an impressive **top-5 match accuracy of 92%** when tested on a held-out set with 20 distinct job categories.
*   **Efficient FastAPI Microservice for Real-Time Matching:**
    *   I developed a REST API using FastAPI, featuring a `/match/` endpoint that accepts a resume and job description, returning a ranked list of candidates with corresponding confidence scores.
    *   To support the frontend team of six developers, I ensured Swagger documentation was automatically generated for easy integration.
*   **Streamlined Containerized Deployment:**
    *   I containerized the application using Docker and set up a CI/CD pipeline with GitHub Actions to automatically push images to AWS ECR. The application was deployed as an AWS ECS service, configured to auto-scale based on CPU load.

**What This Project Highlights About My Abilities:**

*   **Practical NLP Application:** Successfully applying techniques like NER, TF-IDF, and text classification (LinearSVC) to solve a real-world business problem.
*   **Full-Cycle Machine Learning Development:** From data collection and preprocessing to feature engineering, model training, evaluation, and deployment.
*   **Backend & API Development:** Proficiency in building robust and scalable microservices with Python and FastAPI.
*   **Data Engineering & Management:** Experience with web scraping (Selenium, BeautifulSoup), data storage (PostgreSQL, SQLAlchemy), and building data pipelines.
*   **DevOps & Cloud Deployment:** Skills in containerization (Docker) and CI/CD (GitHub Actions) for deployment on AWS (ECR, ECS).
*   **Collaboration & Impact:** Delivering a tool that directly supported a development team and aimed to improve recruiter efficiency.

**Key Technologies I Employed:** Python, spaCy, NLTK, scikit-learn, FastAPI, SQLAlchemy, TF-IDF, LinearSVC, BeautifulSoup, Selenium, PostgreSQL, Docker, AWS ECS, GitHub Actions.