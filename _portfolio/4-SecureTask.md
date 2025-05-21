---
title: "SecureTask – Identity Verification & Real-Time Task Management"
excerpt: "I developed a cloud-native web application that innovatively combines AWS Rekognition for secure facial ID verification with a highly responsive React task board, all running seamlessly on a fully managed AWS stack."
collection: portfolio
# github_link: https://github.com/samshad/SecureTask
---

This project was about building a secure and dynamic environment where users could confidently verify their identity and collaborate on tasks in real-time. I focused on leveraging a fully serverless and cloud-native AWS architecture to deliver a snappy, reliable experience without any server management overhead.

**Key Achievements & Features I Delivered:**

*   **Secure Face-ID Onboarding:** I implemented a robust identity verification process using AWS Rekognition. This system matches a user's live selfie against their uploaded ID photo with **over 80% accuracy** (carefully tuned to minimize false acceptances).
    *   Successful verification is key: it triggers the issuance of a JWT, granting access to the task board and ensuring only verified users can proceed.
    *   Real-time sync was achieved using an efficient SNS to Lambda fan-out pattern, keeping DynamoDB streams perfectly aligned.
*   **Robust Cloud-Native Architecture:** I designed and built the entire application on AWS, making smart use of its managed services:
    *   **AWS Lambda** powers all the business logic, ensuring scalability and efficiency.
    *   **API Gateway** provides secure and managed endpoints for all interactions.
    *   **DynamoDB** serves as the high-performance database for user profiles, tasks, and audit logs, delivering single-digit millisecond latency.
    *   **S3** securely stores ID and selfie images, with signed URLs that expire quickly for an added layer of security.
    *   The user-friendly static React front-end is served from an **EC2** instance.
*   **Impressive Scalability & Cost Efficiency:** The serverless design wasn't just about convenience; it brought significant benefits:
    *   The pay-per-use model of Lambda and S3 **slashed infrastructure costs by approximately 40%** compared to a traditional container-based approach.
    *   I created a **CloudFormation template** that can deploy the entire stack in under 5 minutes, perfect for demonstrations and rapid provisioning.

**What This Project Showcases:**

*   **Advanced Cloud-Native Development:** Expertise in designing and implementing solutions using a comprehensive suite of AWS services (Lambda, DynamoDB, S3, Rekognition, SNS, API Gateway, CloudFormation).
*   **Security-Focused Implementation:** Integrating biometric verification (AWS Rekognition) and secure practices like JWTs and expiring signed URLs.
*   **Full-Stack Capabilities:** From backend logic in Python on Lambda to a dynamic React front-end.
*   **Infrastructure as Code (IaC):** Proficiency with CloudFormation for automated and repeatable deployments.
*   **Cost Optimization & Scalability:** Leveraging serverless architectures to build efficient and scalable applications.

**Technologies I Leveraged:** Python, AWS Lambda, DynamoDB, S3, AWS Rekognition, SNS, API Gateway, CloudFormation, React, Tailwind CSS, Docker, JWT.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/CSCI-5409-Adv.-Topics-in-Cloud-Computing)

### Architecture Snapshot

<p align="center">
    <img src="/images/system-design/SecureTask_Flow.webp" alt="SecureTask System Design" width="60%"><br>
    <em>Figure: An overview of the SecureTask system design, highlighting the flow of data and interactions.</em>
</p>
