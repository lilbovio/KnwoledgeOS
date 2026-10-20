---
created: 2026-06-23
updated: 2026-10-19
status: "Active"
tags: ["software-engineering", "best-practices", "rest", "api-design", "backend", "web-architecture"]
domain: "Knowledge/Software-Engineering"
---

# Summary
Representational State Transfer (REST) is an architectural style—not a protocol—designed to facilitate reliable, standardized communication across heterogeneous platforms, languages, and environments in the modern API economy.

# Key Concepts

## The API Economy & Heterogeneous Systems
Modern business applications rarely exist in isolation. Distributed enterprises rely on web APIs to bridge disparate systems (e.g., Autonomous Databases, Lakehouses, ERPs, cloud microservices) reliably and securely across varying programming languages and environments.

## The 6 Architectural Constraints of REST
1. **Uniform Interface**: Standardizes interaction across resources using URI identifiers, standard representations (JSON), self-descriptive messages, and hypermedia (HATEOAS).
2. **Statelessness**: Every request contains all context needed for execution. The server retains no persistent client session between requests, maximizing horizontal scalability.
3. **Client-Server Separation**: Strict separation of concerns allows user interface components (React, mobile clients) and data storage layers to evolve independently.
4. **Cacheability**: Responses explicitly declare whether they can be cached by clients or intermediaries, optimizing bandwidth and latency.
5. **Layered System**: Components are structured hierarchically; clients interact through an endpoint without needing to know whether they communicate directly with the upstream server or through reverse proxies, API gateways, and load balancers.
6. **Code on Demand (Optional)**: Servers can optionally extend client capabilities dynamically by sending executable code (e.g., client-side scripts).

## Resource-Oriented Design vs. RPC Antipatterns
REST structures systems around tangible data resources rather than procedural actions:
- **The Antipattern (RPC-style URL actions)**:
  - `GET /getuserby?id=123`
  - `POST /createneworder`
  - `POST /deleteUser`
- **The RESTful Standard**:
  - URIs represent **nouns / resources**; standard HTTP verbs represent **actions**:
    - `GET /users/123` $\to$ Fetch user 123.
    - `POST /orders` $\to$ Create a new order.
    - `DELETE /users/123` $\to$ Delete user 123.

## URI Anatomy & Diagnostic Routing
Understanding how URIs break down into routing tiers:

```
https://api.system.com/users/402/orders?status=shipped&sort=date
|<------------------->||<-------------->||<------------------------>|
         Host                 Path                     Query
```

- **Host (`https://api.system.com`)**: Base network address or API gateway domain.
- **Path Parameters (`/users/402/orders`)**:
  - Identifies a specific resource or nested resource collection.
  - Dictates structural hierarchy (`/users/{userId}/orders`).
  - Mandatory for targeting individual entities.
- **Query Parameters (`?status=shipped&sort=date`)**:
  - Modifies, filters, or paginates the returned resource collection.
  - Used for sorting, pagination (`page=1&limit=20`), and property filtering.
  - Optional; omitting them returns default resource sets.

## HTTP Method Matrix
| Method | Idempotent | Safe | Primary Purpose | Typical Status Code |
| :--- | :--- | :--- | :--- | :--- |
| **GET** | Yes | Yes | Retrieve resource representation without side effects | `200 OK` |
| **POST** | No | No | Create a new child resource or submit data | `201 Created` |
| **PUT** | Yes | No | Completely replace existing resource entity | `200 OK` / `204 No Content` |
| **PATCH** | Typically Yes | No | Partially mutate designated fields of a resource | `200 OK` |
| **DELETE**| Yes | No | Destroy or soft-delete target resource | `204 No Content` / `200 OK` |

# Practical Applications
- Structuring clean Express and Next.js REST route handlers across the [[POS System]] and [[OnboardIQ]].
- Integrating cloud data layers (e.g., [[AWS Data Engineering]], Autonomous Databases, Lakehouses) through standard REST microservice interfaces.

# Related Notes
- [[Software Engineering MOC]]
- [[API Design]]
- [[Backend MOC]]
- [[Cloud Computing]]
- [[Databases]]

# References
- The API economy: bridging heterogenaious systems (Keep Note)
- Designing Data-Intensive Applications by Martin Kleppmann
- Clean Code by Robert C. Martin
