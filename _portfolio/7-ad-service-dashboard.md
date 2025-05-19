---
title: "Unified Ad-Service Revenue Dashboard"
excerpt: "One page, all the numbers—scraping AdMob, MoPub, AppLovin, AdColony and many more services into a single MySQL warehouse, then visualising real-time KPIs in Tableau & Excel."
collection: portfolio
# github_link: https://github.com/samshad
---

While at **Free Pixel Games Ltd.** I built a tool that finally answered, *“How much did we actually earn today, across every ad network?”*

**Key Contributions & Results**
* **Automated Multi-Network Ingestion**  
  * Headless Python scrapers (Selenium + BeautifulSoup) and REST calls pull daily earnings, eCPM, fill-rate, and errors from **AdMob, MoPub, AppLovin, AdColony and others**.  
  * Standardised disparate CSV formats into a common schema.
* **Central Data Warehouse**  
  * Normalised tables in **MySQL** enable fast joins for cross-network comparisons and trend queries.  
  * Incremental ETL jobs append ~50 k new rows per month with zero downtime.
* **Single-Page Analytics Dashboard**  
  * Tableau workbook (+ Excel Power Query fallback) shows revenue, impressions, fill rate, and network health side-by-side.  
  * Conditional formatting flags under-performing placements in real time.
* **Alerting & Trend Insight**  
  * Simple Python rule engine emails anomalies (e.g., ≥ 10 % eCPM drop).  
  * Trend lines reveal seasonality and inform ad-unit optimisation.
* **Operational Impact**  
  * Cut manual spreadsheet work **by > 80 %** (two hours → < 15 minutes per day).  
  * Enabled product team to shift spend and raise blended fill-rate **≈ 8 %**.

**Technologies Used:** Python, Selenium, BeautifulSoup, REST APIs, Pandas, MySQL, Tableau, Microsoft Excel, Cron.
