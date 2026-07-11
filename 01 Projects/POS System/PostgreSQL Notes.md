---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["postgres", "sql"]
domain: "Projects/POS"
---

# Summary
Important queries, optimization rules, and setup guides for POS Postgres database.

# Key Concepts
- **Indexing**: Always index `SKU` and index foreign keys on `sale_items(sale_id)`.
- **Backup Strategy**: Automatic daily cron running `pg_dump` targeting external drive.
