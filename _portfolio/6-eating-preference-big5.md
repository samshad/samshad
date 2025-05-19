---
title: "Eating-Preference ↔ Personality Insight Engine"
excerpt: "Mining Twitter & Foursquare data, then pairing Big-Five personality scores with dining habits to reveal how traits shape restaurant choices."
collection: portfolio
# github_link: https://github.com/samshad/eating-preference-personality
---

Conducted while I was a **Research Assistant** with the Cognitive and Behavioral Data Science Research Group at United International University (Bangladesh), this research prototype links social-media footprints to food decisions, showing how Openness or Neuroticism may sway preference for restaurants.

**Key Contributions & Findings**
* **Large-Scale Social-Media Harvest**  
  * Scraped **55 k** Foursquare restaurant check-ins tied to public Twitter handles (Selenium, BeautifulSoup, Rotating Proxies).  
  * Collected ~2 M tweets and cleaned noise via spaCy & NLTK pipelines (emoji strip, URL removal, language filter).
* **Automatic Personality Profiling**  
  * Fed tweet corpora into **IBM Watson Personality Insights** to extract Big-Five scores for 7 800 users.  
  * Implemented caching & rate-limit back-off, cutting API cost by ~45 %.
* **Behavioral Taxonomy & Labeling**  
  * Achieved Cohen’s κ = 0.83 on a 1 000-sample double-annotated subset.
* **Statistical & ML Correlation**  
  * Ran Pearson and Spearman tests, exposing strong **Extraversion → Expensive restaurants** link (ρ = .41, p < 0.01).

**Technologies Used:** Python, spaCy, NLTK, IBM Watson Personality API, Selenium, BeautifulSoup, Pandas, scikit-learn, Jupyter, Docker, Rotating Proxies.