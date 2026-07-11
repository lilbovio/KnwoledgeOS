---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["postmortem", "learnings"]
domain: "Projects/OnboardIQ"
---

# Summary
Retrospective analysis on system design constraints and enterprise integration blockers.

# Key Concepts
- **Enterprise Firewalls**: Integrating with corporate intranets (HPE) requires secure tunnels and VPN configurations.
- **Active Directory Complexity**: Organizational nodes are hierarchical but contain circular cross-reporting. The schema design must support complex tree graph queries.
