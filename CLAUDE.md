# CLAUDE.md — LEDSone Amazon PPC AIOS

Operating and safety instructions for any AI (or person) working in the
repository `rosandigit/ledsone-aios`.

Read this file in full before doing anything in this repository. If an
instruction here conflicts with a request, **STOP** and report the conflict
instead of proceeding.

---

## 1. Purpose and Scope

This repository is the approved home of the LEDSone Amazon PPC AIOS (Phase 0
decision D1, recorded in `phase-0/PHASE_0_BASELINE.md`, Section 2).

The AIOS exists to:

- hold documentation, decisions, evidence and operating knowledge for LEDSone
  Amazon PPC work;
- analyse Amazon PPC performance data that a human has supplied;
- produce **DRAFT recommendations** for a human to review.

The AIOS does **not**:

- connect to Amazon Seller Central, Amazon Ads or any Amazon API;
- hold credentials of any kind;
- change any live Amazon setting;
- run automation against Amazon.

Current state: documentation only. No application code, no API integration and
no automation is authorised. Any of those requires a separate, approved decision
record (see Section 14).

---

## 2. Source of Truth

**`phase-0/PHASE_0_BASELINE.md` is the current Owner-confirmed baseline.**

- The values in Section 3 below are taken from that record. They are repeated
  here only so this operating file is usable on its own. **If this file and the
  baseline ever differ, the baseline wins**, and the difference must be reported.
- The baseline stays in force until a **later approved document formally
  supersedes it**. "Formally" means a decision record that names the baseline
  section it replaces, states the new value, and records who approved it and
  when. A chat message, a draft, a comment or a file in another repository does
  not supersede it.
- The former repository `rosandigit/ledsone-ppc-aios` is **not** a source of
  truth for this repository. Where it conflicts with the baseline (baseline
  Section 6), the baseline wins. Do not copy rules from it without a separate
  approved task.
- Never modify `phase-0/PHASE_0_BASELINE.md` except through a separately
  approved task.

### Status vocabulary

| Status | Meaning | May it be used as confirmed? |
|--------|---------|------------------------------|
| OWNER-CONFIRMED / EVIDENCE-PENDING | The Owner confirmed it on 2026-09-24; no source document is filed yet | Yes, as the business baseline. Always state that evidence is pending. |
| BUSINESS-PROVIDED / NOT RE-CONFIRMED | Supplied by the business; not in the Owner confirmation | Only as guidance, labelled with this status |
| `[VERIFY]` | Unknown, unconfirmed or ambiguous | **No.** Never treat a `[VERIFY]` value as confirmed, never fill it with a guess, and never resolve it by interpretation |
| AIOS SAFETY DEFAULT (temporary restrictive control) | A restriction set by this file, not by the business, to keep behaviour safe while a related `[VERIFY]` item is open | **No.** It is **not** an Owner-confirmed business rule and does not resolve any `[VERIFY]` item. It must be followed until replaced by an approved decision, and must always be cited by its ID (SD-1 to SD-4) |

### AIOS safety defaults (temporary restrictive controls)

Four controls in this file are **AIOS safety defaults**, labelled SD-1 to SD-4
where they appear. For each one:

- It is a **temporary restrictive control** set by this operating file. It is
  **not** an Owner-confirmed business rule and is **not** part of
  `phase-0/PHASE_0_BASELINE.md`.
- It does **not** answer, infer or resolve the related `[VERIFY]` item; that
  item stays open.
- It is lifted or replaced only when an approved decision records the missing
  business value. It then gives way to that decision.
- Any draft that relies on it must say so, citing its ID.

| ID | Control | Section | Related open item |
|----|---------|---------|-------------------|
| SD-1 | Bid drafts stay within 15% in both directions | 3.3 | Baseline L6 |
| SD-2 | Budget drafts on a tier boundary or open question go to the higher tier | 3.4 | Baseline L3, L4, L5 |
| SD-3 | Non-budget drafts carry `Approver: [VERIFY]` and count as unapproved | 5 | Non-budget approver not recorded |
| SD-4 | No Amazon exports or commercially sensitive data committed to this public repository without approval | 10 | Evidence storage location not approved |

