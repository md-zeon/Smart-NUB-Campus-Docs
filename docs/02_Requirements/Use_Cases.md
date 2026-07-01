---
title: Use Cases
version: 1.0
status: Draft
last_updated: 2026-07-01
---

# Use Cases

## Overview

This document describes how different users interact with Smart NUB Campus (SNC) to accomplish specific goals.

Each use case outlines the primary actor, prerequisites, normal flow, alternative flows, and expected outcome.

---

# UC-001 — Register Account

## Primary Actor

Guest

## Goal

Create a new Smart NUB Campus account.

## Preconditions

- User is not logged in.
- User is a Northern University Bangladesh student.

## Main Flow

1. User opens the registration page.
2. User enters required information.
3. User uploads their student ID card.
4. User submits the registration form.
5. System validates the submitted information.
6. System creates an account with **Pending** verification status.
7. User receives confirmation.

## Alternative Flow

- Student ID format is invalid.
- Email is already registered.
- Student ID is already associated with another account.
- Required fields are missing.

## Postconditions

The account exists with **Pending** verification status.

---

# UC-002 — Verify Student

## Primary Actor

Administrator

## Goal

Verify a student's identity.

## Preconditions

- Registration request exists.
- Status is Pending.

## Main Flow

1. Administrator reviews the request.
2. Administrator checks submitted information.
3. Administrator reviews the uploaded student ID.
4. Administrator approves or rejects the request.
5. System updates verification status.
6. Student receives a notification.

## Alternative Flow

- Administrator requests resubmission.
- Administrator rejects the request.

## Postconditions

Verification status becomes Approved or Rejected.

---

# UC-003 — Complete Profile

## Primary Actor

Student

## Goal

Complete academic profile information.

## Preconditions

- Verification status is Approved.

## Main Flow

1. Student opens profile settings.
2. Student uploads profile picture.
3. Student enters bio.
4. Student adds skills.
5. Student adds academic interests.
6. Student saves profile.

## Postconditions

Profile becomes visible to other students.

---

# UC-004 — Share Academic Resource

## Primary Actor

Student

## Goal

Share learning resources.

## Preconditions

- Student is verified.

## Main Flow

1. Student selects "Upload Resource".
2. Student enters title.
3. Student selects resource category.
4. Student uploads the resource.
5. Student submits.
6. System stores the resource.
7. Resource becomes searchable.

---

# UC-005 — Ask AI Assistant

## Primary Actor

Student

## Goal

Receive AI-powered academic assistance.

## Preconditions

- Student is logged in.

## Main Flow

1. Student opens AI Assistant.
2. Student enters a question.
3. AI processes the request.
4. AI returns a response.

---

# UC-006 — Ask Academic Question

## Primary Actor

Student

## Goal

Receive help from other students.

## Main Flow

1. Student creates a question.
2. Student selects a category.
3. Question is published.
4. Other students answer.
5. Student marks the best answer.

---

# UC-007 — Send Connection Request

## Primary Actor

Student

## Goal

Connect with another verified student.

## Preconditions

- Both students are verified.
- No existing connection exists.

## Main Flow

1. Student visits another student's profile.
2. Student clicks Connect.
3. Student writes an optional note.
4. Request is sent.
5. Recipient accepts or declines.

## Postconditions

If accepted, both students become connections.

---

# UC-008 — Send Private Message

## Primary Actor

Student

## Goal

Communicate privately.

## Preconditions

- Connection request has been accepted.

## Main Flow

1. Student opens chat.
2. Student types a message.
3. Message is sent.
4. Recipient receives the message in real time.

---

# UC-009 — Create Collaboration Team

## Primary Actor

Student

## Goal

Recruit teammates.

## Main Flow

1. Student creates a team.
2. Student describes the project.
3. Student specifies required skills.
4. Team is published.
5. Other students apply.
6. Team owner accepts members.

---

# UC-010 — Moderate Platform

## Primary Actor

Administrator

## Goal

Maintain platform quality.

## Main Flow

1. Administrator reviews reports.
2. Administrator investigates.
3. Administrator takes appropriate action.
4. System records the action.

---

# Related Documents

- User_Stories.md
- Business_Rules.md
- Functional_Requirements.md
