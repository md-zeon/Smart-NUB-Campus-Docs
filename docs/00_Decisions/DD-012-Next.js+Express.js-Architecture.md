---
title: DD-012 - Next.js + Express.js Architecture
id: DD-012
status: Accepted
date: 2026-07-01
authors:
  - Zeanur Rahaman Zeon
reviewed_by:
  - Team
---

# Context

Smart NUB Campus requires a modern, scalable web architecture capable of supporting secure authentication, AI integration, real-time communication, and efficient data management while providing an optimized user experience.

Since the platform consists of multiple independent modules—including Identity, Learning, Community, Network, Collaboration, Communication, Reputation, AI, Administration, and Platform—it requires a clear separation between the presentation layer and the business logic layer.

The architecture should leverage modern Next.js capabilities while maintaining an independent backend that can evolve separately from the frontend.

---

# Decision

Smart NUB Campus shall adopt a **decoupled client-server architecture**.

The frontend shall be developed using **Next.js App Router**.

The backend shall be developed using **Express.js**.

Authentication shall be managed using **Better Auth**.

Database access shall be managed through **Prisma ORM** with **PostgreSQL**.

The frontend shall primarily use **Server Components**, **Server Actions**, and **Next.js Data Cache** for data fetching and mutations.

Real-time communication shall be handled using **Socket.io**.

---

# Architecture Overview

## Frontend

- Next.js (App Router)
- React
- TypeScript
- Tailwind CSS
- shadcn/ui
- Server Components
- Server Actions
- Next.js Data Cache
- Socket.io Client

---

## Backend

- Express.js
- TypeScript
- Better Auth
- Prisma ORM
- PostgreSQL
- Socket.io Server

---

# Communication Strategy

The frontend communicates with the backend using different mechanisms depending on the use case.

| Purpose                 | Technology                 |
| ----------------------- | -------------------------- |
| Page Rendering          | Server Components          |
| Data Mutation           | Server Actions             |
| External / Public APIs  | Route Handlers / REST APIs |
| Authentication          | Better Auth                |
| Real-time Communication | Socket.io                  |

---

# Rationale

This architecture combines the strengths of Next.js and Express.js while keeping both applications independent.

Using Next.js App Router enables:

- Server Components
- Server Actions
- Streaming
- Built-in caching
- Incremental rendering
- Reduced client-side JavaScript
- Improved performance

Express.js provides:

- Flexible API development
- Clear business logic separation
- Easy integration with external services
- Scalable backend architecture

Better Auth provides:

- Secure authentication
- Session management
- OAuth support
- Email/password authentication
- Seamless integration with Next.js and Prisma

Separating frontend and backend allows each application to evolve independently while maintaining a clean API boundary.

---

# Consequences

## Positive

- Independent deployments.
- Clear separation of concerns.
- Scalable architecture.
- Reduced client-side JavaScript.
- Built-in caching and revalidation.
- Easier maintenance.
- Reusable backend APIs.
- Modern authentication system.

## Negative

- Requires API versioning.
- Multiple repositories must be maintained.
- Requires CORS configuration during development.
- Server Actions require careful organization to maintain clear boundaries.

---

# Alternatives Considered

## Fullstack Next.js

Use only Next.js Route Handlers for backend services.

**Rejected because:**

- Business logic becomes tightly coupled with the frontend.
- Independent backend scaling becomes more difficult.
- Real-time infrastructure is harder to organize.

---

## Client-side Data Fetching Libraries

Use React Query or similar libraries for all data fetching and caching.

**Rejected because:**

- Next.js Server Actions provide a more integrated mutation model.
- Next.js Data Cache eliminates many common caching requirements.
- Increases client-side JavaScript and application complexity.

---

## Monolithic Express Application

Serve both frontend and backend from Express.

**Rejected because:**

- Tight coupling between presentation and business logic.
- Less flexible deployment strategy.
- Harder to maintain as the project grows.

---

# Affected Components

- Client Repository
- Server Repository
- Authentication
- API Layer
- Database Layer
- Real-time Communication
- Deployment Strategy

---

# Related Decisions

- DD-003 — Separate Repositories
- DD-005 — Module-Based Architecture
- DD-011 — AI as a Learning Assistant
- DD-013 — PostgreSQL + Prisma
- DD-014 — Socket.io for Real-Time Communication

---

# References

- System_Architecture.md
- Development_Roadmap.md
- Module_Architecture.md
