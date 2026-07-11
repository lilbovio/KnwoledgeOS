---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["adr", "technical"]
domain: "Projects/POS"
---

# Summary
Decisions log for the POS system infrastructure.

# Key Concepts
- **Decision**: Node-Postgres direct drivers over heavy ORM.
  - *Rationale*: ORM models add overhead during bulk inserts of transactions. Hand-rolled raw SQL ensures optimal query tuning.
