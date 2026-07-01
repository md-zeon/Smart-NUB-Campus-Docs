---
title: DD-006 - Network Instead of Connections
id: DD-006
status: Accepted
date: 2026-07-01
authors:
  - Zeanur Rahaman Zeon
reviewed_by:
  - Team
---

# Context

During the architectural design of Smart NUB Campus, one of the core modules was initially referred to as **Connections** because its primary responsibility was managing student connection requests and accepted connections.

As the platform evolved, additional features were planned for this module, including:

- Student discovery
- Academic profiles
- Skills and interests
- Student search
- Recommendations
- Mutual connections
- Professional academic networking

It became clear that the module's responsibility extended beyond simply managing connections.

---

# Decision

The module shall be named **Network** instead of **Connections**.

Within this architecture:

- **Network** represents the complete academic networking domain.
- **Connections** represents one feature inside the Network module.

---

# Rationale

The term **Network** better reflects the broader purpose of the module.

It encompasses:

- Discovering students.
- Building academic relationships.
- Viewing public academic profiles.
- Searching for peers.
- Managing connections.
- Exploring skills and interests.
- Supporting future recommendation features.

Using **Connections** as the module name would incorrectly imply that its only responsibility is storing connection relationships.

---

# Consequences

## Positive

- More accurate representation of module responsibilities.
- Easier future expansion.
- Better alignment with professional networking concepts.
- Clear distinction between the domain and a single feature.

## Negative

- Requires consistent terminology throughout the documentation.
- Existing references to "Connections" must be updated where they refer to the module rather than the feature.

---

# Alternatives Considered

## Connections

Use "Connections" as the module name.

**Rejected because:**

- Too narrow.
- Describes only one feature.
- Limits the perceived scope of the module.

---

## Social

Use "Social" as the module name.

**Rejected because:**

- Suggests a traditional social networking platform.
- Does not align with the academic purpose of Smart NUB Campus.

---

# Affected Components

- Module Architecture
- Database Design
- API Design
- Navigation
- User Profiles
- Student Discovery
- Search
- Recommendations

---

# Related Decisions

- DD-004 — Academic Collaboration Network
- DD-005 — Module-Based Architecture

---

# References

- Module_Architecture.md
- Functional_Requirements.md
- User_Stories.md
