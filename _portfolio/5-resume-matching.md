---
title: "Resume ⇔ Job Matching Engine"
excerpt: "Engineered an NLP-powered ranking microservice achieving 92% top-5 accuracy. Benchmarked and deployed a LinearSVC model via AWS ECS with auto-scaling to automate candidate screening."
collection: portfolio
# github_link: https://github.com/samshad/resume-job-matching
---

**The Engineering Challenge:**
Recruitment processes were bottlenecked by manual keyword searching. The objective was to build an automated scoring engine capable of ingesting unstructured resume data and ranking candidates against job descriptions with high semantic accuracy.

**Data Engineering & Feature Extraction:**

* **Automated Ingestion Pipeline:**
    * Built a robust scraper using **Selenium** and **BeautifulSoup** to aggregate a training corpus of **15,000+** resumes and job descriptions.
    * Implemented a normalized storage schema in **PostgreSQL** (via **SQLAlchemy**), creating a reliable ground-truth dataset for reproducible training.
* **NLP Feature Engineering:**
    * Leveraged **spaCy** and **NLTK** for Named Entity Recognition (NER), extracting structured entities (Skills, Education, Location) from unstructured text.
    * Engineered custom interaction features, such as "Skill-Overlap Coefficient" and "Seniority-Gap," combined with **TF-IDF vectors** to capture nuance beyond simple keyword matching.

**Model Selection & Performance:**

* **Rigorous Benchmarking:**
    * Evaluated multiple classifiers (Logistic Regression, Random Forest). **LinearSVC** proved superior for this high-dimensional sparse data, boosting the **macro-F1 score by ~40%** over the baseline.
    * **Result:** The final model achieved a **92% top-5 match accuracy** across 20 distinct job categories, significantly reducing manual screening time.

**MLOps & Production Deployment:**

* **Scalable Microservice Architecture:**
    * Exposed the model via a high-performance **FastAPI** endpoint.
    * Generated automated **Swagger/OpenAPI** documentation to streamline integration for the frontend development team.
* **Containerization & CI/CD:**
    * Dockerized the application and implemented a **GitHub Actions** CI/CD pipeline pushing to **AWS ECR**.
    * Deployed on **AWS ECS** with configured **auto-scaling policies** based on CPU load to handle variable request traffic efficiently.

**Technologies Leveraged:** Python, scikit-learn (LinearSVC), spaCy, NLTK, FastAPI, PostgreSQL, Docker, AWS ECS, GitHub Actions.