---
title: Business Rules
version: 1.0
status: Draft
last_updated: 2026-07-01
---

# Business Rules

## Overview

This document defines the business rules that govern the behavior of Smart NUB Campus (SNC).

Business rules represent the policies, constraints, and decisions that the platform must enforce regardless of implementation details. They ensure consistency, maintain platform integrity, and establish a trusted academic environment.

---

# Identity

### BR-001

Every Smart NUB Campus account must represent one real Northern University Bangladesh student.

---

### BR-002

Each student ID can be associated with only one account.

---

### BR-003

Student identity must be verified before accessing any academic features.

---

### BR-004

Department, admission year, and admission intake shall be derived from the student ID and must not be entered manually.

---

### BR-005

Student ID information becomes immutable after successful verification unless modified by an administrator.

---

# Verification

### BR-006

Every newly registered account begins with the **Pending** verification status.

---

### BR-007

Only administrators may approve or reject verification requests.

---

### BR-008

Only students with **Approved** verification status may access Smart NUB Campus.

---

### BR-009

Rejected students may submit another verification request.

---

### BR-010

Suspended accounts cannot access protected platform features.

---

# Profiles

### BR-011

Students are responsible for maintaining accurate profile information.

---

### BR-012

Students may update personal profile information but may not modify verified identity information.

---

### BR-013

Every profile must clearly display verified academic information.

---

# Learning

### BR-014

Only verified students may upload academic resources.

---

### BR-015

Every uploaded resource must belong to an academic category.

---

### BR-016

Students remain responsible for the accuracy and legality of uploaded resources.

---

### BR-017

Resources that violate university policies or copyright laws may be removed by administrators.

---

# Community

### BR-018

Questions, discussions, and posts must be academic or university-related.

---

### BR-019

Students may report inappropriate content.

---

### BR-020

Administrators may remove content that violates platform policies.

---

# Network

### BR-021

Only verified students may send connection requests.

---

### BR-022

Students cannot send connection requests to themselves.

---

### BR-023

Duplicate connection requests are not permitted.

---

### BR-024

A connection request may include an optional introductory note.

---

### BR-025

Private messaging is available only between accepted connections.

---

# Collaboration

### BR-026

Only verified students may create collaboration teams.

---

### BR-027

Team creators manage membership requests.

---

### BR-028

Students may join teams only after being accepted by the team creator.

---

# Reputation

### BR-029

Students earn reputation through positive academic contributions.

---

### BR-030

Reputation points cannot be transferred between accounts.

---

### BR-031

Badges are awarded according to predefined achievement criteria.

---

# AI Assistant

### BR-032

The AI Assistant is intended to support learning and academic productivity.

---

### BR-033

AI-generated responses should be considered guidance and may require independent verification.

---

### BR-034

Students remain responsible for the academic work they submit.

---

# Security

### BR-035

Users are responsible for protecting their account credentials.

---

### BR-036

The platform shall record important administrative actions for auditing purposes.

---

### BR-037

Student personal information shall be accessible only according to platform permissions.

---

# Platform Governance

### BR-038

Platform administrators are responsible for maintaining a respectful and academically focused environment.

---

### BR-039

Platform rules may evolve over time as the university community grows.

---

# Rule Traceability

| Rule Category       | Rule IDs        |
| ------------------- | --------------- |
| Identity            | BR-001 – BR-005 |
| Verification        | BR-006 – BR-010 |
| Profiles            | BR-011 – BR-013 |
| Learning            | BR-014 – BR-017 |
| Community           | BR-018 – BR-020 |
| Network             | BR-021 – BR-025 |
| Collaboration       | BR-026 – BR-028 |
| Reputation          | BR-029 – BR-031 |
| AI Assistant        | BR-032 – BR-034 |
| Security            | BR-035 – BR-037 |
| Platform Governance | BR-038 – BR-039 |

---

# Related Documents

- Verification_and_Identity.md
- User_Roles.md
- Use_Cases.md
- Functional_Requirements.md
