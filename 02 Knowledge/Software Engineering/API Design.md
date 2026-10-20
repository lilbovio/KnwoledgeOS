---
created: 2026-06-23
updated: 2026-10-19
status: "Active"
tags: ["software-engineering", "best-practices", "api-design", "backend", "contracts"]
domain: "Knowledge/Software-Engineering"
---

# Summary
Architecting robust integration contracts that are predictable, developer-focused, versioned, and resilient across distributed systems.

# Key Concepts
- **Resource-Oriented Architecture**: Align endpoints with resource entities rather than procedural actions (see [[REST]]).
- **URI Conventions**: Use lowercase kebab-case or plural nouns (`/api/v1/orders`), reserve verbs for HTTP methods.
- **Contract Explicit Versioning**: Expose API versioning via path prefixes (`/v1/`), custom headers (`Accept-Version`), or media types to protect backward compatibility.
- **Consistent Response Formatting**: Return standardized envelope structures for success and error objects:
  ```json
  {
    "data": { ... },
    "error": null,
    "metadata": { "page": 1, "total": 42 }
  }
  ```
- **Proper Status Code Utilization**: Distinguish between client mistakes (`400 Bad Request`, `401 Unauthorized`, `403 Forbidden`, `404 Not Found`, `422 Unprocessable Entity`) and server faults (`500 Internal Server Error`, `503 Service Unavailable`).
- **Pagination, Filtering & Sorting**: Employ query parameters (`?limit=20&offset=40&sort=-created_at`) rather than custom path hacks.
- **Rate Limiting & Idempotency**: Provide headers (`X-RateLimit-*`) and support `Idempotency-Key` headers on mutating requests (`POST`).

# Practical Applications
- Applied in constructing API routes and backend services in [[OnboardIQ]] and [[POS System]].
- Designing external webhook consumption interfaces and client SDK schemas.

# Related Notes
- [[Software Engineering MOC]]
- [[REST]]
- [[Backend MOC]]
- [[Testing]]

# References
- The API economy: bridging heterogenaious systems (Keep Note)
- Designing Data-Intensive Applications by Martin Kleppmann
- Clean Code by Robert C. Martin
