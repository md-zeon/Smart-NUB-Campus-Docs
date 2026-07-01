---
title: Verification and Identity
version: 1.0
status: Draft
last_updated: 2026-07-01
---

# Verification and Identity

## Overview

Smart NUB Campus (SNC) is built on trust. Every member of the platform must be a verified student of Northern University Bangladesh (NUB).

This document defines the identity model, student verification process, student ID structure, and the rules governing access to the platform.

Verification ensures that academic collaboration takes place in a trusted environment where every participant represents a real NUB student.

---

# Objectives

The identity system aims to:

- Ensure that only verified NUB students can access the platform.
- Prevent fake or duplicate accounts.
- Build trust between students.
- Simplify profile creation using student information.
- Maintain the integrity of the academic community.

---

# Identity Model

Smart NUB Campus separates authentication, authorization, and verification into three independent concepts.

| Concept        | Purpose                                               |
| -------------- | ----------------------------------------------------- |
| Authentication | Confirms who the user is.                             |
| Authorization  | Determines what the user is allowed to do.            |
| Verification   | Confirms whether the user is an eligible NUB student. |

Only students with an **Approved** verification status are granted access to the platform.

---

# Verification Status

Each student account has one verification status.

| Status    | Description                                                              |
| --------- | ------------------------------------------------------------------------ |
| Pending   | Verification request has been submitted and is awaiting review.          |
| Approved  | Student identity has been verified and access is granted.                |
| Rejected  | Verification request was rejected. The student may submit a new request. |
| Suspended | Student access has been temporarily disabled by an administrator.        |

---

# Registration Requirements

During registration, a student must provide:

- Full Name
- Student ID
- Student ID Card Image
- Email Address
- Password

Additional profile information may be completed after verification.

---

# Student ID Structure

Every student is identified by an official Northern University Bangladesh student ID.

Example:

```text
41230301652
```

Structure:

```text
41 | 230 | 30 | 1652
│    │     │     │
│    │     │     └── Unique Student Number
│    │     └──────── Admission Intake
│    └────────────── Admission Year
└─────────────────── Department Code
```

---

# Department Codes

| Code | Department             |
| ---- | ---------------------- |
| 30   | BTX                    |
| 33   | EBTX                   |
| 41   | CSE                    |
| 42   | ECSE                   |
| 43   | EEE                    |
| 44   | EEEE                   |
| 45   | BBA                    |
| 47   | English                |
| 49   | Bangla                 |
| 51   | LLB                    |
| 55   | BPh                    |
| 58   | Mechanical Engineering |
| 59   | Civil Engineering      |

---

# Admission Intake Codes

| Code | Intake |
| ---- | ------ |
| 10   | Spring |
| 20   | Summer |
| 30   | Fall   |

---

# Registration Workflow

```text
Guest
    │
    ▼
Complete Registration Form
    │
    ▼
Upload Student ID Card
    │
    ▼
Submit Verification Request
    │
    ▼
Pending Review
    │
    ▼
Administrator Review
    │
 ┌──┴────────────┐
 │               │
 ▼               ▼
Approved     Rejected
 │               │
 ▼               ▼
Student     Resubmit Verification
```

---

# Verification Process

An administrator reviews each submitted verification request.

The administrator verifies:

- Student ID
- Student name
- Student ID card image
- Overall authenticity of the submission

If the information is valid, the request is approved.

Otherwise, it is rejected with a reason.

---

# Student Profile

After approval, the platform creates the student's academic profile.

## University Information

- Student ID
- Full Name
- Department
- Admission Year
- Admission Intake
- Verification Status

## Personal Information

- Profile Photo
- Bio
- Skills
- Academic Interests
- Project Interests

## Professional Links

- GitHub
- LinkedIn
- Portfolio Website

---

# Identity Rules

- Every account must represent one real NUB student.
- One student ID may be associated with only one account.
- Student ID information must remain immutable after verification.
- Department and admission information are derived from the student ID.
- Only approved students may access academic features.
- Suspended accounts lose access until reinstated.

---

# Future Enhancements

Future versions of Smart NUB Campus may include:

- OCR-assisted student ID extraction.
- Automatic student ID validation.
- AI-assisted verification support.
- Integration with official university identity systems (if available).

---

# Design Decisions

## DD-001

Authentication, authorization, and verification are independent concepts.

## DD-002

Every platform member must be a verified NUB student.

## DD-003

Each student ID can be associated with only one account.

## DD-004

Department and admission information are derived from the student ID.

## DD-005

Student ID information becomes immutable after successful verification.

---

# Assumptions

The student ID structure documented in this file is based on verified samples collected from Northern University Bangladesh student IDs.

If the university officially changes the student ID format in the future, the parsing and validation rules should be updated accordingly.

---

# Related Documents

- User_Roles.md
- Business_Rules.md
- Functional_Requirements.md
- Student_Identity.md (System Design)
