# decisions

## Purpose

Holds decision records for the LEDSone Amazon PPC AIOS: approvals, rejections
and formal supersessions of earlier records.

This is the folder `CLAUDE.md` refers to when it requires "a decision record"
(Section 2 — formally superseding the Phase 0 baseline; Section 8 — recording
approvals; Section 14 — authorising any automation).

## What belongs here

- One Markdown file per decision, named `DECISION_<TOPIC>.md` in upper case with
  underscores (for example `DECISION_PHASE_1_REPOSITORY_STRUCTURE.md`).
- The decision template: `TEMPLATE_DECISION_RECORD.md`.
- Records at any status: PROPOSED / PENDING APPROVAL, APPROVED, REJECTED or
  SUPERSEDED (defined in the template).

## What does NOT belong here

- Executed changes or rollbacks in Amazon. Those are execution records, kept
  separate from approvals (`CLAUDE.md` Section 6), and belong in
  `change-log/`.
- DRAFT recommendations, analysis or reports.
- Amazon exports, performance data, customer data or commercially sensitive data
  (`CLAUDE.md` Section 10, SD-4).
- Credentials of any kind (`CLAUDE.md` Section 9).
- Business values stated without an approver and date.

## Rules

- A record is **not** in force until its status is APPROVED and it names the
  approver and the approval date.
- A PROPOSED / PENDING APPROVAL record authorises nothing.
- A record that changes a value in `phase-0/PHASE_0_BASELINE.md` must name the
  baseline section it replaces, state the new value, and record who approved it
  and when (`CLAUDE.md` Section 2). Until then, the baseline stands.
- A decision record does not create or change any other file by itself. Files
  are created or changed only by a separate task that cites the approved record.
- `[VERIFY]` items stay `[VERIFY]` until an approved record answers them. Never
  fill them by inference.
- Never edit an APPROVED record's decision. Record a new decision that
  supersedes it, and set the old record's status to SUPERSEDED with a link.

## Owner

Repository Owner — Sarujan
([`decisions/DECISION_REPOSITORY_OWNER.md`](DECISION_REPOSITORY_OWNER.md)).
Maintained by the Coordinator (Sarujan; baseline Section 5). What this
means is defined in the root [`README.md`](../README.md) (Owner).

## Status

Approved 2026-09-24: this folder and its decision-record system (this README
and `TEMPLATE_DECISION_RECORD.md`) were approved as part of the approved
`decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md`.
