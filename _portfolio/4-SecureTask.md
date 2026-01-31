---
title: "SecureTask – Identity Verification & Real-Time Task Management"
excerpt: "Architected a fully serverless identity verification platform integrating AWS Rekognition for biometric security and CloudFormation for rapid, repeatable infrastructure deployment."
collection: portfolio
# github_link: https://github.com/samshad/SecureTask
---

**The Engineering Challenge:**
To engineer a secure, low-maintenance environment for real-time collaboration that requires strict identity proofing. The objective was to implement biometric verification without the operational overhead of managing GPU servers, while ensuring the infrastructure could scale to zero to minimize costs.

**Cloud-Native Architecture & Security:**

* **Serverless Identity Pipeline:**
    * Implemented **AWS Rekognition** to automate identity verification, matching live user selfies against uploaded government IDs with **> 80% accuracy**.
    * Designed a secure authorization flow where successful biometric verification triggers **AWS Lambda** to issue a signed **JWT**, ensuring only verified identities can access the protected task board.
* **Event-Driven Async Processing:**
    * Utilized an **SNS to Lambda fan-out pattern** to handle real-time task synchronization. This decoupled architecture ensures that updates to **DynamoDB Streams** propagate instantly to connected clients without blocking the main application thread.
* **Data Security Best Practices:**
    * Enforced zero-trust storage principles by using **S3 Presigned URLs** for temporary access to sensitive ID documents, ensuring no permanent public access links exist.
    * **DynamoDB** was configured for single-digit millisecond latency to handle user profiles and audit logs at scale.

**DevOps & Infrastructure as Code (IaC):**

* **Automated Deployment:**
    * Codified the entire infrastructure using **AWS CloudFormation**. This allows the complete stack (API Gateway, Lambda, Databases, Buckets) to be provisioned from scratch in **<5 minutes**, facilitating rapid disaster recovery and consistent testing environments.
* **Cost Optimization:**
    * By selecting a pay-per-use serverless architecture over a traditional containerized (ECS/EKS) cluster, I reduced projected infrastructure costs by **~40%**, eliminating idle resource waste.

**Technologies Leveraged:** Python, AWS Lambda, DynamoDB, S3, AWS Rekognition, SNS, API Gateway, CloudFormation, React, Docker, JWT.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/CSCI-5409-Adv.-Topics-in-Cloud-Computing)

### Architecture Snapshot

<p align="center">
    <img src="/images/system-design/SecureTask_Flow.webp" alt="SecureTask System Design" width="60%"><br>
    <em>Figure: An overview of the SecureTask system design, highlighting the flow of data and interactions.</em>
</p>
