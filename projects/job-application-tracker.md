---
layout: project
type: project
image: img/job-application-tracker/job-application-tracker.jpg
title: "Job Application Tracker"
date: 2026-02-27
published: true
labels:
  - TypeScript
  - Next.js
  - React
  - PostgreSQL
  - Prisma
  - Docker
summary: "Full-stack Kanban board leveraging React Server Components, Server Actions, and optimistic UI updates for real-time state management."
---

# Job Application Tracker - Full-Stack Kanban Board

**Job Application Tracker** is a full-stack web application designed to manage the hiring process through a drag-and-drop Kanban interface, built entirely on the Next.js App Router paradigm.

### Key Engineering Achievements

- **Modern React Architecture:** Leveraged React 19 Server Components to fetch board data server-side via Prisma, eliminating client-side loading waterfalls and improving initial render performance.
- **Type-Safe Mutations:** Replaced traditional REST API layers with Next.js Server Actions, handling all database operations, session authentication, and cache invalidation directly on the server.
- **Optimistic State Management:** Engineered a responsive drag-and-drop UI using `dnd-kit` that applies optimistic updates to the client state, rolling back seamlessly if the server-side mutation fails.
- **Algorithmic Data Modeling:** Implemented a float-based ordering system for Kanban columns and cards. This allows for $O(1)$ database updates during mid-list insertions by calculating the midpoint between adjacent elements, avoiding costly cascading database re-indexes.
- **Automated Provisioning:** Integrated Better Auth with custom database lifecycle hooks (`databaseHooks.user.create.after`) to automatically generate default relational records (boards and preset columns) immediately upon user registration.
- **Optimized Containerization:** Designed a multi-stage Dockerfile utilizing the Next.js `standalone` output mode, isolating only the necessary dependencies to drastically reduce the production container's memory footprint and build size.

**Source Code:** [GitHub](https://github.com/nishant-444/job-application-tracker)
**Live API:** [jobs.nishants.dev](https://jobs.nishants.dev/)
