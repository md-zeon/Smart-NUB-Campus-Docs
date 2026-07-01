---
title: DD-013 - PostgreSQL + Prisma
id: DD-013
status: Accepted
date: 2026-07-01
authors:
  - Zeanur Rahaman Zeon
reviewed_by:
  - Team
---

# Context

Smart NUB Campus manages interconnected academic data, including verified students, profiles, academic resources, discussions, questions and answers, teams, connections, messages, notifications, reputation, and AI interactions.

The platform requires a relational database capable of enforcing data integrity, supporting complex relationships, and scaling as the platform grows.

An Object-Relational Mapping (ORM) tool is also required to simplify database access while maintaining type safety and developer productivity.

---

# Decision

Smart NUB Campus shall use **PostgreSQL** as its primary relational database.

Database access shall be managed through **Prisma ORM**.

All application data shall be modeled using Prisma Schema and managed through Prisma Migrations.

---

# Technology Overview

## Database

- PostgreSQL

## ORM

- Prisma ORM

## Migration System

- Prisma Migrate

## Query Engine

- Prisma Client

---

# Rationale

## Why PostgreSQL?

PostgreSQL provides:

- Strong ACID compliance
- Excellent relational data modeling
- Advanced indexing capabilities
- High reliability
- Excellent performance
- JSON support when needed
- Mature ecosystem
- Scalability for future growth

The platform contains many interconnected entities that naturally fit a relational database model.

Examples include:

- Students ↔ Connections
- Students ↔ Resources
- Students ↔ Teams
- Teams ↔ Members
- Questions ↔ Answers
- Discussions ↔ Comments
- Reputation ↔ Activities

---

## Why Prisma?

Prisma provides:

- End-to-end type safety
- Schema-first development
- Automatic Prisma Client generation
- Migration management
- Excellent TypeScript support
- Improved developer productivity
- Clear database modeling

Using Prisma reduces boilerplate code while improving maintainability.

---

# Database Principles

The database design should follow these principles:

- Normalize data where appropriate.
- Enforce referential integrity.
- Use foreign keys for relationships.
- Prevent duplicate records.
- Support efficient querying.
- Maintain audit information where necessary.
- Design for future scalability.

---

# Consequences

## Positive

- Strong data consistency.
- Excellent relational support.
- Type-safe database operations.
- Easier schema evolution.
- Reliable migrations.
- Better developer experience.
- Scalable architecture.

## Negative

- Requires migration management.
- Developers must understand relational database concepts.
- Complex queries may require optimization as data grows.

---

# Alternatives Considered

## MongoDB

Use a document database.

**Rejected because:**

- The platform contains highly relational data.
- Many-to-many relationships become more complex.
- Data consistency is harder to enforce.

---

## Raw SQL

Write SQL directly without an ORM.

**Rejected because:**

- More repetitive code.
- Lower developer productivity.
- Reduced type safety.
- Harder maintenance.

---

## Drizzle ORM

Use Drizzle instead of Prisma.

**Rejected because:**

- Prisma provides a more mature migration workflow.
- Prisma's tooling and ecosystem better match the team's current experience.
- Prisma integrates well with Better Auth and the planned architecture.

---

# Affected Components

- Database Layer
- Identity Module
- Learning Module
- Community Module
- Network Module
- Collaboration Module
- Communication Module
- Reputation Module
- AI Module
- Administration Module

---

# Related Decisions

- DD-005 — Module-Based Architecture
- DD-007 — Student ID Parsing
- DD-012 — Next.js + Express.js Architecture

---

# References

- Database_Architecture.md
- Entity_Relationship_Diagram.md
- Data_Model.md
