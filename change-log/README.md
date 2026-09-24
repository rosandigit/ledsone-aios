# change-log

## Purpose

Records **executed** changes and **rollbacks**: what a human actually changed
in Amazon, after approval.

This is stage 4 (Execution) of `CLAUDE.md` Section 6. It is kept separate from
stage 3 (Approval), which is recorded in `decisions/`. A change record states
what was done; the decision record it cites states that it was allowed.

The AIOS never executes changes in Amazon (`CLAUDE.md` Sections 1 and 5). Every
change recorded here was made manually by a named human.

## What belongs here

- One Markdown file per executed change or rollback, named
  `CHANGE_<YYYY-MM-DD>_<TOPIC>.md` in upper case with underscores.
- The template: `TEMPLATE_CHANGE_RECORD.md`.
- Each record must cite the approved decision it relies on, and state who
  executed the change, the old and new state, the evidence, the result and the
  rollback information (`CLAUDE.md` Section 8).

## What does NOT belong here

- Approvals or decisions — use `decisions/`.
- DRAFT recommendations, analysis or reports.
- Changes made without an approved decision. If one happens, record it and
  mark it `UNAPPROVED — escalate to MD` (`CLAUDE.md` Section 3.7); never
  record it as approved.
- Amazon exports, screenshots of exports, customer data or credentials
  (`CLAUDE.md` Sections 9 and 10).

## Sensitive values — open item

This repository is public. `CLAUDE.md` Section 8 requires the old and new value
of each change to be recorded, and SD-4 (`CLAUDE.md` Section 10) forbids
committing commercially sensitive data without an approved decision.

Whether exact bid and budget amounts may be committed here is **`[VERIFY]`**.
Until an approved decision in `decisions/` settles it, a record containing
exact bid or budget amounts must **not** be committed; stop and raise it
instead. This README does not resolve that item.

## Owner

Repository Owner — `[VERIFY]` (`phase-0/PHASE_0_BASELINE.md`, Limitation L12).
Maintained by the Coordinator (Sarujan; baseline Section 5).

## Status

Created 2026-09-24 under the approved
`decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md` (Group 1). Pending review.
No change records exist yet.
