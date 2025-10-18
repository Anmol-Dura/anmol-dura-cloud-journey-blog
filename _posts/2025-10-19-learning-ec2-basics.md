---
layout: post
title: "Learning EC2 Basics"
date: 2025-10-19
tags: [aws, cloud, learning]
---

It has been over a month I am going deep into a course that is meant for **Cloud Practitioner(CEF-C02)** on coursera from the recommendation of a lot of people in the internet. There are different modules into it, which is a bigener lv exam which only requires the students to understand the pricing model and how the pricing works. Therefore it only has the surface level understanding of how cloud services are provided in the cloud. The flowing covers the **kinda syllabus**:

# AWS Certified Cloud Practitioner (CLF-C02) Exam Study Guide

This document outlines everything a student needs to learn before attempting the **AWS Certified Cloud Practitioner (CLF-C02)** exam.

---

## 🧭 1. Overview of the Exam

- **Type:** Foundational-level certification.
- **Format:** Multiple choice & multiple response.
- **Duration:** 90 minutes.
- **Cost:** USD $100.
- **Validity:** 3 years.
- **Recommended Experience:** 6 months of basic AWS Cloud and IT experience.

---

## 📘 2. Exam Domains & Weightings

| Domain                                    | Weighting | Description                                                                 |
| ----------------------------------------- | --------- | --------------------------------------------------------------------------- |
| **Domain 1: Cloud Concepts**              | ~24%      | Understand cloud principles, AWS global infrastructure, and benefits.       |
| **Domain 2: Security and Compliance**     | ~30%      | Learn the shared responsibility model, IAM, compliance, and security tools. |
| **Domain 3: Cloud Technology & Services** | ~34%      | Study the core AWS services, their use cases, and architecture basics.      |
| **Domain 4: Billing, Pricing & Support**  | ~12%      | Understand pricing models, billing tools, and support plans.                |

---

## ☁️ Domain 1: Cloud Concepts

**Topics to Learn:**

- What cloud computing is and why businesses use it.
- Benefits of AWS Cloud: scalability, elasticity, reliability, pay-as-you-go pricing.
- AWS global infrastructure: Regions, Availability Zones, Edge locations.
- Cloud deployment models: IaaS, PaaS, SaaS.
- AWS Well-Architected Framework basics.
- AWS Cloud Adoption Framework (CAF).

**Real-World Example:**
Hosting a static website on Amazon S3 and distributing it via CloudFront for global users.

---

## 🔒 Domain 2: Security & Compliance

**Topics to Learn:**

- AWS **Shared Responsibility Model**.
- AWS **Identity and Access Management (IAM)**: users, groups, roles, and policies.
- Multi-Factor Authentication (MFA).
- Encryption at rest vs. in transit.
- Security services overview: AWS KMS, GuardDuty, Inspector, WAF, Shield.
- Compliance frameworks: GDPR, HIPAA, SOC, PCI DSS.
- AWS Artifact and AWS Config basics.

**Real-World Example:**
Setting up an IAM user with restricted permissions and MFA for security.

---

## ⚙️ Domain 3: Cloud Technology & Services

**Topics to Learn:**

### Compute

- **EC2:** Virtual servers in the cloud.
- **Lambda:** Serverless compute.
- **Lightsail:** Simplified hosting for small applications.

### Storage

- **S3:** Object storage for static files.
- **EBS:** Block storage for EC2 instances.
- **Glacier:** Archival storage for long-term data retention.

### Databases

- **RDS:** Managed relational database.
- **DynamoDB:** NoSQL database.
- **Aurora:** High-performance database compatible with MySQL/PostgreSQL.

### Networking

- **VPC:** Isolated virtual network in AWS.
- **Subnets, Route Tables, Internet Gateway, NAT Gateway.**
- **CloudFront:** Content delivery network (CDN).

### Other Services

- **Elastic Load Balancer (ELB), Auto Scaling, CloudWatch, CloudTrail, CloudFormation.**
- **AI/ML:** Rekognition, Comprehend (overview only).

**Real-World Example:**
Deploying a 3-tier web app: EC2 + RDS + S3 + CloudFront with monitoring via CloudWatch.

---

## 💰 Domain 4: Billing, Pricing & Support

**Topics to Learn:**

- AWS pricing models: On-Demand, Reserved Instances, Spot Instances, Savings Plans.
- Total Cost of Ownership (TCO) and Operational vs Capital Expenditure (OPEX vs CAPEX).
- AWS Cost Management tools: Cost Explorer, Budgets, Pricing Calculator.
- AWS Organizations and Consolidated Billing.
- AWS Support Plans: Basic, Developer, Business, Enterprise.

**Real-World Example:**
Using AWS Pricing Calculator to estimate monthly cost for a website.

---

## 🧠 Study Tips

1. **Official Resources**

   - [AWS Certified Cloud Practitioner Exam Guide (PDF)](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf)
   - [AWS Training & Certification](https://aws.amazon.com/training/)
   - [AWS Whitepapers](https://aws.amazon.com/whitepapers/)

2. **Hands-On Practice**

   - Create a free AWS account.
   - Launch an EC2 instance.
   - Create an S3 bucket and upload files.
   - Explore IAM policies and permissions.
   - Use AWS Cost Explorer.

3. **Practice Questions**

   - [Tutorials Dojo](https://tutorialsdojo.com/aws-certified-cloud-practitioner-clf-c02-exam-guide/)
   - [Educative.io Practice Exams](https://www.educative.io/blog/aws-cloud-practitioner-exam-questions-clf-c02)

4. **Connect Concepts to Real Projects**
   - Build a serverless app (API Gateway + Lambda + DynamoDB).
   - Host your React portfolio on S3 + CloudFront.

---

## 🚀 Why This Certification Matters

- Builds foundational cloud understanding.
- Opens doors to AWS Associate-level certifications.
- Strengthens your technical vocabulary and cloud confidence.
- Enhances employability in web dev, DevOps, and cloud roles.

---

**Author:** Anmol Dura  
**Date:** October 2025  
**Purpose:** Personal AWS CLF-C02 Study Notes
