---
title: "Serverless Sentiment Analysis for Hotel Customer Feedback"
excerpt: "I built a cost-efficient, fully serverless platform that captures hotel guest feedback in real-time, delivering instant sentiment insights using AWS Lambda, DynamoDB, and Google Cloud's Natural Language API – all without server upkeep."
collection: portfolio
# github_link: https://github.com/samshad/CSCI-5410-Serverless-Data-Processing
---

This project demonstrates how a lean, event-driven architecture can turn raw guest comments into actionable sentiment dashboards. Without any server maintenance.

**Key Achievements & Features:**

*   **Truly Serverless & Cost-Effective Backend:** I engineered the entire backend using AWS Lambda functions to handle all feedback operations (creating, reading, updating, deleting). AWS API Gateway was used to provide secure and throttled access.
    *   **Impact:** This serverless approach not only cut out server maintenance entirely but also led to a **~50% reduction in infrastructure costs and management time** due to pay-per-use billing, and achieved **~30% faster feedback processing** compared to a container-based prototype.
*   **Real-Time, Accurate Sentiment Analysis:** As soon as feedback is submitted, it's analyzed by Google Cloud Natural Language API. This instantly classifies each comment as positive, neutral, or negative.
    *   **Accuracy:** Achieved an impressive **~98% classification accuracy** in benchmark testing, ensuring reliable insights.
*   **Responsive, Event-Driven Data Storage:** I used DynamoDB to store all guest feedback, sentiment scores, and summary metrics. DynamoDB Streams then automatically trigger other Lambda functions to aggregate data, ensuring Key Performance Indicators (KPIs) on the dashboard are refreshed almost instantly.
*   **Intuitive Frontend for Staff & Clear Visualizations:**
    *   I developed a lightweight and responsive interface using React and Bootstrap CSS, allowing hotel staff to easily view, filter, and manage feedback on the fly.
    *   Dynamic charts and dashboards created in Looker Studio clearly highlight sentiment trends and pinpoint service areas needing attention.

**What This Project Showcases:**

*   **Expertise in Serverless Architecture:** Designing and implementing scalable, cost-efficient solutions using AWS Lambda, API Gateway, and DynamoDB.
*   **Real-Time Data Processing & NLP:** Integrating cloud-based AI services (Google Cloud NLP) for immediate and accurate sentiment analysis.
*   **Event-Driven Systems:** Building responsive applications that react to data changes instantaneously.
*   **Full-Stack Capabilities:** Developing both the serverless backend (Python) and a user-friendly frontend (React, Bootstrap CSS, JavaScript).
*   **Focus on Operational Efficiency & Cost Reduction:** Demonstrating how modern cloud paradigms can significantly improve performance and lower expenses.

**Technologies I Leveraged:** Python, AWS Lambda, DynamoDB, API Gateway, Google Cloud NLP, React, Bootstrap CSS, Looker Studio, JavaScript.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/CSCI-5410-Serverless-Data-Processing)

### Architecture Snapshot

<p align="center">
  <img src="https://raw.githubusercontent.com/samshad/samshad/refs/heads/master/images/samshad/Feedback_Architechture.webp" alt="Serverless Sentiment Analysis Architecture" width="70%">
  <br>
  <em>Figure 1: The event-driven pipeline: from raw user feedback to processed sentiment insights.</em>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/samshad/samshad/refs/heads/master/images/samshad/Dashboard_Architechture.webp" alt="Dashboard Architecture" width="70%">
  <br>
  <em>Figure 2: How processed data flows to the Looker Studio dashboard for visualization.</em>
</p>
