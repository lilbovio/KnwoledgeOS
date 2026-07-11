---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["architecture-decisions", "adr"]
domain: "Projects/OnboardIQ"
---

# Summary
Architectural Decisions (ADR) log for OnboardIQ.

# Key Concepts
1. **Decision**: Use Next.js Route Handlers instead of separate Express server.
   - *Rationale*: Simplifies deployment, minimizes infrastructure cost, offers excellent serverless execution on Vercel.
2. **Decision**: PostgreSQL over MongoDB.
   - *Rationale*: Strong relational requirements (Users -> Orgs -> Checklists) require ACID compliance and foreign key safety.
