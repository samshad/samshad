---
title: "Awarded Public Tenders Analysis Dashboard"
excerpt: "I developed an interactive Dash application that uncovers hidden procurement trends within Nova Scotia’s public tender data, using NLP topic modeling and rich visual analytics to provide clear insights."
collection: portfolio
# github_link: https://github.com/samshad/public-tender-analysis-dashboard
---

In this project, I focused on transforming a vast dataset of Nova Scotia's public tender awards into an accessible and powerful tool for procurement analysts. The goal was to move beyond spreadsheets and empower users with real-time insights.

**Here's How I Made It Happen & Key Features:**
*   **An Intuitive & Interactive Dashboard:** I designed and built a user-friendly dashboard using Dash (Python). It allows analysts to:
    *   Instantly filter data by date range, buyer, supplier, and contract value.
    *   Explore dynamic Plotly charts and drill down into detailed tables for deeper investigation.
*   **Uncovering Themes with NLP:** I applied **BERTopic**, a cutting-edge NLP technique, to over 10 years of tender descriptions. This automatically surfaced key underlying themes and topics within the procurement data.
    *   I then visualized how these topic trends evolved over time, offering a clear view of shifting purchasing priorities.
*   **Smart Data Engineering & Automation:** A crucial part of the project was robust data handling:
    *   I developed processes to parse, clean, and normalize messy CSV/JSON tender exports, significantly **reducing data noise by about 35%**.
    *   I built automated ETL (Extract, Transform, Load) scripts that ensure the dashboard is refreshed daily with the latest data.
*   **Delivering Actionable Insights:** The dashboard directly translates data into understanding:
    *   It **improved the speed of identifying trends by approximately 30%** compared to previous manual review methods.

**What This Project Demonstrates:**

*   **End-to-End Analytics Solution:** From raw data ingestion and cleaning to insightful visualization and reporting.
*   **Advanced Data Analysis & NLP:** Practical application of topic modeling (BERTopic) to extract meaningful patterns from text data.
*   **Data Engineering & Automation:** Skills in ETL pipeline development, data cleaning, and scheduling.
*   **Interactive Dashboard Development:** Proficiency in creating dynamic and user-centric tools with Dash and Plotly.
*   **Problem Solving for Real-World Impact:** Creating a solution that directly enhances efficiency and strategic decision-making for procurement professionals.

**Key Technologies I Leveraged:** Python, Dash, Plotly, Pandas, BERTopic, scikit-learn, Docker, AWS EC2.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/public-tender-analysis-dashboard)

### Dashboard Snapshot

<p align="center">
  <img src="https://raw.githubusercontent.com/samshad/samshad/refs/heads/master/images/samshad/tender-dashboard.webp" alt="Public Tenders Dashboard Screenshot" width="50%">
  <br>
  <em>Figure: A glimpse of the interactive dashboard, bringing procurement trends to life.</em>
</p>