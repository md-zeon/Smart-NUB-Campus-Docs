---
title: DD-007 - Student ID Parsing
id: DD-007
status: Accepted
date: 2026-07-01
authors:
  - Zeanur Rahaman Zeon
reviewed_by:
  - Team
---

# Context

Every Northern University Bangladesh (NUB) student is assigned a student ID that follows a structured format.

Information collected from the Northern University Bangladesh Admission Office, together with analysis of multiple student IDs, confirms that the student ID follows a structured format containing encoded academic information.

Examples:

- 41230301652
- 42230200943
- 45250200976
- 51240304123

The encoded information includes:

- Department
- Admission Year
- Admission Intake
- Student Sequence Number

Since this information already exists within the student ID, asking students to enter it manually would introduce unnecessary duplication and increase the risk of incorrect data.

---

# Decision

Smart NUB Campus shall treat the student ID as the authoritative source of academic identity.

During registration, the system shall automatically extract:

- Department
- Admission Year
- Admission Intake

These values shall populate the student's verified academic profile and shall not be editable by the student after verification.

---

# Student ID Structure

The student ID follows the format:

XXYYYZZNNNN

Where:

- XX = Department Code
- YYY = Admission Year
- ZZ = Admission Intake
- NNNN = Student Sequence Number

Example:

41 230 30 1652

Parses to:

Department:
Computer Science & Engineering (CSE)

Admission Year:
2023

Admission Intake:
Fall

Student Number:
1652

---

# Known Department Codes

| Code | Department |
| ---- | ---------- |
| 30   | BTX        |
| 33   | EBTX       |
| 41   | CSE        |
| 42   | ECSE       |
| 43   | EEE        |
| 44   | EEEE       |
| 45   | BBA        |
| 46   | MBA        |
| 47   | English    |
| 48   | MAE        |
| 49   | Bangla     |
| 50   | MAB        |
| 51   | LLB        |
| 53   | MPh        |
| 55   | BPh        |
| 58   | ME         |
| 59   | Civil      |

The department codes documented below have been confirmed through information provided by the Northern University Bangladesh Admission Office.

If the university introduces new academic programs in the future, this mapping should be updated accordingly.

---

# Known Intake Codes

| Code | Intake |
| ---- | ------ |
| 10   | Spring |
| 20   | Summer |
| 30   | Fall   |

The intake codes documented below have been verified through information obtained from the Northern University Bangladesh Admission Office.

---

# Rationale

Automatically deriving academic information from the student ID:

- Eliminates duplicate data entry.
- Reduces user errors.
- Standardizes academic profiles.
- Improves verification accuracy.
- Simplifies registration.

The student ID becomes the single source of truth for verified academic identity.

---

# Consequences

## Positive

- Faster registration.
- Consistent academic profiles.
- Reduced manual input.
- Improved data quality.
- Simplified verification.

## Negative

- Future changes to the university's ID format may require updates.
- Unknown department or intake codes must be handled gracefully.

---

# Alternatives Considered

## Manual Academic Information Entry

Allow students to manually enter department, year, and intake.

**Rejected because:**

- Increases user effort.
- Higher chance of incorrect information.
- Makes verification more difficult.

---

# Affected Components

- Identity Module
- Registration
- Verification
- Student Profiles
- Database Design
- Authentication

---

# Related Decisions

- DD-001 — Verified Students Only
- DD-008 — Manual Verification Before AI Verification

---

# References

- Verification_and_Identity.md
- Business_Rules.md
- Functional_Requirements.md
