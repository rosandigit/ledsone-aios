# change-log

## Purpose

Records **executed** changes and **rollbacks**: what a human actually changed
in Amazon, after approval.

This is stage 4 (Execution) of `CLAUDE.md` Section 6, kept separate from
stage 3 (Approval). A change record states what was done and references the
approval or authority that allowed it.

Where approvals are recorded (`CLAUDE.md` Section 8 permits "a decision or
change log"):

- Formal decisions, policy changes, baseline changes and supersessions are
  recorded in `decisions/`.
- A routine approval given under an existing approved rule or authority may be
  recorded in the change record itself. A separate decision record is not
  required for a routine PPC action that an existing approved rule or
  authority already permits.

The AIOS never executes changes in Amazon (`CLAUDE.md` Sections 1 and 5). Every
change recorded here was made manually by a named human.

## What belongs here

- One Markdown file per executed change or rollback, named
  `CHANGE_<YYYY-MM-DD>_<TOPIC>.md` in upper case with underscores, where the
  date is the execution date of the change.
- The template: `TEMPLATE_CHANGE_RECORD.md`.
- Each record must reference the applicable approval or authority — an
  approved decision in `decisions/`, or a routine approval recorded in the
  record under an existing approved rule or authority — and state who executed
  the change, the old and new state, the evidence, the result and the rollback
  information (`CLAUDE.md` Section 8).

## What does NOT belong here

- Formal decisions, policy changes, baseline changes or supersessions — use
  `decisions/`.
- DRAFT recommendations, analysis or reports.
- Amazon exports, screenshots of exports, customer data or credentials
  (`CLAUDE.md` Sections 9 and 10).

## Changes made without the required approval

Every executed change should have an applicable approval or authority. If a
change was made without the required approval, record it factually, state that
the required approval was not obtained, and treat it as a governance exception:
escalate it according to the applicable approved governance rules. Never record
it as approved. This README does not create any new approval or escalation
rule.

## Sensitive values — open item

This repository is public. `CLAUDE.md` Section 8 requires the old and new value
of each change to be recorded, and SD-4 (`CLAUDE.md` Section 10) forbids
committing commercially sensitive data without an approved decision.

Whether exact bid and budget amounts may be committed here is **`[VERIFY]`**.
Until an approved decision in `decisions/` settles it, a record containing
exact bid or budget amounts must **not** be committed; stop and raise it
instead. This README does not resolve that item.

## Owner

Repository Owner — Sarujan
([`decisions/DECISION_REPOSITORY_OWNER.md`](../decisions/DECISION_REPOSITORY_OWNER.md)).
Maintained by the Coordinator (Sarujan; baseline Section 5). What this
means is defined in the root [`README.md`](../README.md) (Owner).

## Status

Created 2026-09-24 under the approved
`decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md` (Group 1). Pending review.
No change records exist yet.
