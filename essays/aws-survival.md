---
layout: essay
type: essay
title: "Surviving Production on 1GB RAM"
date: 2026-02-04
published: true
labels:
  - AWS
  - DevOps
  - Optimization
---

# Deploying VizTube on the Free Tier

Hosting a full-stack video platform on an **AWS t2.micro** instance is not for the faint of heart. You have exactly 1GB of RAM. One memory leak, one unoptimized process, and the server crashes.

Here is how I engineered VizTube to survive in this harsh environment.

### 1. Nginx as the Gatekeeper

I configured **Nginx** as a reverse proxy. [cite_start]Instead of letting Node.js handle static assets (which eats memory), Nginx serves images and CSS files efficiently, leaving Node.js to handle only the API logic.

### 2. PM2 Process Management

I used **PM2** not just to keep the app running, but to limit it. I set strict memory restart limits. [cite_start]If a process exceeded 400MB, PM2 would gracefully restart it before it crashed the entire server.

### 3. Swap Memory

I configured a 2GB swap file on the Linux instance. While disk-based memory is slow, it prevented the OOM (Out of Memory) killer from terminating my database process during traffic spikes.

This experience taught me that **constraints breed creativity**. You don't need a massive server to build scalable software; you just need to understand your resources.
