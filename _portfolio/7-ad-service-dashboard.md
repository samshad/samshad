---
title: "Unified Ad-Service Revenue Dashboard"
excerpt: "I developed a unified dashboard that consolidates revenue data from multiple ad networks (AdMob, MoPub, AppLovin, AdColony, etc.) into a single MySQL warehouse, providing real-time KPI visualization in Tableau & Excel. This automated solution saved significant manual effort and improved ad performance."
collection: portfolio
# github_link: https://github.com/samshad
---

During my time at **Free Pixel Games Ltd.**, I identified a critical need: a clear, consolidated view of daily earnings across all our ad networks. My solution was to build a comprehensive tool that answered the simple but vital question, *"How much did we actually earn today, across every single ad network?"* – and to do it automatically.

**Key Contributions & The Impact I Made:**

*   **Automated Multi-Network Data Ingestion:**
    *   I engineered robust headless Python scrapers (using Selenium and BeautifulSoup) and utilized REST APIs to automatically pull daily earnings, eCPM, fill-rate, and error data from numerous ad networks including **AdMob, MoPub, AppLovin, AdColony, and others.**
    *   A key challenge I overcame was standardizing the various disparate CSV formats from these networks into a single, common schema for consistent analysis.
*   **Centralized & Efficient Data Warehouse:**
    *   I designed and implemented a normalized data structure in **MySQL**. This central warehouse enables fast data joins, allowing for quick cross-network comparisons and trend analysis.
    *   I built incremental ETL jobs that reliably append approximately **50,000 new rows of data each month** with zero downtime, ensuring the dashboard always has the latest information.
*   **Single-Page Analytics Dashboard for Clear Insights:**
    *   I created a comprehensive, single-page dashboard using **Tableau** (with an Excel Power Query version as a fallback) to display revenue, impressions, fill rate, and network health metrics side-by-side.
    *   The dashboard features conditional formatting to instantly flag under-performing ad placements, enabling quick action.
*   **Proactive Alerting & Trend Identification:**
    *   I developed a simple yet effective Python-based rule engine that automatically emails alerts for anomalies, such as a significant (e.g., ≥10%) drop in eCPM.
    *   The visualized trend lines in the dashboard clearly revealed seasonality in ad performance, directly informing strategies for ad unit optimization.
*   **Significant Operational Improvements:**
    *   This automated solution drastically **reduced manual spreadsheet work by over 80%** (slashing daily effort from two hours to less than 15 minutes).
    *   Empowered by these clear insights, the product team was able to optimize ad spend and successfully **increased the blended fill-rate by approximately 8%**.

**What This Project Showcases About My Skills:**

*   **End-to-End Data Solution Development:** From automated data extraction and warehousing to insightful visualization and alerting.
*   **Automation & Efficiency:** Proven ability to identify inefficiencies and build solutions that save significant time and resources.
*   **Data Engineering & Warehousing:** Expertise in web scraping, API integration, data cleaning, schema design (MySQL), and ETL processes.
*   **Business Intelligence & Visualization:** Proficiency in creating actionable dashboards with tools like Tableau and Excel Power Query that drive decision-making.
*   **Problem-Solving & Initiative:** Taking ownership of a business challenge and delivering a high-impact solution.

**Key Technologies I Mastered & Applied:** Python, Selenium, BeautifulSoup, REST APIs, Pandas, MySQL, Tableau, Microsoft Excel (Power Query), Cron, ETL processes.
