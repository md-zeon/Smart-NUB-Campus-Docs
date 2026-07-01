---
title: DD-003 - Separate Repositories
id: DD-003
status: Accepted
date: 2026-07-01
authors:
  - Zeanur Rahaman Zeon
reviewed_by:
  - Team
---

# Context

Smart NUB Campus consists of multiple aspects of software development, including documentation, frontend development, backend development, UI/UX design, and system architecture.

Using a single repository for all project assets would tightly couple documentation with implementation, making it more difficult to manage changes, maintain version history, and collaborate effectively.

Since the project follows a documentation-first workflow, the documentation itself should be treated as an independent project.

---

# Decision

Smart NUB Campus shall use separate Git repositories for documentation, frontend, and backend development.

The repositories are:

- Smart-NUB-Campus-Docs
- Smart-NUB-Campus-Client
- Smart-NUB-Campus-Server

Each repository has a distinct responsibility and lifecycle while collectively representing the Smart NUB Campus ecosystem.

---

# Rationale

Separating repositories improves project organization and allows each part of the system to evolve independently.

Benefits include:

- Clear separation of responsibilities.
- Independent version history.
- Cleaner issue tracking.
- Easier code reviews.
- Simpler CI/CD configuration.
- Documentation remains accessible without navigating source code.
- Frontend and backend can be developed independently.

This structure also mirrors the organization commonly used in professional software teams where documentation and implementation are maintained as separate deliverables.

---

# Consequences

## Positive

- Better project organization.
- Cleaner repository structure.
- Independent release management.
- Easier onboarding for contributors.
- Reduced repository complexity.
- Documentation can evolve without affecting application code.

## Negative

- Changes spanning multiple repositories require coordinated updates.
- Contributors must clone multiple repositories.
- Cross-repository version compatibility must be managed.

---

# Alternatives Considered

## Monorepo

Store documentation, frontend, backend, and assets in a single repository.

**Rejected because:**

- Documentation becomes less discoverable.
- Repository grows rapidly in size.
- Harder to manage unrelated changes.
- Increased complexity for contributors interested in only one part of the project.

---

## Documentation Inside Client Repository

Store documentation within the frontend project.

**Rejected because:**

- Documentation becomes tied to frontend development.
- Backend architecture and project planning are no longer independent.
- Reduces documentation visibility.

---

# Repository Responsibilities

## Smart-NUB-Campus-Docs

Responsible for:

- Project documentation
- Requirements
- Architecture
- System design
- Diagrams
- Development standards
- Decision records

---

## Smart-NUB-Campus-Client

Responsible for:

- Next.js application
- UI components
- User experience
- Client-side state management
- Real-time communication
- Frontend testing

---

## Smart-NUB-Campus-Server

Responsible for:

- REST API
- Authentication
- Business logic
- Database access
- AI integration
- Socket.io services
- Backend testing

---

# Affected Components

- Development Workflow
- Git Strategy
- CI/CD
- Documentation
- Frontend Development
- Backend Development

---

# Related Decisions

- DD-002 — Documentation-First Development
- DD-005 — Module-Based Architecture

---

# References

- Development_Roadmap.md
- Coding_Standards.md
- Git_Workflow.md
