---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["architecture", "nextjs", "system-design"]
domain: "Projects/OnboardIQ"
---

# Summary
Architecture plan utilizing Next.js App Router for frontend/backend BFF, with PostgreSQL as the relational data layer.

# Key Concepts
- **Frontend Architecture**: Next.js client components using Tailwind for styles, Zustand for layout state.
- **Backend Architecture**: Next.js Route Handlers acts as REST endpoints. External task runners for automated account provisioning.
- **Data Architecture**: Relational PostgreSQL database featuring tables for Users, ChecklistTemplates, UserChecklists, TaskStatus, and OrgNodes.

# Related Notes
- [[01 Projects/OnboardIQ/Technical Decisions|OnboardIQ Technical Decisions]]
- [[System Design]]
