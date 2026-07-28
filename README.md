# Enterprise AI Operations Center (AIOps)

## A Unified Multi-LLM Gateway, Governance, Observability & Root Cause Analysis Platform

---

## Project Overview

Enterprise AI Operations Center (AIOps) is a cloud-native SaaS platform that provides a unified gateway for managing multiple AI providers. Instead of applications directly connecting to different AI providers, all requests pass through a centralized AI Gateway that handles authentication, routing, governance, caching, analytics, monitoring, and root cause analysis.

The platform simplifies enterprise AI management by offering a single interface to multiple AI providers while providing complete visibility into AI usage, operational costs, provider health, and system performance.

---

## Problem Statement

Organizations increasingly use multiple AI providers such as Groq, GPT, Gemini, and Claude. Managing these providers individually creates several challenges:

- Multiple provider integrations
- No centralized monitoring
- High AI operational costs
- Lack of governance and policy enforcement
- Poor visibility into AI usage
- Difficult troubleshooting
- Vendor dependency

---

## Vision Statement

To build a scalable, secure, provider-agnostic AI operations platform that enables enterprises to monitor, govern, optimize, and analyze AI usage through a centralized management system.

---

## Target Users (Personas)

- Super Admin
- Organization Admin
- Team Admin
- Developer
- Viewer

---

## Key Features

- Secure JWT Authentication
- Role-Based Access Control (RBAC)
- Multi-Tenant Organization Management
- Unified AI Gateway
- Groq API Integration
- Mock GPT, Gemini, and Claude Providers
- Intelligent Routing Engine
- Redis Caching
- Analytics Dashboard
- Cost Governance
- Provider Health Monitoring
- Audit Logging
- Notification System
- Root Cause Analysis (RCA)
- Real-Time Dashboard using WebSockets
- Docker Support
- Cloud Deployment

---

## Technology Stack

### Frontend
- React
- TypeScript
- Tailwind CSS
- React Router
- React Query
- Axios
- Recharts
- React Flow
- Framer Motion

### Backend
- Java 21
- Spring Boot
- Spring Security
- JWT Authentication
- Spring Data JPA
- Hibernate
- Maven

### Database
- PostgreSQL (Neon)

### Cache
- Redis (Upstash)

### Deployment
- Vercel
- Render
- Docker
- Docker Compose

---

## Success Metrics

- Secure authentication for all users
- Unified access to multiple AI providers
- Real-time analytics and monitoring
- Intelligent provider routing
- Reduced AI costs using caching
- Effective governance and policy enforcement
- Accurate root cause analysis
- Successful cloud deployment

---

## Assumptions

- Internet connectivity is available.
- Groq API is accessible.
- PostgreSQL and Redis services are available.
- Users have valid credentials.

---

## Constraints

- Groq is the only real AI provider.
- Other AI providers are simulated.
- Free-tier cloud services are used.
- Development timeline is approximately 25 days.

---

## Branching Strategy

This project follows **GitHub Flow**.

```
main
   │
feature/authentication
   │
Pull Request
   │
Merge into main
```

Each new feature will be developed in a separate feature branch before being merged into the main branch.

---

## Quick Start – Local Development

```bash
# Clone the repository
git clone <repository-url>

# Navigate to the project
cd enterprise-ai-operations-center

# Start the application
docker compose up
```

---

## Development Tools

- Java 21
- Spring Boot
- React
- VS Code
- IntelliJ IDEA
- PostgreSQL
- Redis
- Docker Desktop
- Git & GitHub
- Postman
- Draw.io
- Figma

---

## License

This project is developed for academic purposes as part of the B.Tech CSE (AI & ML) Software Engineering Capstone Project at VIT Chennai.