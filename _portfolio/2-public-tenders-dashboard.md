---
title: "Awarded Public Tenders Analysis Dashboard"
excerpt: "Engineered a visual analytics platform that replaces manual spreadsheet workflows with real-time insights, utilizing BERTopic for NLP trend detection across 10 years of procurement data."
collection: portfolio
# github_link: https://github.com/samshad/public-tender-analysis-dashboard
---

**The Engineering Challenge:**
Legacy procurement analysis relied on manual reviews of static spreadsheets, making it impossible to identify shifting purchasing priorities across a decade of data. The objective was to architect a scalable analytics tool that could ingest messy government data and surface hidden trends automatically.

**Core Architecture & Implementation:**

* **Visual Analytics Engine:** Built a reactive Single Page Application (SPA) using **Python Dash** and **Plotly**. This replaced static reporting with dynamic filtering (by buyer, supplier, contract value), enabling deep-dive granularity that was previously impossible.
* **Unstructured Data Processing (NLP):**
    * Applied **BERTopic** to perform unsupervised topic modeling on 10 years of unstructured tender descriptions.
    * This successfully clustered thousands of diverse contracts into coherent themes, visualizing how government spending priorities evolved year-over-year.
* **Automated ETL Pipeline:**
    * Engineered a robust ETL script to parse, clean, and normalize disparate CSV/JSON exports from government portals.
    * **Impact:** Reduced dataset noise by **~35%** by handling missing values and standardizing vendor names, ensuring downstream accuracy.
    * Configured daily automated refreshes to ensure the dashboard serves real-time decision support.

**Business Impact:**

* **Operational Efficiency:** Accelerated the identification of procurement trends by **~30%**, eliminating hours of manual data crunching.
* **Strategic Visibility:** Transformed raw text into strategic intelligence, allowing analysts to visualize vendor concentration and spending anomalies instantly.

**Technologies Leveraged:** Python, Dash, Plotly, Pandas, BERTopic (NLP), scikit-learn, Docker, AWS EC2.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/public-tender-analysis-dashboard)

### Dashboard Snapshot

<p align="center">
  <img src="/images/system-design/tender-dashboard.webp" alt="Public Tenders Dashboard Screenshot" width="50%">
  <br>
  <em>Figure: A glimpse of the interactive dashboard, bringing procurement trends to life.</em>
</p>