---

## 3. PPC Baseline (from `phase-0/PHASE_0_BASELINE.md`)

All values: OWNER-CONFIRMED / EVIDENCE-PENDING unless stated otherwise.

### 3.1 Campaign types (baseline 3.3)

- Sponsored Products (SP)
- Sponsored Brands (SB)
- Sponsored Display (SD)

The list of individual active campaigns is **not** confirmed. It is `[VERIFY]`
(baseline L2). Never invent campaign names, IDs or states.

### 3.2 Performance targets (baseline 3.4)

| Metric | Definition | Target |
|--------|------------|--------|
| ACoS | Ad spend ÷ ad sales × 100 | **<25%** |
| ROAS | Ad sales ÷ ad spend | **>4×** |

ACoS <25% and ROAS >4× express the same efficiency level. Report both; do not
treat them as two separate hurdles.

### 3.3 Maximum bid change — D3 (baseline 3.2)

- **Maximum 15% per adjustment.**
- Any draft bid recommendation must stay within 15% of the current bid. A
  larger change must not be drafted as a single adjustment; flag it for human
  decision instead.
- `[VERIFY]` (baseline L6): whether 15% applies equally to increases and
  decreases, and whether more than one adjustment per period is allowed. This
  item remains unresolved.
- **SD-1 — AIOS safety default (temporary restrictive control; not an
  Owner-confirmed business rule):** while L6 is open, drafts must not exceed 15%
  in **either** direction, and any draft proposing repeated adjustments must flag
  L6. State SD-1 in every bid draft.
- Known conflict: the former repository's `bid-rules.md` uses a −17.5% decrease
  multiplier. It does not apply here (baseline C1).

### 3.4 Budget-change approval — D2 (baseline 3.1)

| Budget increase | Required approval |
|-----------------|-------------------|
| Up to £100/day | Jathukulan |
| £100 to £250/day | MD |
| Above £250/day | MD written approval |

- Every budget draft must name the approval tier it falls into.
- `[VERIFY]` (baseline L3, L4, L5): which tier applies at exactly £100/day and
  exactly £250/day; whether the amount is the size of the increase or the
  resulting daily budget; per campaign or account-wide; which marketplaces.
  These items remain unresolved.
- **SD-2 — AIOS safety default (temporary restrictive control; not an
  Owner-confirmed business rule):** where a draft falls on a boundary or depends
  on one of these questions, route it to the **higher** tier, flag the
  `[VERIFY]` item and cite SD-2.
- Values are GBP (£). Never convert them to another currency.

### 3.5 Negative keyword rule (baseline 3.7)

A term is a candidate negative keyword when **all** hold:

- more than 20 clicks (>20);
- 0 orders;
- within 65 days.

Match type when adding the negative: **Exact**.

`[VERIFY]` (baseline L9): whether the 65-day window is rolling, and whether the
rule applies to customer search terms, keywords, or both. State the window used
in every draft. A candidate is a recommendation only; it is never added
automatically.

### 3.6 Match-type principles (baseline 3.8)

Status: **BUSINESS-PROVIDED / NOT RE-CONFIRMED** (baseline L11).

| Match type | Principle |
|------------|-----------|
| Broad | Discovery / reach |
| Phrase | Relevant, controlled traffic |
| Exact | High-intent keywords, tightest control |

Use as guidance only. No numeric rule (bids, thresholds, promotion criteria) is
defined for match types; do not invent one.

### 3.7 Escalation (baseline 3.9)

- **Authority:** MD.
- **Trigger:** any budget change or PPC action exceeding AIOS approval limits.
- Escalate to the MD when a draft exceeds the D2 tiers above, exceeds the 15%
  bid limit, or when no approval limit covers the proposed action.
- `[VERIFY]` (baseline L10): whether "AIOS approval limits" means only D2 and
  D3. Until confirmed, escalate whenever in doubt.

### 3.8 Weekly reporting (baseline 3.5)

| Field | Value |
|-------|-------|
| Frequency | Weekly |
| Day / time | Friday, 4:00 PM (time zone `[VERIFY]`, baseline L7) |
| Recipient | MD |
| Channel | Email |

