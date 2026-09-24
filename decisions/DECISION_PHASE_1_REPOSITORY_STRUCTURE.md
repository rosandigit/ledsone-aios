# DECISION — Phase 1 Repository Structure

> **STATUS: APPROVED** — by Sarujan on 2026-09-24.
> This record approves a repository structure. It is **not** a business rule,
> and it does not itself create any file or folder: each item is still created
> only by a separate approved task (Section 9). Nothing listed as proposed below
> exists yet unless stated.

---

## Document Metadata

| Field | Value |
|-------|-------|
| Decision ID | `DECISION_PHASE_1_REPOSITORY_STRUCTURE` |
| Title | Phase 1 repository structure for `rosandigit/ledsone-aios` |
| Status | APPROVED |
| Date proposed | 2026-09-24 |
| Proposed by | AIOS, from the Phase 1 read-only repository inspection of 2026-09-24 |
| Approver | Sarujan |
| Date approved | 2026-09-24 |
| Supersedes | None |
| Superseded by | — |

---

## 1. Decision

Proposed: adopt the documentation-only folder structure in Section 5 as the
Phase 1 structure of `rosandigit/ledsone-aios`, to be created in stages by
separate approved tasks.

## 2. Context

- `phase-0/PHASE_0_BASELINE.md` (D1) makes `rosandigit/ledsone-aios` the PPC
  home.
- `CLAUDE.md` Section 13 requires documentation before building, a `README.md`
  in every folder, and no duplicate truth.
- The Phase 1 read-only inspection (2026-09-24, branch
  `claude/happy-fermi-04tnrh` at commit `9f8317b`) found only three files:
  `README.md`, `CLAUDE.md` and `phase-0/PHASE_0_BASELINE.md`. No configuration
  files and no other PPC assets existed.

## 3. Scope

- **Covers:** folder and file layout for documentation and repository
  configuration only.
- **Does not cover:** business values, PPC rules, skills, application code,
  Amazon API access, automation, evidence storage location, or merging to
  `main`.

## 4. Baseline impact

- Baseline sections affected: **None.** No baseline value is changed.
- Safety defaults affected: **None.** SD-4 (no Amazon exports or commercially
  sensitive data in this public repository) shapes the proposed `evidence/` and
  `reports/` folders but is not changed by this record.

## 5. Proposed structure

```
ledsone-aios/
├── README.md                    existing — change requires approval by name
├── CLAUDE.md                    existing — untouched
├── .gitattributes               proposed
├── .gitignore                   proposed
├── phase-0/
│   ├── README.md                proposed
│   └── PHASE_0_BASELINE.md      existing — untouched
├── decisions/
│   ├── README.md                existing, approved for this decision-record system
│   ├── TEMPLATE_DECISION_RECORD.md               existing, approved template
│   └── DECISION_PHASE_1_REPOSITORY_STRUCTURE.md  this approved record
├── change-log/
│   ├── README.md                proposed
│   └── TEMPLATE_CHANGE_RECORD.md proposed
├── evidence/
│   ├── README.md                proposed — needs storage decision first
│   └── TEMPLATE_EVIDENCE_RECORD.md proposed — needs storage decision first
└── reports/
    ├── README.md                proposed — needs storage decision first
    └── weekly/
        ├── README.md            proposed — needs storage decision first
        └── TEMPLATE_WEEKLY_REPORT.md proposed — needs storage decision first
```

For every proposed item:

- **Owner:** Repository Owner — `[VERIFY]` (baseline L12); maintained by the
  Coordinator (Sarujan; baseline Section 5).
- **Status:** PROPOSED — not created. The three `decisions/` files are the
  exception: they were created as part of the approved decision-record system
  and are currently uncommitted on the feature branch. Their existence does not
  mean any other proposed item is approved for creation (Section 9).

