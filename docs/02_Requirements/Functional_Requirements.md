---
title: Functional Requirements
version: 1.0
status: Draft
last_updated: 2026-07-01
---

# Functional Requirements

## Overview

This document specifies the functional requirements of Smart NUB Campus (SNC).

Each requirement describes a capability that the platform must provide. These requirements are organized according to the core system modules.

---

# Identity Module

## ID-FR-001

The system shall allow guests to register a new account.

Derived From:

- UC-001
- BR-006

---

## ID-FR-002

The system shall validate the format of every submitted student ID.

---

## ID-FR-003

The system shall automatically derive the student's department, admission year, and admission intake from the student ID.

Derived From:

- BR-004

---

## ID-FR-004

The system shall require students to upload an image of their official university ID card during registration.

---

## ID-FR-005

The system shall create newly registered accounts with a **Pending** verification status.

Derived From:

- BR-006

---

## ID-FR-006

The system shall prevent students with Pending, Rejected, or Suspended verification status from accessing academic modules.

Derived From:

- BR-008
- BR-010

---

## ID-FR-007

The system shall allow approved students to complete their academic profile.

---

# Learning Module

## LRN-FR-001

The system shall allow students to upload academic resources.

---

## LRN-FR-002

The system shall organize resources into academic categories.

---

## LRN-FR-003

The system shall allow students to search academic resources.

---

## LRN-FR-004

The system shall allow students to bookmark resources.

---

## LRN-FR-005

The system shall allow students to download shared resources.

---

# Community Module

## COM-FR-001

The system shall allow students to create academic discussion posts.

---

## COM-FR-002

The system shall allow students to comment on discussions.

---

## COM-FR-003

The system shall allow students to ask academic questions.

---

## COM-FR-004

The system shall allow students to answer academic questions.

---

## COM-FR-005

The system shall allow students to report inappropriate content.

---

# Network Module

## NET-FR-001

The system shall allow students to search for other students.

---

## NET-FR-002

The system shall allow students to filter search results by department, admission year, academic interests, and skills.

---

## NET-FR-003

The system shall allow students to send connection requests.

---

## NET-FR-004

The system shall allow students to include an optional note with connection requests.

---

## NET-FR-005

The system shall allow students to accept or reject connection requests.

---

## NET-FR-006

The system shall display each student's public academic profile.

---

# Collaboration Module

## COL-FR-001

The system shall allow students to create collaboration teams.

---

## COL-FR-002

The system shall allow students to recruit teammates.

---

## COL-FR-003

The system shall allow students to request to join collaboration teams.

---

## COL-FR-004

The system shall allow team creators to manage team membership.

---

# Communication Module

## MSG-FR-001

The system shall allow private messaging between accepted connections.

---

## MSG-FR-002

The system shall provide real-time message delivery.

---

## MSG-FR-003

The system shall notify students when new messages are received.

---

# Reputation Module

## REP-FR-001

The system shall maintain reputation scores for students.

---

## REP-FR-002

The system shall award badges according to predefined achievement criteria.

---

## REP-FR-003

The system shall display a student's reputation and badges on their profile.

---

# AI Module

## AI-FR-001

The system shall provide an AI-powered academic assistant.

---

## AI-FR-002

The AI assistant shall answer academic questions.

---

## AI-FR-003

The AI assistant shall summarize study materials.

---

## AI-FR-004

The AI assistant shall generate study plans.

---

## AI-FR-005

The AI assistant shall assist students in generating project and research ideas.

---

# Administration Module

## ADM-FR-001

The system shall allow administrators to review verification requests.

---

## ADM-FR-002

The system shall allow administrators to approve or reject verification requests.

---

## ADM-FR-003

The system shall allow administrators to manage users.

---

## ADM-FR-004

The system shall allow administrators to moderate discussions and resources.

---

## ADM-FR-005

The system shall allow administrators to manage reports.

---

## ADM-FR-006

The system shall provide administrators with platform analytics.

---

# Requirement Traceability

| Module         | Related Use Cases      | Related Business Rules |
| -------------- | ---------------------- | ---------------------- |
| Identity       | UC-001, UC-002, UC-003 | BR-001 – BR-013        |
| Learning       | UC-004                 | BR-014 – BR-017        |
| Community      | UC-006                 | BR-018 – BR-020        |
| Network        | UC-007                 | BR-021 – BR-025        |
| Collaboration  | UC-009                 | BR-026 – BR-028        |
| Communication  | UC-008                 | BR-025                 |
| Reputation     | Community & Learning   | BR-029 – BR-031        |
| AI             | UC-005                 | BR-032 – BR-034        |
| Administration | UC-002, UC-010         | BR-006 – BR-039        |

---

# Related Documents

- Business_Rules.md
- Use_Cases.md
- Non_Functional_Requirements.md
