---
layout: blog
type: blog
title: "The Great Migration: Why I ditched MongoDB for PostgreSQL"
date: 2025-12-29
published: true
labels:
  - Database Engineering
  - System Design
  - PostgreSQL
---

# From NoSQL to ACID Compliance

When I started building **VizTube**, I chose MongoDB. It was flexible, easy to set up, and the JSON-like structure felt natural with JavaScript.

But as the platform grew, I hit a wall. Managing complex relationships—like user subscriptions, video likes, and comment threads—became a nightmare of manual data joins and inconsistent states.

### The Breaking Point

I found myself writing convoluted code just to ensure that when a user deleted their account, their comments didn't turn into "orphan data." MongoDB's eventual consistency wasn't cutting it for a system that needed strict relational integrity.

### The Solution: PostgreSQL + Prisma

I decided to migrate the entire backend to **PostgreSQL**. I used **Prisma ORM** to manage the schema and migrations.

The benefits were immediate:

1.  **ACID Compliance:** Transactions became reliable. No more partial updates.
2.  **Relational Integrity:** Foreign keys ensured that data remained consistent automatically.
3.  **Complex Queries:** What used to be three database calls and a map function became a single SQL join.

This migration taught me that while NoSQL is great for rapid prototyping, relational databases are often the better choice for structured, interconnected data.
