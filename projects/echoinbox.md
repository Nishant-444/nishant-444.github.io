---
layout: project
type: project
image: img/echoinbox/echoinbox.png
title: "EchoInbox"
date: 2026-07-15
published: true
labels:
  - Next.js
  - TypeScript
  - PostgreSQL
  - Prisma
  - NeonDB
  - Vercel AI SDK
  - NextAuth
summary: "Anonymous messaging platform featuring AI-assisted responses via Vercel AI SDK, serverless database connection pooling on NeonDB, and custom JWT authentication."
---

# EchoInbox - Anonymous Messaging & AI-Assisted Responses

**EchoInbox** is a full-stack web application designed for anonymous feedback and message management, featuring real-time AI-powered response suggestions and serverless connection management.

### Key Engineering Achievements

- **Serverless Database Pooling (NeonDB):** Modeled a fully normalized PostgreSQL schema via **Prisma ORM**, integrating **NeonDB serverless connection pooling** to prevent database connection exhaustion under high concurrency on Next.js Edge runtimes.
- **AI-Assisted Streaming Responses:** Integrated **Vercel AI SDK** to generate real-time, context-aware reply suggestions for users, paired with custom client-side debouncing to optimize token usage and prevent API abuse.
- **Custom JWT NextAuth Pipeline:** Designed a credentials authentication flow injecting Zod-validated user state and Resend OTP flags directly into JWT payloads, eliminating redundant database queries during route protection middleware execution.
- **Interactive UI Component Design:** Built a dynamic landing page and message management dashboard using **Next.js App Router**, **Shadcn UI**, and responsive tailwind layout components with toast notifications and confirmation dialogs.

**Source Code:** [GitHub](https://github.com/Nishant-444/echoinbox)
