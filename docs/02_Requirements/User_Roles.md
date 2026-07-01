---
title: User Roles
version: 1.0
status: Draft
last_updated: 2026-07-01
---

# User Roles

## Overview

This document defines the user roles available in Smart NUB Campus (SNC). Roles determine the responsibilities and permissions granted to users after successful authentication.

Verification status is managed separately and is not considered a user role.

---

# Role Hierarchy

```text
Guest
   │
Register
   │
Pending Verification
   │
Approved
   ▼
Student

Administrator
```

Only verified students are granted access to the Smart NUB Campus platform.

---

# Roles

## Guest

A guest is any visitor who has not authenticated.

### Capabilities

- View the landing page.
- Learn about Smart NUB Campus.
- Register for a new account.
- Log in to an existing account.

### Restrictions

Guests cannot:

- Access student profiles.
- Access academic resources.
- Participate in discussions.
- Connect with students.
- Use AI features.
- Send messages.

---

## Student

A Student is a verified Northern University Bangladesh student.

Students are the primary users of the platform.

### Responsibilities

Students should:

- Maintain an accurate profile.
- Share academic knowledge.
- Respect community guidelines.
- Collaborate ethically.
- Contribute positively.

### Permissions

Students can:

### Identity

- View and edit their profile.
- Update profile information.
- Upload a profile picture.

### Learning

- Upload academic resources.
- Browse academic resources.
- Download shared resources.
- Bookmark resources.
- Receive AI-powered study assistance.

### Community

- Ask academic questions.
- Answer questions.
- Participate in discussions.
- Comment on posts.

### Network

- Search students.
- View student profiles.
- Send connection requests.
- Accept or reject connection requests.

### Collaboration

- Create teams.
- Join teams.
- Recruit teammates.

### Communication

- Exchange private messages with accepted connections.
- Receive notifications.

### Reputation

- Earn reputation points.
- Earn badges.
- View contribution history.

---

## Administrator

Administrators maintain the quality, security, and integrity of the platform.

### Responsibilities

Administrators are responsible for:

- Reviewing verification requests.
- Managing users.
- Moderating discussions.
- Reviewing reports.
- Maintaining platform integrity.

### Permissions

Administrators can:

### Identity Management

- Approve student verification.
- Reject verification.
- Suspend accounts.
- Restore accounts.

### Content Management

- Remove inappropriate resources.
- Remove inappropriate discussions.
- Moderate comments.
- Handle reports.

### Platform Management

- View analytics.
- Manage announcements.
- Configure platform settings.

---

# Verification Status

Verification status is independent of user roles.

| Status    | Description                                 |
| --------- | ------------------------------------------- |
| Pending   | Registration submitted and awaiting review. |
| Approved  | Student identity verified.                  |
| Rejected  | Verification request rejected.              |
| Suspended | Student access temporarily disabled.        |

Only students with an **Approved** verification status may access Smart NUB Campus.

---

# Design Decisions

## DD-001

Authentication, authorization, and verification are separate concepts.

Authentication determines:

> Who the user is.

Authorization determines:

> What the user can do.

Verification determines:

> Whether the student is eligible to access the platform.

---

# Future Roles

The following roles are intentionally excluded from Version 1 but may be introduced in future releases:

- Faculty
- Alumni
- Moderator
- Club Representative

---

# Related Documents

- Verification_and_Identity.md
- Business_Rules.md
- Functional_Requirements.md
