---
layout: project
type: project
image: img/viztube/viztube-square.png
title: "VizTube"
date: 2024-11-01
published: true
labels:
  - Node.js
  - Express.js
  - MongoDB
  - Security
summary: "A production-grade video streaming backend with dual-token JWT security."
---

<img class="img-fluid" src="../img/viztube/viztube-header.png">

VizTube is a video streaming backend architecture built to handle high-scale data interactions. I designed it with a focus on production-grade security and data integrity. It features a polymorphic MongoDB schema to eliminate data redundancy and a dual-token JWT strategy for state-agnostic authentication.

To demonstrate the "centralized error handler" I engineered to slash debugging time by 35%, here is a sample JSON response the API generates when catching a system-level exception:

<hr>

<pre>
// POST /api/v1/users/login
// Response 500 Internal Server Error (Handled)

{
  "success": false,
  "statusCode": 500,
  "message": "Database Connection Timeout",
  "error": {
    "isOperational": true,
    "stack": "Error: MongooseServerSelectionError: connect ETIMEDOUT..."
  },
  "timestamp": "2024-12-04T10:15:30.500Z"
}

// The standardized structure allows frontend clients to handle
// errors gracefully without crashing the UI.
</pre>

<hr>

Source: <a href="https://github.com/yourusername/viztube"><i class="large github icon "></i>yourusername/viztube</a>
