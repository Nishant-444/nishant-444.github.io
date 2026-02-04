---
layout: project
type: project
image: img/viztube/viztube.jpg
title: "VizTube"
date: 2026-01-20
published: true
labels:
  - Node.js
  - AWS
  - PostgreSQL
  - Prisma
  - Nginx
summary: "Video Infrastructure Migration (Mongo -> Postgres). Optimized for ACID compliance and 1GB RAM constraints."
---

# VizTube - Video Sharing Infrastructure

**VizTube** is a complex video sharing platform where I led the migration from a NoSQL architecture to a relational system to resolve data consistency issues.

### Key Achievements

- **Database Migration:** Migrated from MongoDB to **PostgreSQL** using **Prisma ORM**. This resolved data consistency issues and allowed for better management of complex relational features like user subscriptions and video likes.
- **Infrastructure Optimization:** Hosted on **AWS EC2** within a strict **1GB RAM constraint**. configured **Nginx** as a reverse proxy and used **PM2** for process management to maintain high availability.
- **Security:** Implemented a dual-token JWT authentication strategy and routed traffic through **Cloudflare** to protect against XSS, CSRF, and DDoS vulnerabilities.
- **CI/CD:** Automated the deployment lifecycle using **GitHub Actions**, achieving zero-downtime updates.

**Source Code:** [GitHub](https://github.com/nishant-444/viztube)
**Live Demo:** [VizTube.me](https://www.viztube.me/)