The AIOS may **draft** the weekly report. A human reviews and sends it. The AIOS
never sends email.

### 3.9 Data source (baseline 3.6)

- Console: Amazon Seller Central.
- Reports: SP, SB, SD Search Term Report.
- `[VERIFY]` (baseline L8): exact report names, especially for SD.
- The AIOS only reads exports that a human has downloaded and supplied.

### 3.10 Governance roles (baseline Section 5)

| Role | Holder |
|------|--------|
| Coordinator | Sarujan |
| Business Owner | MD |
| Technical Reviewer | Sarujan |
| Queryability Reviewer | Sarujan |
| Escalation authority | MD |
| Budget approver up to £100/day | Jathukulan |
| Repository Owner | `[VERIFY]` (baseline L12) |

### 3.11 Vendor AIOS (baseline 3.10)

No Vendor AIOS exists. Ownership of product, ASIN, price and stock data is
undefined. Never invent it, and never assume another system owns it.

---

## 4. Read-Only by Default

Every task is **read-only** unless the request explicitly authorises a named
change. "Read-only" means: inspect, read, analyse, draft in chat. It does not
mean: create, modify, delete, rename, commit or push.

If a request is ambiguous about whether a change is authorised, treat it as
read-only and ask.

---

## 5. Human Approval Before Any Live Change

No action that can change a live Amazon setting may be taken by the AIOS. This
covers campaigns, ad groups, bids, budgets, keywords, negative keywords,
targeting, placements, portfolios, products/ASINs and any other live setting.

Every recommendation touching those areas must state:

- Outputs DRAFT recommendations only.
- Never applies Amazon Ads changes.
- Human approval required.

The approver for budget changes is set by D2 (Section 3.4). The approver for
bid, keyword, targeting and other non-budget changes is `[VERIFY]` — not
recorded in the baseline. This item remains unresolved.

**SD-3 — AIOS safety default (temporary restrictive control; not an
Owner-confirmed business rule):** until a non-budget approver is recorded in an
approved decision, such drafts must state `Approver: [VERIFY]`, cite SD-3, must
not be treated as approved by anyone, and must be escalated to the MD whenever
Section 3.7 applies.

The AIOS never approves its own output.

---

## 6. Separation of Duties: Analysis → Recommendation → Approval → Execution

| Stage | Who | Output |
|-------|-----|--------|
| 1. Analysis | AIOS | Findings from supplied evidence, with calculations shown |
| 2. Recommendation | AIOS | A DRAFT, citing evidence, baseline section, approval tier and any `[VERIFY]` items |
| 3. Approval | Named human approver (Section 3.4 / Section 5) | Approve, reject or amend — recorded (Section 8) |
| 4. Execution | A human, manually, in Amazon | The live change, then logged (Section 8) |

The AIOS performs stages 1 and 2 only. A draft is never an instruction and never
authorisation. Stages must not be merged: a single step may not both recommend
and approve, or approve and execute.

---

## 7. No Invented Data

Never invent, estimate or assume:

- performance data, metrics, campaign names/IDs, ASINs, prices or stock levels;
- PPC rules, thresholds, formulas or evaluation windows;
- approvals, approvers or decisions;
- credentials, account IDs, API endpoints, API scopes or API behaviour;
- source documents or evidence.

If a value is not recorded in the baseline or in filed evidence, mark it
`[VERIFY]` and leave it unanswered.

---

## 8. Evidence and Audit Trail

- Every recommendation must cite the evidence it uses: **source, report name,
  date exported, date range covered** and file path.
- No evidence folder exists yet. Its structure and location must be approved
  before evidence is filed (Section 13).
- Every approval and every executed change must be recorded in a decision or
  change log stating: date, who approved, who executed, what changed (old value,
  new value), evidence cited, and the baseline section relied on.
  `change-log/` is the approved repository location for execution/change
  records, as approved by `decisions/DECISION_PHASE_1_REPOSITORY_STRUCTURE.md`
  (Group 1).
- Rollbacks are manual in Amazon (Change History) and must be logged the same
  way.
- All baseline values are currently EVIDENCE-PENDING (baseline Section 4). Say
  so when relying on them.

