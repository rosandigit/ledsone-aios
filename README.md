# ledsone-aios

Documentation home of the LEDSone Amazon PPC AIOS — the approved PPC home under
Phase 0 decision D1 ([`phase-0/PHASE_0_BASELINE.md`](phase-0/PHASE_0_BASELINE.md),
Section 2).

This repository holds documentation, decision records and change records only.
It contains no application code and has no connection to Amazon. What the AIOS
may and may not do is defined in [`CLAUDE.md`](CLAUDE.md), not here.

## Start here

1. [`CLAUDE.md`](CLAUDE.md) — operating and safety instructions. Read it in full
   before doing any work in this repository.
2. [`phase-0/PHASE_0_BASELINE.md`](phase-0/PHASE_0_BASELINE.md) — the
   Owner-confirmed Phase 0 baseline; the source of truth for business values.
3. [`decisions/`](decisions/) — decision records, including the approved
   [`DECISION_PHASE_1_REPOSITORY_STRUCTURE.md`](decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md).

## Repository structure

| Path | Contents |
|------|----------|
| [`CLAUDE.md`](CLAUDE.md) | Operating and safety instructions for any AI or person working here |
| [`phase-0/`](phase-0/) | The Phase 0 baseline and its folder README |
| [`decisions/`](decisions/) | Decision records (approvals, rejections, supersessions) and the decision template |
| [`change-log/`](change-log/) | Records of executed changes and rollbacks, and the change-record template |
| [`evidence/`](evidence/) | Evidence records (metadata only): [`README.md`](evidence/README.md), [`TEMPLATE_EVIDENCE_RECORD.md`](evidence/TEMPLATE_EVIDENCE_RECORD.md). The evidence files themselves are stored outside this repository, as approved in [`decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md`](decisions/DECISION_EVIDENCE_AND_REPORT_STORAGE.md) |
| [`reports/`](reports/) | Report templates and sent-log records: [`README.md`](reports/README.md). Filled-in reports are stored outside this repository, as approved in the same decision |
| [`reports/weekly/`](reports/weekly/) | Weekly report to the MD: [`README.md`](reports/weekly/README.md), [`TEMPLATE_WEEKLY_REPORT.md`](reports/weekly/TEMPLATE_WEEKLY_REPORT.md) |
| `.gitattributes` | Text and line-ending settings |
| `.gitignore` | Guardrail against committing credentials, exports and sensitive files |

Each folder has its own `README.md` stating what belongs there and what does
not.

All folders in the approved Phase 1 structure
([`decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md`](decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md))
now exist. Folders the record defers, such as `context/` and `skills/`, are
created only after a separate approved decision and task.

## Rules and values

This README states no business rule, value or approval. Business values live in
[`phase-0/PHASE_0_BASELINE.md`](phase-0/PHASE_0_BASELINE.md); operating and
safety rules live in [`CLAUDE.md`](CLAUDE.md). If this README appears to
disagree with either, they win.

## Owner

Repository Owner — `[VERIFY]` (baseline, Limitation L12).
Maintained by the Coordinator (Sarujan; baseline Section 5).

## Status

Active — Phase 1 in progress.
