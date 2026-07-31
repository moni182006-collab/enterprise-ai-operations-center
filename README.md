# Enterprise AI Operations Center (AIOps)

> A Unified Multi-LLM Gateway, Governance, Observability & Root Cause Analysis Platform

---

# Vision Statement

To build a centralized AI Operations Platform that enables organizations to securely manage, monitor, govern, and optimize multiple Large Language Models (LLMs) through a single intelligent gateway while providing complete visibility, analytics, cost management, and automated root cause analysis.

---

# Project Overview

Enterprise AI Operations Center (AIOps) is a cloud-native SaaS platform that acts as a centralized control plane for enterprise AI applications.

Instead of applications directly communicating with multiple AI providers, all requests pass through a unified AI Gateway that performs authentication, governance, intelligent routing, caching, analytics, auditing, and observability before forwarding requests to AI providers.

The platform integrates one real provider (Groq API) and multiple simulated providers (Mock GPT, Mock Gemini, and Mock Claude) to demonstrate provider-agnostic AI infrastructure.

---

# Problem Statement

Modern organizations increasingly use multiple AI providers for different workloads. However, this introduces several challenges:

- No centralized AI management
- Vendor lock-in
- High AI operational cost
- Lack of monitoring and observability
- Poor governance and compliance
- No centralized audit logging
- Difficulty identifying failures
- No automated root cause analysis

This project addresses these problems by introducing a centralized AI Operations Layer.

---
# Screenshots
## 1. GitHub Repository
<img width="940" height="481" alt="image" src="https://github.com/user-attachments/assets/abad7663-061c-41ea-8101-fdfe9dca9ea8" />
## 2. GitHub Branches
<img width="954" height="476" alt="image" src="https://github.com/user-attachments/assets/492344d7-e286-49da-87d1-098f1199e25c" />
## 3. GitHub Boards
<img width="959" height="496" alt="image" src="https://github.com/user-attachments/assets/ff107538-ca21-4ad1-8b86-3673f2393eac" />

## 4. ER Diagram (StarUML)
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/28458887-3cd9-44b0-9f8e-8d9e7a3968d4" />

## 5. Use Case Diagram (StarUML)
<img width="1200" height="485" alt="image" src="https://github.com/user-attachments/assets/28c7ae9b-f08a-4876-a76f-464424bc3ac0" />

## 6. Class Diagram (StarUML)
<img width="1408" height="1117" alt="image" src="https://github.com/user-attachments/assets/fce93bfe-8a60-4b8d-8a17-91cf7dd211b3" />

## 7. Architecture Diagram (Draw.io)
<img width="2866" height="2316" alt="AIOps_Architecture (2)" src="https://github.com/user-attachments/assets/a1ed6508-0553-4848-ac7f-7b26a8209b23" />

## 8. Docker Desktop
<img width="952" height="541" alt="image" src="https://github.com/user-attachments/assets/a65abcb8-9bdb-426e-b824-383c6eef1954" />

## 9. Docker Build & Run (Terminal)
<img width="721" height="515" alt="image" src="https://github.com/user-attachments/assets/ae369aa9-8b63-4848-b4f7-085634e8ff3e" />

## 10. Running Web App
<img width="940" height="520" alt="image" src="https://github.com/user-attachments/assets/cee11548-8e46-4c9a-b4ad-6417740c8d6f" />
<img width="940" height="522" alt="image" src="https://github.com/user-attachments/assets/2673d38a-6102-4cea-aeae-d25e5274a49d" />

# Target Users (Personas)

## Super Administrator
- Manage the complete platform
- Configure providers
- Manage organizations
- Monitor overall system health

## Organization Administrator
- Manage teams and users
- Configure governance policies
- Monitor AI usage and budgets

## Team Administrator
- Manage team members
- Monitor team analytics
- Review incidents

## Developer
- Submit AI requests
- Monitor request history
- View provider performance

## Viewer
- Read-only access to dashboards
- View analytics and reports

---

# Key Features

