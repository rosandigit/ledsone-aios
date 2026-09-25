# DECISION — Evidence and Report Storage

> **STATUS: PROPOSED / PENDING APPROVAL.**
> This record is written for review. It is **not** approved, it is **not** a
> business rule, and it authorises **nothing**. No folder, file or storage
> location is created, chosen or permitted by it while it is PROPOSED.

---

## Document Metadata

| Field | Value |
|-------|-------|
| Decision ID | `DECISION_EVIDENCE_AND_REPORT_STORAGE` |
| Title | Storage of Amazon exports, source evidence files and filled-in PPC reports |
| Status | PROPOSED / PENDING APPROVAL |
| Date proposed | 2026-09-24 |
| Proposed by | AIOS, drafted on the direction given in the task of 2026-09-24 |
| Approver | Sarujan |
| Date approved | — |
| Supersedes | None |
| Superseded by | — |

---

## 1. Decision

Proposed: Amazon exports, source evidence files and filled-in PPC reports are
stored in restricted company file storage, **not** in the public repository
`rosandigit/ledsone-aios`. This repository holds only metadata and reference
records about those files, and report templates with sent-log metadata.

In detail, if approved:

1. **Not in this repository.** Amazon exports, source evidence files and
   filled-in PPC reports must never be committed to `rosandigit/ledsone-aios`.
2. **Where the files live.** Actual files are stored in restricted company file
   storage: `Company Google Drive`, folder
   `Amazon PPC AIOS / Evidence & Reports`.
3. **Access.** Access to that storage is limited to: `MD + PPC Team Leader`.
4. **Retention.** Files are kept for: `1 year`.
5. **No links, tokens or credentials.** Share links, access tokens and
   credentials must never be committed to GitHub. A storage reference in this
   repository names the location by platform and folder path only.
6. **`evidence/`** will contain metadata and reference records only — for
   example source, report name, export date, date range, who exported it and
   the storage reference. It will contain no file contents and no figures.
7. **`reports/`** will contain report templates and sent-log metadata only —
   for example date sent, recipient role, channel and storage reference. It will
   contain no filled-in reports and no figures.
8. **No sanitized or aggregated data.** No sanitized, aggregated or otherwise
   derived commercial data may be committed unless a separate approved decision
   defines the sanitization rules.
9. **SD-4 remains in force** (`CLAUDE.md` Section 10). This record does not
   relax it and does not permit committing any Amazon export or commercially
   sensitive data.

## 2. Context

- `rosandigit/ledsone-aios` is a public GitHub repository (`CLAUDE.md`
  Section 9). Anything committed and pushed must be assumed visible to anyone,
  and remains in git history even if later deleted.
- `CLAUDE.md` Section 8 requires evidence to be cited with source, report name,
  date exported and date range, and states that the structure and location of
  evidence must be approved before evidence is filed.
- SD-4 (`CLAUDE.md` Section 10) forbids committing Amazon exports or
  commercially sensitive data without an approved decision stating where they
  may be stored.
- `phase-0/PHASE_0_BASELINE.md` records that no source evidence is filed
  (Limitation L1) and that a weekly report goes to the MD (Section 3.5). Both
  need a storage location outside this repository.
- `decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md` (APPROVED) makes
  Group 3 (`evidence/`, `reports/`) conditional on "an approved decision on where
  exports and filled-in reports are stored" (Section 9), and lists that storage
  location as an open `[VERIFY]` item (Section 7). This record is proposed to
  answer that precondition.

## 3. Scope

- **Covers:**
  - where Amazon exports, source evidence files and filled-in PPC reports are
    stored;
  - what `evidence/` and `reports/` may and may not contain;
  - how storage locations may be referenced from this repository.
- **Does not cover:**
  - whether exact bid and budget amounts may appear in change records
    (`change-log/README.md`, open `[VERIFY]`), which remains unresolved;
  - sanitization rules for derived data;
  - making the repository private, merging to `main`, or any Amazon connection,
    API work, automation or application code;
  - creating any file or folder.

## 4. Baseline impact

- Baseline sections affected (`phase-0/PHASE_0_BASELINE.md`): **None.** No
  baseline value is replaced. The record relates to Limitation L1 (evidence to
  be filed) and Section 3.5 (weekly report) without changing either.
- Safety defaults affected (`CLAUDE.md` SD-1 to SD-4): **None changed.** SD-4
  remains in force and is not relaxed.

## 5. Evidence

| Source | Report / document | Date exported | Date range | Location |
|--------|-------------------|---------------|------------|----------|
| — | — | — | — | — |

None filed — EVIDENCE-PENDING. The proposed direction comes from the written
instruction in the task of 2026-09-24. The repository's public visibility is
recorded in `CLAUDE.md` Section 9.

## 6. Open `[VERIFY]` items

- Whether exact bid and budget amounts in change records must also be kept in
  the restricted storage (`change-log/README.md`) — outside this record's scope
  unless added on approval.

## 7. Safety statement

This record changes no Amazon setting and involves no bids, budgets, keywords,
campaigns or targeting. Any later recommendation that relies on evidence stored
under this record:

- Outputs DRAFT recommendations only.
- Never applies Amazon Ads changes.
- Human approval required.

## 8. Actions authorised

**None while PROPOSED / PENDING APPROVAL.**

After this record is APPROVED, a separate explicitly approved task may create the
Group 3 documentation files for `evidence/` and `reports/` listed in
`decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md` (Section 5). Those files are
documentation only: metadata and reference records, templates and sent-log
metadata.

Even after approval:

- actual Amazon exports, source evidence files and completed reports remain
  outside the public repository, in the restricted company file storage;
- no share link, access token or credential may be committed;
- no sanitized or aggregated commercial data may be committed without a
  separate approved decision;
- any change to an existing file (`CLAUDE.md`, `README.md`,
  `decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md`) still requires approval
  naming that file.

## 9. Approval

| Field | Value |
|-------|-------|
| Approver | Sarujan |
| Date | — |
| How approval was given | — |
