---
title: "Resume ⇔ Job Matching Engine"
excerpt: "An NLP-driven service that ranks resumes against open job descriptions with multi-class classification, named-entity extraction, and real-time REST APIs."
collection: portfolio
# github_link: https://github.com/samshad/resume-job-matching
---

Developed during my tenure as a **Junior Python Developer** at Smartbytes Ltd. (Bangladesh), this project automates screening by scoring and ranking candidate résumés against job ads, freeing recruiters from manual keyword hunts.

**Key Contributions & Features**
* **End-to-End Data Pipeline**  
  * Scraped & normalised **15 k+** public resumes and job ads with Selenium + BeautifulSoup.
  * Stored structured text in PostgreSQL via SQLAlchemy for repeatable experiments.
* **Rich Feature Engineering**
  * Used **spaCy + NLTK** NER to pull skills, education, locations, and experience.
  * Generated TF-IDF vectors and engineered “skill-overlap” and “seniority-gap” scores.
* **Multi-Class Matching Model**
  * Benchmarked Logistic Regression, Random Forest, and **LinearSVC**; the latter lifted macro-F1 by **≈ 40 %** over baseline.
  * Top-5 match accuracy reached **92 %** on a 20-class held-out set.
* **FastAPI Micro-service**
  * `/match/` endpoint accepts a résumé + JD, returns a ranked list with confidence scores.
  * Swagger docs auto-generated for the frontend team of six developers.
* **Containerised Deployment**
  * Docker and GitHub Actions CI push images to AWS ECR; ECS service auto-scales on CPU load.

**Technologies Used:** Python, spaCy, NLTK, scikit-learn, FastAPI, SQLAlchemy, TF-IDF, LinearSVC, BeautifulSoup, Selenium, PostgreSQL, Docker, AWS ECS.
