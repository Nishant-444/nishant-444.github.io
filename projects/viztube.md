---
layout: project
type: project
image: img/viztube/viztube.jpg
title: "VizTube"
date: 2026-01-20
published: true
labels:
  - TypeScript
  - Node.js
  - Docker
  - AWS
  - PostgreSQL
  - CI/CD
summary: "Production-grade video infrastructure on AWS. Dockerized, resource-optimized (1GB RAM), and fully automated."
---

# VizTube - Production Video Infrastructure

**VizTube** is a resource-optimized backend for a video sharing platform, engineered to run a full micro-service architecture on strictly constrained cloud resources.

### Key Engineering Achievements

- **Resource Optimization:** Dockerized the entire stack (Node.js API + PostgreSQL) to run efficiently on a single **AWS EC2 t3.micro (1GB RAM)** instance. Optimized build processes to reduce image size by **~12%**.
- **Automated DevOps:** Architected a CI/CD pipeline using **GitHub Actions** that builds Docker images, pushes to Docker Hub, and deploys to production in **<90 seconds**.
- **Database Migration:** Re-architected the data layer from MongoDB to **PostgreSQL** using **Prisma ORM**. This transition ensured **ACID compliance** for critical features like user subscriptions and view counting.
- **Security Hardening:** Configured **Nginx** as a reverse proxy with SSL/TLS termination and implemented strict **AWS Security Groups** to block direct access to internal API ports.
- **Resilient Media Pipeline:** Designed an asynchronous upload system using Multer (disk buffering) and Cloudinary CDN to prevent **OOM (Out of Memory)** crashes during high-volume traffic.

**Source Code:** [GitHub](https://github.com/nishant-444/viztube)
**Live API:** [VizTube.me](https://www.viztube.me/)
