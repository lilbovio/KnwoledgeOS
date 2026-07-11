---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["architecture", "postgres"]
domain: "Projects/POS"
---

# Summary
Monolithic backend paired with Single Page Client. Emphasizes database integrity and transaction performance.

# Key Concepts
- **Architecture**: React SPA + Express REST API.
- **DB System**: PostgreSQL instance hosted locally on local area network servers to maximize speed.
- **Sync System**: WebSockets (Socket.io) broadcasting real-time item stock levels to prevent double-selling.
