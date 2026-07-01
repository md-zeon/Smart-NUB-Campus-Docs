---
title: DD-008 - Manual Verification Before AI Verification
id: DD-008
status: Accepted
date: 2026-07-01
authors:
  - Zeanur Rahaman Zeon
reviewed_by:
  - Team
---

# Context

Smart NUB Campus requires every user to be a verified Northern University Bangladesh (NUB) student before accessing the platform.

Several approaches to identity verification were considered, including:

- Manual administrator verification
- Optical Character Recognition (OCR)
- AI-assisted document verification
- Fully automated verification

While automation has the potential to reduce administrative effort, implementing a reliable verification pipeline requires high-quality document recognition, fraud detection, and extensive testing.

Incorrect verification could compromise the trust and integrity of the platform.

---

# Decision

Version 1 of Smart NUB Campus shall use **manual administrator verification** as the primary verification process.

Students must:

- Register an account.
- Provide their student ID.
- Upload an image of their official university ID card.
- Wait for administrator approval.

The system architecture shall remain extensible so that OCR or AI-assisted verification can be integrated in future versions without redesigning the verification workflow.

---

# Rationale

Manual verification provides the highest confidence during the initial release.

Benefits include:

- Greater verification accuracy.
- Reduced risk of fraudulent accounts.
- Easier handling of exceptional cases.
- Simpler implementation.
- Opportunity to collect verification data for future AI improvements.

By designing the verification workflow to be modular, the platform can evolve from manual verification to AI-assisted verification over time.

---

# Consequences

## Positive

- High confidence in verified identities.
- Simpler implementation.
- Easier moderation.
- Lower risk of false approvals.
- Creates a reliable dataset for future automation.

## Negative

- Verification depends on administrator availability.
- New users may experience approval delays.
- Increased administrative workload as the platform grows.

---

# Future Evolution

Future versions may introduce:

- OCR-based data extraction.
- AI-assisted document validation.
- Duplicate document detection.
- Face-to-ID comparison (subject to university policy and privacy considerations).
- Automatic verification confidence scoring.

Any automated verification process should assist administrators rather than completely replacing human review unless proven sufficiently accurate.

---

# Alternatives Considered

## Fully Automated Verification

Automatically approve students using OCR and AI.

**Rejected because:**

- Higher risk of incorrect approvals.
- Requires extensive training and testing.
- Difficult to handle edge cases.

---

## OCR Only

Extract information using OCR while automatically approving registrations.

**Rejected because:**

- OCR cannot independently verify document authenticity.
- Recognition errors could lead to incorrect approvals.

---

# Affected Components

- Identity Module
- Registration
- Verification Workflow
- Administration
- Future AI Integration

---

# Related Decisions

- DD-001 — Verified Students Only
- DD-007 — Student ID Parsing
- DD-010 — AI as a Learning Assistant

---

# References

- Verification_and_Identity.md
- Functional_Requirements.md
- Business_Rules.md
