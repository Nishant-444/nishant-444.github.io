---
layout: project
type: project
image: img/viztube/viztube.jpg
title: "VizTube"
date: 2026-07-01
published: true
labels:
  - TypeScript
  - Node.js
  - FastAPI
  - PostgreSQL (pgvector)
  - Docker
  - AWS
  - AI / RAG
  - Groq & OpenRouter
summary: "Production video platform backend featuring an AI-Powered RAG engine, Groq Whisper audio transcription, pgvector similarity search, and a decoupled FastAPI worker on AWS EC2."
---

# VizTube - Video Platform with AI-Powered RAG Engine (v2.1)

**VizTube** is a resource-optimized production backend for a video-sharing platform, featuring a microservice architecture and an AI-powered RAG pipeline optimized for constrained cloud environments.

### Key Engineering Achievements

- **AI-Powered RAG Pipeline (v2.1):** Engineered an intelligent Retrieval-Augmented Generation pipeline allowing natural language querying of video transcripts. Integrated **Groq API (Whisper-large-v3)** for cloud audio transcription to prevent CPU overload on small instances.
- **pgvector Vector Database:** Generated vector embeddings locally using **Hugging Face `all-MiniLM-L6-v2`** (~90MB RAM footprint) and executed cosine distance vector searches directly inside PostgreSQL using **pgvector** (`<=>` operator), saving hundreds of megabytes by omitting extra vector database containers like ChromaDB.
- **Decoupled FastAPI Worker:** Architected an independent Python microservice (**FastAPI**) for ML ingestion and similarity queries, keeping the core **Node.js/Express** API clean and responsive.
- **AWS EC2 Resource Optimization (1GB RAM):** Containerized the multi-service stack (Node.js API + PostgreSQL + FastAPI AI Worker) using **Docker Compose** with strict memory boundaries and automated health checks on an **AWS EC2 t3.micro** instance.
- **Database Architecture & UUIDv7:** Migrated database primary keys to **UUID v7** (time-ordered, lexicographically sortable) with **Prisma ORM** to optimize B-tree index clustering and prevent fragmentation.
- **Automated DevOps & SSL:** Configured a **GitHub Actions CI/CD pipeline** for automated container builds and deployments, paired with **Cloudflare DNS/SSL** and an **Nginx reverse proxy** with Certbot auto-renewal.

**Source Code:** [GitHub](https://github.com/Nishant-444/VizTube)  
**Live API Endpoint:** [VizTube.me](https://viztube.me)
