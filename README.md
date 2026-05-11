# Ontime

Ontime is a SaaS scheduling platform serving medical offices, salons, and service-based businesses. It simplifies appointment booking, client file management, payment tracking, and customer engagement through a Customer Club feature. The platform includes robust reporting tools, making it a valuable asset for CEOs and administrators.

As the **Founder and Lead Developer**, I architected and built Ontime end-to-end — from an initial full-stack foundation to a fully cloud-native serverless microservices platform on AWS.

Ontime operates on a freemium model, offering essential features for free with advanced features available as part of a monetized plan.

---

## Architecture

### Version 2 — Cloud-Native (Feb 2023 – Present) | Victoria, BC

The platform was re-architected from the ground up using **Clean Architecture** and **Domain-Driven Design (DDD)**, deployed as a serverless microservices system on AWS:

- **Serverless backend** on AWS Lambda (Node.js) with API Gateway and Cognito for auth — achieving near-infinite horizontal scalability and reducing infrastructure costs by ~60% through a pay-per-invocation model, eliminating idle server provisioning.
- **Optimized data layer** using DynamoDB with single-table design (PK/SK + GSI indexes), improving API response times by ~40% and reducing Lambda cold-start latency.
- **Real-time analytics pipeline** built with DynamoDB Streams → S3 → Glue → Athena, enabling serverless business reporting fully decoupled from the OLTP database with zero production performance impact.
- **Monorepo structure** with shared TypeScript types across the React/TypeScript frontend and backend, applying the MVVM pattern to cleanly separate UI and business logic — reducing integration bugs and improving maintainability.

### Version 1 — Foundation (Nov 2019 – Feb 2023) | Tehran

The initial platform was built as a full-stack system:

- **Backend:** ASP.NET Core + SQL Server
- **Frontend:** React.js + TypeScript + Material-UI
- Full dashboards for appointments, payments, and customer loyalty tracking

---

## Features

**Client Management:**
- Define and manage client profiles and files
- Manage client appointments, payments, and images

**Appointment Management:**
- Daily dashboard with daily and monthly calendar views

**Customer Engagement:**
- Customer Club for client loyalty and engagement

**Specialist Management:**
- Define and manage specialists/practitioners

**Reporting:**
- Payment reports filtered by specialist and time period
- Customer Club reports
- Debtors reports
- Introductory reports

> **Note:** Currently, Ontime is available in Persian. English support is planned.

---

## Tech Stack

| Layer | V1 (Foundation) | V2 (Cloud) |
|---|---|---|
| Backend | ASP.NET Core | AWS Lambda (Node.js) |
| Database | SQL Server | DynamoDB (single-table design) |
| Frontend | React.js + TypeScript + Material-UI | React + TypeScript (MVVM) |
| Auth | — | AWS Cognito |
| API | REST | AWS API Gateway |
| Analytics | — | DynamoDB Streams + S3 + Glue + Athena |
| Architecture | Monolithic | Clean Architecture + DDD + Microservices |

---

## Live Demo

[ontimecore.com](https://ontimecore.com/)

---

## Team 👩‍💻👨‍💻

- **Majid Ghajari** — Founder, Product Owner & Lead Developer (Front-end & Back-end)
  [majidgdotcom@gmail.com](mailto:majidgdotcom@gmail.com)

- **Neda Hajibabaei** — Front-end Developer
  [n.hajibabaei88@gmail.com](mailto:n.hajibabaei88@gmail.com)

---

## Roadmap

- English language support
- Expanded reporting and business insights
- Broader industry support beyond medical — salons, fitness, and general service businesses
