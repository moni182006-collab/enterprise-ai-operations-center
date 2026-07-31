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
<img width="746" height="453" alt="image" src="https://github.com/user-attachments/assets/c3840ce8-ae98-4369-a685-28bc149ff239" />


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

# 🏗 High-Level Architecture

The Enterprise AI Operations Center follows a modular, provider-agnostic architecture where every AI request passes through a centralized gateway before reaching an AI provider.

```
                         ┌──────────────────────┐
                         │        Users         │
                         └──────────┬───────────┘
                                    │
                                    ▼
                     ┌─────────────────────────────┐
                     │      React Frontend         │
                     └──────────┬──────────────────┘
                                │ REST APIs
                                ▼
                 ┌────────────────────────────────────┐
                 │      Spring Boot Backend           │
                 └────────────────┬───────────────────┘
                                  │
                                  ▼
                  ┌─────────────────────────────────┐
                  │        AI Gateway               │
                  ├─────────────────────────────────┤
                  │ • Authentication                │
                  │ • Governance Engine             │
                  │ • Routing Engine                │
                  │ • Redis Cache                   │
                  │ • Analytics Engine              │
                  │ • Audit Logging                 │
                  └────────────────┬────────────────┘
                                   │
                                   ▼
                  ┌─────────────────────────────────┐
                  │    Provider Adapter Layer       │
                  ├─────────────────────────────────┤
                  │ • Groq API                      │
                  │ • Mock GPT                      │
                  │ • Mock Gemini                   │
                  │ • Mock Claude                   │
                  └────────────────┬────────────────┘
                                   │
                ┌──────────────────┴──────────────────┐
                ▼                                     ▼
      PostgreSQL Database                    Redis Cache
```

The architecture is designed to ensure:

- Provider independence using the Adapter Pattern
- Intelligent AI routing using the Strategy Pattern
- Enterprise governance and policy enforcement
- High scalability through modular architecture
- Centralized analytics, monitoring, and observability

---

# 📂 Folder Structure

```
enterprise-ai-operations-center
│
├── backend/                        
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   ├── resources/
│   │   │   └── ...
│   │   └── test/
│   ├── Dockerfile                   
│   ├── pom.xml
│   └── mvnw
│
├── frontend/                       
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── hooks/
│   │   ├── utils/
│   │   └── App.tsx
│   ├── Dockerfile                  
│   ├── package.json
│   └── vite.config.ts
│
├── docs/                           
├── diagrams/                    
├── screenshots/                   
├── docker/                      
├── .github/                    
├── docker-compose.yml               
├── .gitignore
├── LICENSE
└── README.md
```

---

# Branching Strategy

This project follows the **GitHub Flow** branching strategy.

## Branches

- **main** – Stable production-ready branch.
- **feature/setup-project** – Initial project setup and Review 1 implementation.
- Future feature branches will follow:

```
feature/authentication
feature/dashboard
feature/gateway
feature/provider-adapters
feature/analytics
feature/root-cause-analysis
feature/deployment
```

## Workflow

1. Create a feature branch from **main**.
2. Implement the assigned feature.
3. Commit changes with meaningful commit messages.
4. Push the feature branch.
5. Create a Pull Request.
6. Review and merge into **main**.

---

# 🚀 Quick Start – Local Development

## Prerequisites

Before running the project, install:

- Java 21
- Maven
- Node.js 20+
- npm
- Git
- Docker Desktop
- PostgreSQL
- Redis

---

## Clone Repository

```bash
git clone https://github.com/moni182006-collab/enterprise-ai-operations-center.git

cd enterprise-ai-operations-center
```

---

## Setup Using Docker (Recommended)

Docker provides the easiest way to run the project without manually configuring Java, Node.js, PostgreSQL, or Redis.

### Step 1 — Build Docker Images

```bash
docker compose build
```

---

### Step 2 — Start the Application

```bash
docker compose up --build
```

The following services will start automatically:

- Frontend → http://localhost:5173
- Backend → http://localhost:8080

---

### Step 3 — Stop Containers

```bash
docker compose down
```

To remove volumes:

```bash
docker compose down -v
```

---

# Docker Support

Enterprise AI Operations Center is fully containerized for simplified local development and deployment.

The project includes:

✅ Spring Boot Backend Docker Image

✅ React Frontend Docker Image

✅ Docker Compose Configuration

✅ Container Networking

✅ Easy Local Development

Future versions will additionally include:

- PostgreSQL Container
- Redis Container
- Hot Reload
- Environment Variable Management
- Production Deployment Configuration

---

# Local Development (Without Docker)

### Backend

```bash
cd backend

./mvnw spring-boot:run
```

Backend runs at:

```
http://localhost:8080
```

---

### Frontend

```bash
cd frontend

npm install

npm run dev
```

Frontend runs at:

```
http://localhost:5173
```

---

# Useful Commands

| Command | Purpose |
|----------|----------|
| docker compose build | Build Docker Images |
| docker compose up | Start Containers |
| docker compose down | Stop Containers |
| docker ps | List Running Containers |
| docker images | List Images |
| git status | Check Repository Status |
| git branch | Show Branches |
| git pull | Pull Latest Changes |
| git push | Push Changes |

---

# Local Development Tools

The following tools are used throughout development:

- Visual Studio Code
- Git
- GitHub
- Java 21
- Spring Boot
- Maven
- React
- TypeScript
- Vite
- Docker Desktop
- PostgreSQL
- Redis
- Postman
- Draw.io
- Figma

---

# Repository

### GitHub Repository

**Repository Link**

> https://github.com/moni182006-collab/enterprise-ai-operations-center

---
# GitHub Project Board

Development follows an Agile workflow using GitHub Issues and Project Boards.

Workflow:

```
Backlog
      ↓

To Do
      ↓

In Progress
      ↓

Testing
      ↓

Done
```

Every module and feature is tracked as a GitHub Issue and managed throughout the project lifecycle.

---

# Development Timeline

| Phase | Description |
|--------|-------------|
| Phase 1 | Planning, Requirements, Architecture & UI Design |
| Phase 2 | Backend Foundation & Authentication |
| Phase 3 | AI Gateway, Provider Adapters & Routing |
| Phase 4 | Analytics, Governance & Root Cause Analysis |
| Phase 5 | Frontend Dashboard Development |
| Phase 6 | Testing, Docker & Cloud Deployment |
| Phase 7 | Documentation & Presentation |

---

# Future Enhancements

- Kubernetes Deployment
- AI Cost Prediction
- Enterprise Single Sign-On (SSO)
- Multi-Cloud AI Support
- Predictive Incident Detection
- AI-based Recommendation Engine
- Mobile Dashboard
- Auto Scaling
- Real-time WebSocket Monitoring
- Advanced Governance Policies

---

# Author

**Monisha S B**
**TEJAL SELVAM**
# 📄 License

This project is licensed under the **MIT License**.
