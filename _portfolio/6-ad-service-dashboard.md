---
title: "Unified Ad-Service Revenue Dashboard"
excerpt: "Architected an automated ETL pipeline consolidating revenue data from 5+ ad networks into a central MySQL warehouse, reducing manual reporting time by 80% and driving an 8% increase in fill rates."
collection: portfolio
# github_link: https://github.com/samshad
---

**The Engineering Challenge:**
Daily revenue reporting was fragmented across disparate ad networks (AdMob, MoPub, AppLovin), requiring hours of manual CSV merging. The business needed a unified, normalized view of earnings to identify eCPM fluctuations and optimize ad spend in real-time.

**ETL Architecture & Data Warehousing:**

* **Automated Ingestion Pipeline:**
    * Engineered a headless **Python** scraper suite (Selenium/BeautifulSoup) and REST API integrations to ingest daily performance metrics (eCPM, Fill-Rate, Impressions).
    * **Schema Normalization:** Solved the "N+1 format" problem by designing a unified **MySQL** schema that standardized conflicting data structures from 5+ providers, enabling apples-to-apples performance comparison.
* **Scalable Data Operations:**
    * Built robust, incremental ETL jobs handling **~50,000 new records/month**, ensuring zero-downtime updates and historical data integrity.
* **Proactive Anomaly Detection:**
    * Developed a custom **Python Rule Engine** to monitor data stream health. It automatically triggers email alerts when critical metrics (like eCPM) drop by **≥10%**, enabling immediate remediation of revenue leaks.

**Business Intelligence & Impact:**

* **Operational Automation:**
    * Replaced manual spreadsheet workflows with a self-service **Tableau** dashboard.
    * **Impact:** Reduced daily reporting overhead by **>80%** (cutting 2 hours of work to <15 minutes).
* **Revenue Optimization:**
    * The unified visibility allowed the product team to identify and remove underperforming ad units.
    * **Result:** Directly contributed to an **~8% increase** in blended fill-rates across the portfolio.

**Technologies Leveraged:** Python, Selenium, MySQL, REST APIs, Tableau, Pandas, Cron, ETL Pipelines.