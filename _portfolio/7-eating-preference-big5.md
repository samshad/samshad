---
title: "Eating Preference Analysis Based on Human Personality Traits"
excerpt: "Engineered a distributed data acquisition pipeline to harvest 2M+ tweets and 55k check-ins, leveraging IBM Watson for psychographic profiling to correlate digital footprints with physical dining behavior."
collection: portfolio
# github_link: https://github.com/samshad/eating-preference-analysis
---

**The Engineering & Research Challenge:**
To quantify the relationship between latent personality traits and physical world behavior (dining choices). The technical barrier was acquiring and cleaning massive datasets from rate-limited social media platforms to build a statistically significant sample size for psychographic modeling.

**Data Engineering & Acquisition Infrastructure:**

* **Distributed Scraping Pipeline:**
    * Architected a robust scraper using **Selenium** and **BeautifulSoup** to harvest **55,000 Foursquare check-ins** and **~2 million tweets**.
    * **Rate-Limit Mitigation:** Implemented a **rotating proxy network** and request throttling to bypass strict API rate limits, ensuring continuous data ingestion without IP bans.
* **Cost-Optimized API Integration:**
    * Integrated **IBM Watson Personality Insights API** to extract Big-Five personality traits for **7,800** unique users.
    * **Optimization:** Engineered a caching layer and smart back-off strategy that reduced redundant API calls, cutting project overhead costs by **~45%**.

**NLP & Statistical Inference:**

* **Noise Reduction Pipeline:**
    * Developed automated cleaning scripts using **spaCy** and **NLTK** to strip noise (emojis, URLs) from the raw text corpus.
    * **Result:** Reduced dataset noise by **~45%**, significantly improving the signal-to-noise ratio for downstream analysis.
* **Correlation Analysis:**
    * Conducted rigorous statistical testing (Pearson/Spearman) to validate the behavioral taxonomy.
    * **Key Finding:** Established a statistically significant correlation (**ρ = .41, p < 0.01**) between high Extraversion scores and a preference for high-cost dining establishments.

**Technologies Leveraged:** Python, IBM Watson API, Selenium, BeautifulSoup, scikit-learn (Pearson/Spearman), spaCy, NLTK, Pandas, Docker, Rotating Proxies.