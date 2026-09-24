# TEMPLATE — Decision Record

Copy this file to `decisions/DECISION_<TOPIC>.md` and fill in every field.
Where a value is unknown, write `[VERIFY]`. Never guess.

This template is not a decision. It authorises nothing.

---

## Document Metadata

| Field | Value |
|-------|-------|
| Decision ID | `DECISION_<TOPIC>` |
| Title | |
| Status | PROPOSED / PENDING APPROVAL · APPROVED · REJECTED · SUPERSEDED |
| Date proposed | YYYY-MM-DD |
| Proposed by | |
| Approver | Name and role, or `[VERIFY]` |
| Date approved | YYYY-MM-DD, or `—` if not approved |
| Supersedes | Record or baseline section replaced, or `None` |
| Superseded by | Record that replaces this one, or `—` |

### Status definitions

| Status | Meaning |
|--------|---------|
| PROPOSED / PENDING APPROVAL | Written for review. Authorises nothing. |
| APPROVED | The named approver approved it on the stated date. In force. |
| REJECTED | The approver declined it. Kept for the record. Authorises nothing. |
| SUPERSEDED | Replaced by a later approved record, linked above. No longer in force. |

---

## 1. Decision

State the decision in one or two plain sentences.

## 2. Context

Why the decision is needed. Link the files it relates to.

## 3. Scope

- **Covers:**
- **Does not cover:**

## 4. Baseline impact

- Baseline sections affected (`phase-0/PHASE_0_BASELINE.md`): list them, or
  `None`.
- If a baseline value is replaced: the section, the old value, the new value.
- Safety defaults affected (`CLAUDE.md` SD-1 to SD-4): list them, or `None`.

## 5. Evidence

| Source | Report / document | Date exported | Date range | Location |
|--------|-------------------|---------------|------------|----------|
| | | | | |

If no evidence is filed, write: `None filed — EVIDENCE-PENDING`.

## 6. Open `[VERIFY]` items

List every question this decision leaves open. Do not answer them here unless
the approver has answered them.

## 7. Safety statement

Where the decision involves bids, budgets, keywords, campaigns or targeting:

- Outputs DRAFT recommendations only.
- Never applies Amazon Ads changes.
- Human approval required.

## 8. Actions authorised

List exactly what this decision authorises once APPROVED (for example, which
files a separate task may create). Write `None` if it authorises nothing.

## 9. Approval

| Field | Value |
|-------|-------|
| Approver | |
| Date | |
| How approval was given | For example: written confirmation in the task of YYYY-MM-DD |
