# reports

## Purpose

Holds **report templates** and **sent-log metadata** for LEDSone Amazon PPC
reports.

Filled-in reports — anything containing figures — are **not** stored here. They
are stored outside this repository, in the location, under the access roles and
for the retention period approved in
[`decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md`](../decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md).
This README does not restate those details; read the decision.

This repository is public (`CLAUDE.md` Section 9). SD-4 remains in force
(`CLAUDE.md` Section 10).

## Structure

| Path | Contents |
|------|----------|
| [`weekly/`](weekly/) | The weekly report template and weekly sent-log records |

## What belongs here

- Report templates: headings and placeholders only.
- Sent-log records: one Markdown file per report sent, stating only the date
  sent, recipient role, channel and storage reference of the filled-in report.
- A `README.md` in each sub-folder.

## What does NOT belong here

- Filled-in reports, drafts containing figures, or extracts of either.
- Spend, sales, ACoS, ROAS, bid, budget or other performance figures.
- Sanitized or aggregated commercial data (not permitted without a separate
  approved decision).
- Amazon exports — evidence records go in `evidence/`.
- Customer personal data, share links, access tokens or credentials
  (`CLAUDE.md` Sections 9 and 10).

The AIOS may **draft** a report; a human reviews and sends it. The AIOS never
sends email (`CLAUDE.md` Section 3.8).

## Owner

Repository Owner — Sarujan
([`decisions/DECISION_REPOSITORY_OWNER.md`](../decisions/DECISION_REPOSITORY_OWNER.md)).
Maintained by the Coordinator (Sarujan; baseline Section 5). What this
means is defined in the root [`README.md`](../README.md) (Owner).

## Status

Created 2026-09-25 under the approved
`decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md` (Group 3) and
`decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md`. Pending review.
