---
title: "Serverless Sentiment Analysis for Hotel Customer Feedback"
excerpt: "A cost-efficient, fully serverless platform that captures hotel guest feedback and delivers real-time sentiment insights via AWS Lambda, DynamoDB, and Google Cloud Natural Language API."
collection: portfolio
# github_link: https://github.com/samshad/CSCI-5410-Serverless-Data-Processing
---

This project demonstrates how a lean, event-driven architecture can turn raw guest comments into actionable sentiment dashboards. Without any server maintenance.

**Key Contributions & Features:**
* **True Serverless Backend**
  * AWS Lambda functions power all CRUD operations for feedback entries.  
  * AWS API Gateway secures and throttles public endpoints.
* **Real-Time Sentiment Analysis**
  * Google Cloud Natural Language API classifies each comment as positive, neutral, or negative on ingestion.  
  * Achieved ~ 98 % classification accuracy in benchmark testing.
* **Event-Driven Data Store**
  * DynamoDB tables store feedback, sentiment scores, and summary metrics.  
  * Streams trigger aggregation Lambdas for near-instant KPI refresh.
* **Frontend & Visualization**
  * Lightweight React and Tailwind interface lets hotel staff view, filter, and delete feedback on the fly.  
  * Dynamic charts on Looker Studio highlight sentiment trends and service pain points.
* **Operational Impact**
  * ~ 30 % faster processing versus a container-based prototype.  
  * ~ 50 % reduction in infrastructure management time and costs thanks to pay-per-use billing.

**Technologies Used:** Python, AWS Lambda, DynamoDB, API Gateway, Google Cloud NLP, React, Tailwind CSS, Looker Studio, JavaScript.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/CSCI-5410-Serverless-Data-Processing)

### Architecture Snapshot

<p align="center">
  <img src="https://raw.githubusercontent.com/samshad/samshad/refs/heads/master/images/Feedback_Architechture.jpg" alt="Serverless Sentiment Analysis Architecture" width="70%">
  <br>
  <em>Figure 1: Event-driven pipeline from user feedback to sentiment insights</em>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/samshad/samshad/refs/heads/master/images/Dashboard_Architechture.jpg" alt="Dashboard Architecture" width="70%">
  <br>
  <em>Figure 2: Pipeline feeding the Looker Studio dashboard</em>
</p>