| Item | Purpose | Belongs there | Does not belong there |
|------|---------|---------------|-----------------------|
| `README.md` (change) | Repository front page | What the repository is; links to `CLAUDE.md`, the baseline and each folder | Rules, values, or restated `CLAUDE.md` content |
| `.gitattributes` | Enforce text files with LF line endings (`CLAUDE.md` Section 11) | End-of-line and text attributes | Anything else |
| `.gitignore` | Prevent accidental commits of exports and credentials (`CLAUDE.md` Section 9, SD-4) | Patterns such as `*.csv`, `*.xlsx`, `.env`, `*.key` | Rules that hide approved documentation |
| `phase-0/README.md` | Folder README required by `CLAUDE.md` Section 13 | Purpose of `phase-0/`; link to the baseline | Baseline values |
| `decisions/` | Approvals, rejections and supersessions | Decision records; the template | Executed changes, drafts, raw data |
| `change-log/` | Executed changes and rollbacks — stage 4 of `CLAUDE.md` Section 6, kept separate from approvals | Date, who executed, old and new value, link to the approving decision | Approvals, recommendations, credentials |
| `evidence/` | Evidence **records** only (metadata), because the repository is public (SD-4) | Source, report name, export date, date range, where the file is stored | Actual exports, spend or sales figures, customer data |
| `reports/`, `reports/weekly/` | Weekly report to the MD, Friday 4:00 PM (baseline 3.5) | A template; a record of sending (date, recipient) | Filled-in reports with figures, until a storage location is approved (SD-4) |

### Deliberately deferred (not part of this proposal)

Each needs its own design record and approval first:

- `context/` rule files — would restate the baseline (duplicate truth).
- `skills/`.
- `validation/` gap register — would duplicate baseline Section 8.
- `handover/`.
- `CODEOWNERS` — GitHub usernames are not recorded (`[VERIFY]`).
- Pull request template.
- Application code, Amazon API access and automation — not authorised
  (`CLAUDE.md` Sections 1 and 14).

## 6. Duplication and conflict risks noted

1. `CLAUDE.md` Section 3 restates baseline values. Any future baseline change
   must update `CLAUDE.md` Section 3 in the same task.
2. The former repository `rosandigit/ledsone-ppc-aios` uses similar folder
   names. Matching names is acceptable; copying content is not (baseline C1,
   C2).
3. A gap register would duplicate baseline Section 8 unless that section is
   formally superseded.
4. `CLAUDE.md` metadata still reads "Draft — pending review and approval"
   although it was approved. Correcting it requires approval naming
   `CLAUDE.md`.
5. `main` shows none of the governance files until the feature branch is
   merged, which requires explicit approval (`CLAUDE.md` Section 11).
6. `evidence/` and `reports/` conflict with SD-4 unless limited to templates and
   metadata until a storage location is approved.
7. A future `README.md` must link to, not restate, `CLAUDE.md` and the baseline.

## 7. Open `[VERIFY]` items

- Storage location for Amazon exports and filled-in reports (baseline L1; SD-4).
- GitHub usernames for any future `CODEOWNERS`.

## 8. Safety statement

This record changes no Amazon setting and involves no bids, budgets, keywords,
campaigns or targeting. Any later recommendation made within this structure:

- Outputs DRAFT recommendations only.
- Never applies Amazon Ads changes.
- Human approval required.

## 9. Actions authorised

This record is APPROVED, but it does not itself create or modify files. Each
proposed item still requires a separate explicit approved task before creation.

This approval permits separate explicitly approved tasks to create the proposed
items in stages, subject to the preconditions below:

| Group | Items | Precondition |
|-------|-------|--------------|
| 1 | `change-log/` (README, template), `phase-0/README.md`, `.gitattributes`, `.gitignore` | Approval of this record |
| 2 | Change to `README.md`; correction of `CLAUDE.md` metadata | Approval naming each file (`CLAUDE.md` Sections 11 and 15) |
| 3 | `evidence/`, `reports/` | An approved decision on where exports and filled-in reports are stored |

## 10. Approval

| Field | Value |
|-------|-------|
| Approver | Sarujan |
| Date | 2026-09-24 |
| How approval was given | Written approval in the current task on 2026-09-24 |
