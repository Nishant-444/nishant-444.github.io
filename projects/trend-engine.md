---
layout: project
type: project
image: img/trend-engine/trend-engine.png
title: "Trend-Engine"
date: 2025-08-15
published: true
labels:
  - React.js
  - Appwrite
  - Tailwind CSS
  - Vite
  - TMDB API
summary: "Real-time movie analytics platform. Implemented search debouncing and backend metrics tracking using Appwrite."
---

# Trend-Engine - Real-Time Movie Analytics

**Trend-Engine** is a reactive movie discovery application that goes beyond simple fetching. It implements a live "trending" algorithm driven by actual user search data stored in a backend database.

### Key Achievements

- **Performance Optimization:** Implemented a custom **debouncing algorithm** (500ms delay) for the search input. This drastically reduced API calls to TMDB, preventing rate-limiting and improving client-side performance.
- **Backend Integration:** Utilized **Appwrite** as a Backend-as-a-Service (BaaS) to store search terms and frequency counts, enabling a real-time "Trending Movies" feature based on user behavior rather than static lists.
- **Modern Architecture:** Built with **React 18** and **Vite** for rapid bundling, utilizing a component-based structure for maintainability and scalability.
- **Responsive Design:** Styled with **Tailwind CSS v4**, implementing a mobile-first grid system that adapts from 1 to 4 columns based on viewport size.

**Source Code:** [GitHub](https://github.com/Nishant-444/Trend-Engine)
**Live Demo:** [Trend-Engine](https://trend-engine.vercel.app/)