- Multi-LLM AI Gateway
- Provider Adapter Architecture
- Groq API Integration
- Mock GPT Provider
- Mock Gemini Provider
- Mock Claude Provider
- Intelligent Routing Engine
- JWT Authentication
- Role-Based Access Control (RBAC)
- Multi-Tenant Organizations
- Redis Prompt Cache
- Analytics Dashboard
- AI Cost Monitoring
- Governance Policy Engine
- Audit Logging
- Provider Health Monitoring
- Notification System
- Root Cause Analysis Engine
- Real-Time Dashboard
- Docker Support
- Cloud Deployment

---

# Success Metrics

- 99% Gateway Availability
- AI Request Success Rate >95%
- Cache Hit Ratio >70%
- Low Response Latency
- Accurate Root Cause Detection
- Secure Multi-Tenant Access
- Real-Time Monitoring
- Successful Cloud Deployment

---

# Assumptions

- Stable internet connection
- Groq API availability
- Docker installed
- Java 21 installed
- Node.js installed
- PostgreSQL available
- Redis available

---

# Constraints

- Uses Groq free-tier API
- Neon PostgreSQL free tier
- Upstash Redis free tier
- Render free tier backend
- Vercel free tier frontend

---

# Technology Stack

## Frontend

- React
- TypeScript
- Tailwind CSS
- React Router
- React Query
- Axios
- Framer Motion
- Recharts
- React Flow

## Backend

- Java 21
- Spring Boot
- Spring Security
- Spring Data JPA
- Hibernate
- JWT
- Maven

## Database

- PostgreSQL
- Neon PostgreSQL

## Cache

- Redis
- Upstash Redis

## AI

- Groq API
- Mock GPT
- Mock Gemini
- Mock Claude

## DevOps

- Docker
- Docker Compose
- GitHub
- Render
- Vercel

---

# High-Level Architecture

```
Users
   │
   ▼
React Frontend
   │
   ▼
Spring Boot Backend
   │
   ▼
AI Gateway
   │
   ├── Authentication
   ├── Governance
   ├── Routing Engine
   ├── Cache
   ├── Analytics
   └── Audit Logs
   │
   ▼
Provider Adapter Layer
   │
   ├── Groq
   ├── Mock GPT
   ├── Mock Gemini
   └── Mock Claude
   │
   ▼
PostgreSQL + Redis
```

---

# Folder Structure

```
enterprise-ai-operations-center
│
├── backend
├── frontend
├── docs
├── diagrams
├── screenshots
├── docker
├── .github
├── README.md
├── .gitignore
├── docker-compose.yml
└── LICENSE
```

---

# Branching Strategy

This project follows **GitHub Flow**.

```
main
 │
 └── feature/setup-project
```

Development is performed in feature branches and merged into the `main` branch after review and testing.

---

# Quick Start – Local Development

## Prerequisites

- Java 21
- Node.js 20+
- Docker Desktop
- Git
- Maven

## Clone Repository

```bash
git clone https://github.com/moni182006-collab/enterprise-ai-operations-center.git
```

## Open Project

```bash
cd enterprise-ai-operations-center
```

## Build Using Docker

```bash
docker compose up --build
```

## Backend

```
http://localhost:8080
```

## Frontend

```
http://localhost:5173
```

---

# Development Timeline

## Phase 1
Planning, Vision Document, UI Design, Architecture

## Phase 2
Backend Foundation & Authentication

## Phase 3
AI Gateway, Provider Adapters, Routing Engine

## Phase 4
Analytics, Governance, RCA Engine

## Phase 5
Frontend Dashboard Development

## Phase 6
Testing, Docker, Deployment

## Phase 7
Documentation & Presentation

---

# Future Enhancements

- Kubernetes Deployment
- AI Cost Prediction
- Enterprise SSO
- Multi-Cloud Support
- Predictive Incident Detection
- Advanced AI Governance
- Mobile Dashboard
- Auto Scaling

---

# Screenshots

The `screenshots/` folder contains:

- GitHub Repository
- GitHub Branches
- Docker Build
- Docker Compose
- Docker Desktop
- Localhost Application
- Development Environment

---

# License

MIT License

---

# Author

**Monisha S B**

B.Tech Computer Science Engineering (AI & ML)

VIT Chennai

2026
