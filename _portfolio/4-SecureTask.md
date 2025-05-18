---
title: "SecureTask – Identity Verification & Real-Time Task Management"
excerpt: "A cloud-native web app that fuses AWS Rekognition facial-ID verification with a snappy React task board, all on a fully managed AWS stack."
collection: portfolio
# github_link: https://github.com/samshad/SecureTask
---

The app lets users **register, verify their face against an ID photo, and manage tasks in real time**—all without touching a single server.

**Key Contributions & Features:**
* **Face-ID Onboarding**  
  * AWS Rekognition matches selfie ↔ ID-card with **> 80 % accuracy** (threshold tuned for low false-accept).
  * Verification result drives JWT issuance; unverified users can’t reach the task board.
* **Real-Time Task Board**  
  * Create, update and delete tasks—changes broadcast instantly to all sessions.
  * SNS → Lambda fan-out keeps DynamoDB streams and WebSockets in sync.
* **Cloud-Native Architecture**  
  * **AWS Lambda** for all business logic; **API Gateway** provides secure endpoints.  
  * **DynamoDB** stores user profiles, tasks, and audit logs with single-digit-ms latency.  
  * **S3** hosts ID/selfie images; signed URLs expire quickly for extra security.  
  * Static React front-end served from an **EC2** instance.
* **Scalability & Cost Efficiency**
  * Pay-per-use Lambda/S3 combo cut infra costs vs. a container baseline by ~40 %.  
  * CloudFormation template spins the whole stack up in < 5 min for demos.

**Technologies Used:** Python, AWS Lambda, DynamoDB, S3, Rekognition, SNS, API Gateway, CloudFormation, React, Tailwind CSS, Docker, JWT.

[![Code on GitHub](https://img.shields.io/badge/Source-Code-blue?logo=github)](https://github.com/samshad/CSCI-5409-Adv.-Topics-in-Cloud-Computing)

### Architecture Snapshot

<p align="center">
    <img src="https://raw.githubusercontent.com/samshad/samshad/refs/heads/master/images/SecureTask_Flow.jpg" alt="SecureTask System Design" width="60%"><br>
    <em>Figure — System Design</em>
</p>
