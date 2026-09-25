# TEMPLATE — Change Record

Copy this file to `change-log/CHANGE_<YYYY-MM-DD>_<TOPIC>.md`, where the date
is the execution date of the change, and fill in every field. Where a value is
unknown, write `[VERIFY]`. Never guess.

This template is not a change record. It records nothing and authorises
nothing. Read `change-log/README.md` before filling it in, including the open
item on sensitive values.

---

## 1. Record Metadata

| Field | Value |
|-------|-------|
| Change ID | `CHANGE_<YYYY-MM-DD>_<TOPIC>` |
| Record type | Executed change · Rollback |
| Date executed | YYYY-MM-DD |
| Time executed | HH:MM and time zone |
| Executed by | Name of the human who made the change in Amazon |
| Recorded by | Name of the person or AIOS session that wrote this record |
| Date recorded | YYYY-MM-DD |

## 2. Approval Reference

| Field | Value |
|-------|-------|
| Approval basis | Approved decision · Routine approval under an existing approved rule or authority · Required approval not obtained |
| Approved decision | `decisions/DECISION_<TOPIC>.md`, or `—` if not applicable |
| Rule or authority relied on | For a routine approval: the existing approved rule or authority that permits the action; otherwise `—` |
| Approver | Name and role — as named in the decision, or of the person who gave the routine approval; `—` if not obtained |
| Date approved | YYYY-MM-DD, or `—` if not obtained |
| How approval was given | For a routine approval: how it was given; for a decision: `As recorded in that decision`; `—` if not obtained |
| Approval tier (budget changes) | Tier from `phase-0/PHASE_0_BASELINE.md` Section 3.1, or `Not a budget change` |
| Safety defaults relied on | `CLAUDE.md` SD-1 to SD-4, or `None` |

Formal decisions, policy changes, baseline changes and supersessions need an
approved decision in `decisions/`. A routine PPC action may instead rely on an
existing approved rule or authority, with the routine approval recorded above.

If the required approval was not obtained, set "Approval basis" to
`Required approval not obtained`, and treat the change as a governance
exception, escalated according to the applicable approved governance rules.
Never record the change as approved. See `change-log/README.md`.

## 3. What Was Changed

| Field | Value |
|-------|-------|
| Marketplace | |
| Campaign type | SP · SB · SD |
| Level | Campaign · Ad group · Keyword · Negative keyword · Target · Placement · Other |
| Item identifier | Name or ID as shown in Amazon |
| Change type | Bid · Budget · Keyword · Negative keyword · Targeting · Status · Other |

## 4. Old State and New State

| Field | Old state | New state |
|-------|-----------|-----------|
| Value / setting | | |

- Where the change is a bid, state whether it is within the maximum bid change
  in `phase-0/PHASE_0_BASELINE.md` Section 3.2 (and `CLAUDE.md` SD-1).
- Where the change is a budget, state the approval tier used.
- **Sensitive values:** whether exact bid or budget amounts may be committed to
  this public repository is `[VERIFY]` (`change-log/README.md`). Do not commit a
  record containing them until an approved decision allows it.

## 5. Evidence / Reference

| Source | Report / document | Date exported | Date range | Location |
|--------|-------------------|---------------|------------|----------|
| | | | | |

If no evidence is filed, write: `None filed — EVIDENCE-PENDING`. Never attach or
paste Amazon exports into this file (`CLAUDE.md` Section 10).

## 6. Result

| Field | Value |
|-------|-------|
| Outcome | Succeeded · Failed · Partially applied |
| Checked in Amazon by | Name |
| Date checked | YYYY-MM-DD |
| Notes | What was observed; any difference from the approved change |

## 7. Rollback Information

Rollbacks are manual in Amazon, using Change History (`CLAUDE.md` Section 8).

| Field | Value |
|-------|-------|
| How to roll back | Steps to restore the old state |
| Rolled back? | No · Yes |
| Date rolled back | YYYY-MM-DD, or `—` |
| Rolled back by | Name, or `—` |
| Reverted to | Value restored, or `—` |
| Reason for rollback | Or `—` |
| Rollback record | `change-log/CHANGE_<YYYY-MM-DD>_<TOPIC>.md`, or `—` |

## 8. Safety Statement

- Outputs DRAFT recommendations only.
- Never applies Amazon Ads changes.
- Human approval required.

The change recorded here was made manually by the named human, not by the AIOS.