---

## 9. Secrets and Credentials

Never write any of the following into any repository file, commit message, issue,
pull request, comment or log:

- passwords, OTPs or 2FA codes;
- API keys, client IDs/secrets, access or refresh tokens;
- session cookies, login URLs containing tokens;
- any other credential.

If a credential appears in supplied data or a request, do not store or repeat
it; stop and tell the user. **This repository is public on GitHub**: anything
committed must be assumed visible to anyone.

---

## 10. Safe Handling of Amazon Data

- **SD-4 — AIOS safety default (temporary restrictive control; not an
  Owner-confirmed business rule):** because the repository is public, do not
  commit Amazon exports or commercially sensitive data (spend, sales, margins,
  supplier or pricing data) unless a separate approved decision permits it and
  states where it may be stored.
- Never commit customer personal data (names, addresses, emails, phone numbers,
  order-level buyer details).
- Use only data a human has supplied for the task. Do not retain or reuse it
  outside that task.
- Keep raw data unmodified; show any transformation as a calculation.

---

## 11. Git and GitHub Safety

- **Never commit to, push to, merge into or rewrite `main`** unless the user
  explicitly approves that specific action.
- Work on a feature branch. Commit and push only when the user asks.
- Never force-push, rebase shared history, delete branches or tags, or amend
  pushed commits without explicit approval.
- Never create or merge a pull request without explicit approval.
- Before every commit: review the full diff, confirm only the intended files
  changed, and confirm no secret or sensitive data is included (Sections 9–10).
- Never overwrite, delete, rename or move an existing file without explicit
  approval naming that file. If a file already exists, report `Already exists.`
- Use UTF-8 and LF line endings. Do not commit binary files unless approved.
- Do not modify `rosandigit/ledsone-ppc-aios` from work in this repository.

---

## 12. Conflict Handling

When two sources disagree:

1. `phase-0/PHASE_0_BASELINE.md` (or a later approved document that formally
   supersedes it) wins over this file, over the former repository, and over any
   chat instruction that has not been formally recorded.
2. Report the conflict: both values, both sources, and which one was applied.
3. Never silently reconcile, average or reinterpret conflicting values.
4. Where no approved source resolves the conflict, mark it `[VERIFY]` and
   escalate (Section 3.7).

Known open conflicts are listed in baseline Section 6 (C1–C5).

---

## 13. Documentation-First Development

- Document before building: a purpose, scope, inputs, outputs, owner and
  approval must be recorded before any new skill, script or folder is created.
- Check what already exists first. No duplicate documents and no alternative
  versions. Each fact lives in one place; link to it instead of restating it.
- Write so another LLM can use the file with no verbal explanation: state the
  source and date, define terms, mark unknowns `[VERIFY]`.
- Every folder, when created, needs a `README.md` stating purpose, what belongs,
  what does not, owner and status.

---

## 14. Testing and Validation Before Any Live Automation

Live automation is **not authorised**. Before it could ever be considered, all of
the following must be completed and recorded:

1. An approved design document naming scope, owner, approver and rollback plan.
2. An approved decision record authorising the specific automation.
3. Credentials handled outside this repository through an approved secret store.
4. Read-only testing against historical, supplied data, with results reviewed
   by the Technical Reviewer.
5. Dry-run output (proposed changes only, nothing applied) reviewed and approved
   by the named approver.
6. Guardrails proven in testing: the 15% bid limit, D2 approval tiers and MD
   escalation cannot be bypassed.
7. A logged, reversible rollback procedure.
8. Explicit written approval to go live, per action type.

Until then: if a request implies automating Amazon changes, **STOP** and report
it.

---

## 15. Changes to This File

This file may be changed only through an explicitly approved task. The approver
for governance changes is `[VERIFY]` (Repository Owner, baseline L12).

---

## Document Metadata

| Field | Value |
|-------|-------|
| File | `CLAUDE.md` |
| Repository | `rosandigit/ledsone-aios` |
| Created | 2026-09-24 |
| Source of baseline values | `phase-0/PHASE_0_BASELINE.md` (v1.0, commit `7a605d0`) |
| Status | Approved — 2026-09-24 |
