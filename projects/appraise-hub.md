---
layout: project
type: project
image: img/appraise-hub/appraise-hub.png
title: "AppraiseHub"
date: 2026-06-30
published: true
labels:
  - Java
  - Spring Boot
  - Next.js
  - React
  - MySQL
  - JWT
  - Docker
summary: "Full-stack employee appraisal platform featuring multi-role workflows, stateless JWT auth, and an automated review pipeline."
---

# AppraiseHub - Employee Appraisal Platform

**AppraiseHub** is a production-ready, full-stack employee performance and appraisal management platform. It features a robust Spring Boot REST API for business logic and a highly responsive Next.js frontend to guide employees and administrators through complex annual review cycles.

### Key Engineering Achievements

- **Multi-Role RBAC Security:** Engineered a stateless authentication layer using **Spring Security 6.x** and **JJWT 0.12.6**, enforcing strict Role-Based Access Control (RBAC) across `HR`, `MANAGER`, and `EMPLOYEE` accounts.
- **Layered Monolith Architecture:** Developed a clean, decoupled backend following the **Controller-Service-Repository** pattern. DTO mappings isolate Hibernate/JPA persistence entities from external API contracts to maintain API flexibility.
- **Relational Integrity & Schema Design:** Designed an optimized MySQL database schema via **Hibernate 6**, establishing critical database-level constraints to prevent duplicate appraisal cycles per employee and ensure clean audit trails.
- **Modern Dashboard UI:** Built a modern, accessible user interface using **Next.js 16.2.0 (App Router)** and **React 19.2.4**, integrated with **Radix UI** primitives and styled using **Tailwind CSS 4.2** for a fluid user experience.
- **Global Error Handling & Validation:** Structured robust request body validation via `jakarta.validation` coupled with a centralized `@RestControllerAdvice` exception handler to return clean, standardized RFC-compliant error envelopes.
- **Multi-Stage Containerization:** Written optimized multi-stage `Dockerfile` and `docker-compose` files to isolate builds, reducing runtime image sizes and simplifying cloud deployment processes.

**Source Code:** [GitHub](https://github.com/Nishant-444/AppraiseHub)  
**Live Application:** [appraise-hub.vercel.app](https://appraise-hub.vercel.app)
