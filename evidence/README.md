# evidence

## Purpose

Holds **evidence records**: metadata describing the source files that PPC
recommendations rely on (`CLAUDE.md` Section 8).

The source files themselves — Amazon exports, source evidence files — are
**not** stored here. They are stored outside this repository, in the location,
under the access roles and for the retention period approved in
[`decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md`](../decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md).
This README does not restate those details; read the decision.

This repository is public (`CLAUDE.md` Section 9). SD-4 remains in force
(`CLAUDE.md` Section 10).

## What belongs here

- One Markdown file per evidence file, named
  `EVIDENCE_<YYYY-MM-DD>_<TOPIC>.md` in upper case with underscores, where the
  date is the export date.
- The template: `TEMPLATE_EVIDENCE_RECORD.md`.
- Each record states: source, report name, export date, date range, who
  exported it, and a storage reference (platform and folder path plus file name
  only).

## What does NOT belong here

- Amazon exports or any copy, extract, screenshot or paste of their contents.
- Spend, sales, bid, budget or other figures from any export.
- Sanitized, aggregated or otherwise derived commercial data (not permitted
  without a separate approved decision).
- Customer personal data (`CLAUDE.md` Section 10).
- Share links, access tokens, credentials or any URL that grants access
  (`CLAUDE.md` Section 9).
- Recommendations, decisions, change records or reports.

## Owner

Repository Owner — Sarujan
([`decisions/DECISION_REPOSITORY_OWNER.md`](../decisions/DECISION_REPOSITORY_OWNER.md)).
Maintained by the Coordinator (Sarujan; baseline Section 5). What this
means is defined in the root [`README.md`](../README.md) (Owner).

## Status

Created 2026-09-25 under the approved
`decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md` (Group 3) and
`decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md`. Pending review.
No evidence records exist yet.
