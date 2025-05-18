---
title: "Awarded Public Tenders Analysis Dashboard"
excerpt: "An interactive Dash application that uncovers procurement trends in Nova Scotia’s public-tender dataset using NLP topic modeling and rich visual analytics."
collection: portfolio
# github_link: https://github.com/samshad/public-tender-analysis-dashboard
---

This project delivers an end-to-end analytics pipeline and dashboard that empowers procurement analysts to explore and monitor Nova Scotia public-tender awards data.

**Key Contributions & Features:**
* **Interactive Dash Dashboard:**
  * Enables real-time filtering (date range, buyer, supplier, contract value).
  * Presents dynamic Plotly charts, and drill-down tables for deep dives.
* **NLP-Driven Topic Modeling:**
  * Applied **BERTopic** to over 10 years of tender descriptions, surfacing latent procurement themes.
  * Topic trends visualized over time to highlight emerging purchasing priorities.
* **Data Engineering & Cleaning:**  
  * Parsed and normalized CSV/JSON tender exports, reducing noise by ~35 %.
  * Automated ETL scripts schedule updates and refresh the dashboard daily.
* **Insight Generation:**  
  * Improved trend identification by ~30 % versus manual spreadsheet review.  
  * Flagged high-value contracts and supplier concentration risks via percentile-based alerts.

**Technologies Used:** Python, Dash, Plotly, Pandas, BERTopic, scikit-learn, Docker, EC2.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/public-tender-analysis-dashboard)

### Dashboard Snapshot

<p align="center">
  <img src="https://raw.githubusercontent.com/samshad/samshad/refs/heads/master/images/tender-dashboard.jpg" alt="Public Tenders Dashboard Screenshot" width="50%">
  <br>
  <em>Figure — Interactive dashboard revealing procurement trends and KPIs</em>
</p>