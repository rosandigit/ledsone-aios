# reports/weekly

## Purpose

Supports the weekly PPC report to the MD. The schedule, recipient and channel
are defined in `phase-0/PHASE_0_BASELINE.md` Section 3.5 and are not restated
here.

## What belongs here

- `TEMPLATE_WEEKLY_REPORT.md` — the structure of the weekly report, with
  placeholders only.
- Sent-log records, one per report sent, named `SENT_<YYYY-MM-DD>.md` where the
  date is the date sent. Each states only:
  - date sent;
  - recipient role;
  - channel;
  - storage reference of the filled-in report (platform and folder path plus
    file name, as approved in `decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md`).

## What does NOT belong here

- The filled-in weekly report, or any draft of it that contains figures. The
  filled-in report is stored in the approved location outside this repository.
- Figures of any kind, share links, access tokens or credentials.

## Process

1. The AIOS drafts the report from the template, using evidence recorded in
   `evidence/`.
2. A human reviews the draft.
3. The filled-in report is saved in the approved storage location.
4. A human sends it; the AIOS never sends email.
5. A sent-log record is added here.

## Owner

Repository Owner — `[VERIFY]` (`phase-0/PHASE_0_BASELINE.md`, Limitation L12).
Maintained by the Coordinator (Sarujan; baseline Section 5).

## Status

Created 2026-09-25 under the approved
`decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md` (Group 3) and
`decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md`. Pending review.
No sent-log records exist yet.
