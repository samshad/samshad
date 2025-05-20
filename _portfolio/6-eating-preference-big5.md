While working as a **Research Assistant** with the Cognitive and Behavioral Data Science Research Group at United International University (Bangladesh), I spearheaded this research prototype. Our aim was to explore the intriguing connections between an individual's digital footprint on social media and their real-world food decisions, specifically how personality traits like Openness or Neuroticism might influence their restaurant preferences.

**My Key Contributions & Discoveries:**

*   **Harvesting & Refining Large-Scale Social Data:**
    *   I engineered a system to collect **55,000 Foursquare restaurant check-ins** linked to public Twitter profiles, employing Selenium, BeautifulSoup, and rotating proxies to navigate complex data sources.
    *   Alongside this, I gathered approximately **2 million tweets**. I then developed robust NLP pipelines using spaCy and NLTK to meticulously clean this vast text data (e.g., stripping emojis, removing URLs, filtering by language) to prepare it for analysis.
*   **Automated Personality Profiling at Scale:**
    *   I integrated the **IBM Watson Personality Insights API** to process the tweet corpora, successfully extracting Big-Five personality scores for **7,800 users**.
    *   To manage resources effectively, I implemented smart caching and rate-limit back-off strategies, which impressively **cut API usage costs by about 45%**.
*   **Developing a Robust Behavioral Classification Framework:**
    *   To systematically link personality to dining, I was involved in creating and validating a behavioral taxonomy for classifying dining preferences or restaurant characteristics apparent in the data.
*   **Uncovering Statistically Significant Correlations:**
    *   Through rigorous statistical analysis (including Pearson and Spearman tests), we unearthed compelling links. For instance, we found a notable **positive correlation between Extraversion and a preference for more expensive restaurants** (ρ = .41, p < 0.01).

**What This Research Showcases:**

*   **In-Depth Research & Analytical Skills:** From hypothesis generation to data collection, complex analysis, and interpretation of findings within an academic research setting.
*   **Advanced Data Collection & Wrangling:** Proficiency in web scraping (Selenium, BeautifulSoup, proxies) and cleaning large, noisy social media datasets.
*   **Practical Application of NLP & AI:** Utilizing tools like spaCy, NLTK, and cloud AI services (IBM Watson) for large-scale text processing and personality profiling.
*   **Statistical Analysis & Insight Generation:** Ability to apply statistical methods to uncover meaningful patterns and correlations in complex datasets.
*   **Problem-Solving & Resourcefulness:** Developing cost-saving measures (API caching) and ensuring data quality.

**Key Technologies & Tools I Utilized:** Python, spaCy, NLTK, IBM Watson Personality API, Selenium, BeautifulSoup, Pandas, scikit-learn, Jupyter Notebooks, Docker, Rotating Proxies.