# Architecture Decision Records (ADRs)

## Overview

This directory contains the **Architecture Decision Records (ADRs)** for the Smart NUB Campus (SNC) project.

An Architecture Decision Record documents an important technical, architectural, or product decision made during the project's lifecycle, including the reasoning behind the decision, alternatives considered, and its long-term consequences.

These records provide a historical log of how the project evolved and help ensure that future contributors understand not only **what** decisions were made, but also **why** they were made.

---

# Purpose

The ADRs aim to:

- Document major architectural and product decisions.
- Preserve design rationale.
- Improve consistency across the project.
- Reduce repeated discussions.
- Assist future contributors in understanding the system.
- Serve as long-term project knowledge.

---

# ADR Lifecycle

Each decision follows a simple lifecycle.

```
Proposed
    ↓
Discussion
    ↓
Accepted
    ↓
Implemented
    ↓
Superseded (if replaced)
```

Most ADRs in this repository are currently in the **Accepted** state.

---

# ADR Naming Convention

Each Architecture Decision Record follows the format:

```
DD-XXX-Decision-Name.md
```

Example:

```
DD-004-Academic-Collaboration-Network.md
```

---

# Decision Categories

The ADRs are organized into three logical groups.

## 1. Identity & Product Vision

These decisions define the project's purpose, scope, identity, and guiding principles.

| ID     | Decision                                   |
| ------ | ------------------------------------------ |
| DD-001 | Verified Students Only                     |
| DD-002 | Documentation-First Development            |
| DD-003 | Separate Repositories                      |
| DD-004 | Academic Collaboration Network             |
| DD-005 | Module-Based Architecture                  |
| DD-006 | Network Instead of Connections             |
| DD-007 | Student ID Parsing                         |
| DD-008 | Manual Verification Before AI Verification |

---

## 2. Product Philosophy

These decisions define how the platform should behave and what it intentionally does **not** become.

| ID     | Decision                                 |
| ------ | ---------------------------------------- |
| DD-009 | No ERP Features                          |
| DD-010 | Trust-Based Networking and Communication |
| DD-011 | AI as a Learning Assistant               |

---

## 3. Technical Architecture

These decisions define the project's technical foundation.

| ID     | Decision                              |
| ------ | ------------------------------------- |
| DD-012 | Next.js + Express.js Architecture     |
| DD-013 | PostgreSQL + Prisma                   |
| DD-014 | Event-Driven Real-Time Communication  |
| DD-015 | University-Agnostic Core Architecture |

---

# Relationship with Other Documentation

The ADRs explain **why** a decision was made.

Other documentation explains **how** that decision is implemented.

| Documentation         | Purpose                                       |
| --------------------- | --------------------------------------------- |
| 00_Decisions          | Why decisions were made                       |
| 01_Project_Foundation | Project vision and scope                      |
| 02_Requirements       | Functional and business requirements          |
| 03_System_Design      | System architecture and implementation design |
| 04_Diagrams           | Visual representations                        |
| 05_UI_UX              | Interface and user experience                 |
| 06_Development        | Development workflow and standards            |

---

# Writing Guidelines

Every ADR should include:

- Context
- Decision
- Rationale
- Consequences
- Alternatives Considered
- Affected Components
- Related Decisions
- References

Each ADR should describe **one significant decision**.

---

# Future ADRs

Additional ADRs should be created whenever a significant architectural or product decision is made.

Examples include:

- Infrastructure changes
- Authentication strategy changes
- AI architecture changes
- Deployment strategy
- Search engine architecture
- File storage strategy
- Performance optimization strategy

---

# Current Status

**Total ADRs:** 15

- Identity & Product Vision: 8
- Product Philosophy: 3
- Technical Architecture: 4

The ADR collection currently defines the architectural foundation of Smart NUB Campus and serves as the primary reference for future system design and implementation decisions.
