# Phase 0 Baseline — LEDSone Amazon PPC AIOS

Owner-confirmed Phase 0 business baseline for LEDSone Amazon PPC work, recorded
in the approved PPC home repository `rosandigit/ledsone-aios`.

This record documents decisions. It performs no action. It does not change
Amazon Ads, does not build skills or automation, and does not change any file in
the former repository `rosandigit/ledsone-ppc-aios`.

---

## Document Metadata

| Field | Value |
|-------|-------|
| Record type | Phase 0 verification / decision record |
| Repository | `rosandigit/ledsone-aios` |
| Path | `phase-0/PHASE_0_BASELINE.md` |
| Date recorded | 2026-09-24 |
| Date values were confirmed | 2026-09-24 (Owner confirmation supplied in the Phase 0 baseline task) |
| Status | Active — Owner-confirmed; source evidence pending |
| Version | 1.0 |

---

## 1. Requirement / Purpose

The Owner required one Phase 0 record that states, in one place, the confirmed
business baseline for LEDSone Amazon PPC work, before any further PPC assets are
created in this repository.

This record exists so that any person or LLM can answer, without verbal
explanation:

- where LEDSone PPC work now lives;
- which business values the Owner has confirmed;
- which of those values have filed source evidence (currently: none);
- who holds each governance role;
- which conflicts with the former repository are known and unresolved;
- what must happen next.

**Safety statement.** Anything derived from this baseline that involves bids,
budgets, keywords, campaigns or targeting:

- Outputs DRAFT recommendations only.
- Never applies Amazon Ads changes.
- Human approval required.

---

## 2. Approved Repository / Home

**Decision D1 — PPC home: `rosandigit/ledsone-aios`.** Status: OWNER-CONFIRMED.

Repository state inspected immediately before this record was written
(2026-09-24):

- one commit on `main`: `4e50246` ("Initial commit");
- one file: `README.md`, containing only the line `# ledsone-aios`;
- no `CLAUDE.md`, no `context/`, no `evidence/`, no existing Phase 0 location.

No equivalent Phase 0 location existed, so `phase-0/` was created for this
record only.

**Former repository:** `rosandigit/ledsone-ppc-aios` (inspected at commit
`b69a2b0`). It still holds the earlier PPC documentation, rule files, skills and
governance. It was **not** copied, modified or deleted. Its relationship to this
repository after D1 is covered in **Sections 6 and 7**.

---

## 3. Owner-Confirmed Baseline Values

Values below are recorded exactly as the Owner supplied them. Nothing has been
interpreted, converted or extended. Where the wording leaves a question open,
the question is listed in **Section 8** as `[VERIFY]`; it is not answered here.

Status vocabulary used in this record:

| Status | Meaning |
|--------|---------|
| OWNER-CONFIRMED / EVIDENCE-PENDING | The Owner confirmed the value on 2026-09-24. No source document supporting it is filed in this repository. |
| BUSINESS-PROVIDED / NOT RE-CONFIRMED | The business supplied the value in the Phase 0 baseline of 2026-09-23. It was not included in the 2026-09-24 Owner confirmation. |
| PENDING | No value has been supplied. |

### 3.1 D2 — Budget Approval

| Budget increase | Who approves |
|-----------------|--------------|
| Up to £100/day | Jathukulan approval |
| £100 to £250/day | MD approval |
| Above £250/day | MD written approval |

Status: OWNER-CONFIRMED / EVIDENCE-PENDING.

### 3.2 D3 — Maximum Bid Change

- Maximum **15% per adjustment**.

Status: OWNER-CONFIRMED / EVIDENCE-PENDING. D3 is the approved business
baseline. See **Section 6, Conflict C1** for the conflict with the former
repository.

### 3.3 Campaign Types

- Sponsored Products (SP)
- Sponsored Brands (SB)
- Sponsored Display (SD)

Status: OWNER-CONFIRMED / EVIDENCE-PENDING.

The **active campaign register** (the list of individual live campaigns, with
name, ID, ad type and state) is **PENDING**. Only the three campaign types are
confirmed.

### 3.4 Performance Targets

| Metric | Target |
|--------|--------|
| ACoS (Advertising Cost of Sales = ad spend ÷ ad sales × 100) | **<25%** |
| ROAS (Return on Ad Spend = ad sales ÷ ad spend) | **>4×** |

Status: OWNER-CONFIRMED / EVIDENCE-PENDING.

### 3.5 Weekly Reporting

| Field | Value |
|-------|-------|
| Frequency | Weekly |
| Day | Friday |
| Time | 4:00 PM |
| Recipient | MD |
| Channel | Email |

Status: OWNER-CONFIRMED / EVIDENCE-PENDING.

### 3.6 PPC Data Source

| Field | Value |
|-------|-------|
| Console | Amazon Seller Central |
| Reports | SP, SB, SD Search Term Report |

Status: OWNER-CONFIRMED / EVIDENCE-PENDING.

### 3.7 Negative Keyword Rule

A term qualifies as a negative keyword when **all** of the following hold:

- more than 20 clicks (>20);
- 0 orders;
- within 65 days.

Match type used when adding the negative: **Exact**.

Status: OWNER-CONFIRMED / EVIDENCE-PENDING.

### 3.8 Match Strategy

| Match type | Purpose |
|------------|---------|
| Broad | Keyword discovery / reach |
| Phrase | Relevant traffic + control |
| Exact | High-intent keywords + tighter control |

Status: BUSINESS-PROVIDED / NOT RE-CONFIRMED. This was item 9 of the Phase 0
business baseline supplied on 2026-09-23. It was not listed in the 2026-09-24
Owner confirmation, so it is recorded here without Owner-confirmed status.

### 3.9 Escalation

| Field | Value |
|-------|-------|
| Authority | MD |
| Trigger | Any budget change or PPC action exceeding AIOS approval limits |

Status: OWNER-CONFIRMED / EVIDENCE-PENDING.

### 3.10 Vendor AIOS

- A Vendor AIOS **does not exist**.
- Ownership of product, ASIN, price and stock data **remains undefined** and
  must not be invented.

Status: OWNER-CONFIRMED.

### Baseline coverage check

| # | Phase 0 baseline area | Recorded in | Status |
|---|-----------------------|-------------|--------|
| 1 | Active campaign types (SP, SB, SD) | 3.3 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| 2 | ACoS target | 3.4 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| 3 | ROAS target | 3.4 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| 4 | Budget approval (D2) | 3.1 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| 5 | Maximum bid change (D3) | 3.2 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| 6 | Weekly reporting | 3.5 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| 7 | PPC data source | 3.6 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| 8 | Negative keyword rule | 3.7 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| 9 | Match strategy | 3.8 | BUSINESS-PROVIDED / NOT RE-CONFIRMED |
| 10 | Escalation | 3.9 | OWNER-CONFIRMED / EVIDENCE-PENDING |
| — | PPC home (D1) | 2 | OWNER-CONFIRMED |
| — | Governance roles | 5 | OWNER-CONFIRMED |
| — | Vendor AIOS | 3.10 | OWNER-CONFIRMED |

---

## 4. Source / Evidence Status

**No source evidence is filed in this repository.** Every value in Section 3 is
recorded on the strength of the Owner's (or, for 3.8, the business's)
confirmation alone. None is externally evidenced.

| Value | Source document filed here? | Source cited elsewhere |
|-------|-----------------------------|------------------------|
| D1 PPC home | No — Owner decision, recorded by this document | None |
| D2 budget approval | No | Former repo `context/budget-rules.md` holds the tiered structure but no £ values |
| D3 maximum bid change | No | None |
| Campaign types | No | None |
| ACoS / ROAS targets | No | Former repo `context/target-metrics.md` cites "Approved PPC Metrics (2026-07-22)" and `Amazon_BGCT_PayPerClick.pdf`; neither document is filed in either repository |
| Weekly reporting | No | None |
| PPC data source | No | None |
| Negative keyword rule | No | None |
| Match strategy | No | None |
| Escalation | No | None |
| Governance roles | No — Owner decision, recorded by this document | None |
| Vendor AIOS | No — Owner decision, recorded by this document | None |

No source document has been invented. Where a value has no source document, it
stays EVIDENCE-PENDING until one is filed.

---

## 5. Owner / Reviewer Fields

| Role | Holder | Status |
|------|--------|--------|
| Coordinator | Sarujan | OWNER-CONFIRMED |
| Business Owner | MD | OWNER-CONFIRMED |
| Technical Reviewer | Sarujan | OWNER-CONFIRMED |
| Queryability Reviewer | Sarujan | OWNER-CONFIRMED |
| Escalation authority | MD | OWNER-CONFIRMED (see 3.9) |
| Budget approver, up to £100/day | Jathukulan | OWNER-CONFIRMED (see 3.1) |
| Repository Owner of `rosandigit/ledsone-aios` | [VERIFY] — not stated in the Phase 0 confirmation. Jathukulan is the recorded Owner of the former repository `rosandigit/ledsone-ppc-aios`. | PENDING |

"MD" is recorded as a role. The individual who holds it is not named in the
confirmation.

---

## 6. Known Conflicts with the Former Repository

The former repository `rosandigit/ledsone-ppc-aios` (commit `b69a2b0`) was
**not modified** in this task. Each conflict below is a
**migration/reconciliation item requiring a separate, approved task**.

### C1 — Maximum bid change

| Source | Content |
|--------|---------|
| This baseline (D3) | Maximum 15% per adjustment |
| Former repo `context/bid-rules.md`, line 17 | Multiplier ×1.125 for increases (+12.5%) and ×0.825 for decreases (−17.5%) |

The −17.5% decrease multiplier exceeds the D3 maximum. D3 is the approved
business baseline. The former file was not edited. Required action: a separate
approved reconciliation task.

### C2 — Budget approval thresholds

| Source | Content |
|--------|---------|
| This baseline (D2) | Up to £100/day — Jathukulan; £100 to £250/day — MD; above £250/day — MD written approval |
| Former repo `context/budget-rules.md`, lines 41–46 | The same three-tier structure (Jathukulan → MD → MD written approval), with every £ threshold marked `[VERIFY]` |

The structure matches; the Owner has now confirmed £100 and £250 for this
baseline. The former file still shows `[VERIFY]` and was not edited. Required
action: a separate approved task to reconcile the former file (or retire it)
under D1.

### C3 — Original Phase 0 budget wording

The business's original Phase 0 wording (2026-09-23) was "Budget increases
require MD approval." D2 supersedes it for this baseline: increases up to
£100/day are approved by Jathukulan. The original wording must not be reused.

### C4 — Data source naming

| Source | Content |
|--------|---------|
| This baseline | Amazon Seller Central; SP, SB, SD Search Term Report |
| Former repo `context/target-metrics.md` | "Amazon Ads reporting"; exact report name `[VERIFY]` |

Recorded, not reconciled.

### C5 — Governance and safety rules not yet in this repository

The former repository's `CLAUDE.md` holds the operating and safety rules (for
example: never modify Amazon Ads, evidence first, `[VERIFY]` for undocumented
values, no duplicate truth, existing-asset-first) and three Owner-approved
authorisation clauses (marketplace scope UK, DE, FR, IT; US excluded). This
repository has no `CLAUDE.md`. Those rules are therefore **not yet in force
here**. They were not copied, by instruction.

---

## 7. Duplicate-Truth Risk

1. **Two PPC homes.** Until the former repository is formally reconciled or
   retired, both `rosandigit/ledsone-ppc-aios` and `rosandigit/ledsone-aios`
   describe LEDSone PPC. **For the Phase 0 baseline values in Section 3, this
   record is the authoritative source.** Where the former repository disagrees
   (Section 6), this record wins.
2. **Values restated from the former repository.** ACoS <25%, ROAS >4× and the
   D2 tier structure also appear in the former repository. They are recorded
   here only because the Owner re-confirmed them as the Phase 0 baseline. No
   rule file was copied, and no rule file was created in this repository.
3. **Future rule files.** Any later file in this repository that holds bid,
   budget, reporting, negative-keyword or escalation rules must either **link to
   this record** for these values or **explicitly supersede it** through a new
   approved decision record. It must not restate them independently.
4. **Inventory knowledge base.** A separate inventory AIOS knowledge base
   (reached through the `inv_AIOS` connector) contains `database/schemas/ppc/`,
   `integrations/amazon/` and stock rules. Its relationship to this repository
   is undefined. Product, ASIN, price and stock ownership remains undefined
   (3.10) and must not be assumed to live there.

Result: duplicate-truth risk is **documented, not eliminated**. Elimination
requires the reconciliation tasks in Section 6.

---

## 8. Known Limitations

| # | Limitation | Exact information still required |
|---|------------|----------------------------------|
| L1 | No source evidence filed for any value (Section 4) | The original source documents, filed with source, date and date range |
| L2 | Active campaign register not supplied | A campaign export: name, ID, ad type (SP/SB/SD), state, marketplace |
| L3 | D2 boundary wording: "Up to £100/day" and "£100 to £250/day" both include £100 | [VERIFY] Which tier applies at exactly £100/day, and at exactly £250/day |
| L4 | D2 measure | [VERIFY] Whether the £ amount is the size of the increase or the resulting daily budget, and whether it applies per campaign or account-wide |
| L5 | Currency and marketplace scope | [VERIFY] Values are in GBP (£). Which marketplaces they apply to is not stated. Do not convert them to other currencies |
| L6 | D3 scope | [VERIFY] Whether 15% applies equally to increases and decreases, and whether more than one adjustment per period is permitted |
| L7 | Weekly report time zone | [VERIFY] Time zone for "4:00 PM" |
| L8 | Sponsored Display report name | [VERIFY] Confirm the exact report name for SD in the console; confirm the exact report names for SP and SB |
| L9 | Negative keyword rule scope | [VERIFY] Whether the 65-day window is rolling, and whether the rule applies to customer search terms, keywords, or both |
| L10 | Escalation trigger | [VERIFY] "AIOS approval limits" — confirm this means the D2 and D3 limits only |
| L11 | Match strategy (3.8) | Owner re-confirmation |
| L12 | Repository Owner of `rosandigit/ledsone-aios` | A named Owner |
| L13 | Role concentration | Sarujan holds Coordinator, Technical Reviewer and Queryability Reviewer. Recorded as confirmed; noted for awareness only |
| L14 | No `CLAUDE.md` in this repository (C5) | An approved operating and safety governance file for this repository |
| L15 | Former repository not reconciled (C1, C2, C4) | Separate approved migration/reconciliation tasks |

---

## 9. Pass / Fail Status

| Criterion | Result |
|-----------|--------|
| All 10 Phase 0 baseline areas recorded | PASS — Section 3 coverage check |
| D1, D2 and D3 recorded | PASS — Sections 2, 3.1, 3.2 |
| Governance roles recorded | PASS — Section 5 |
| Evidence status explicit | PASS — Section 4; every value marked EVIDENCE-PENDING or NOT RE-CONFIRMED |
| Duplicate-truth risks documented | PASS — Section 7 |
| No unsafe production action | PASS — no Amazon Ads change, no automation, no skill built, former repository untouched |
| Queryable by another LLM without verbal explanation | PASS — terms defined, sources and dates stated, open questions marked `[VERIFY]` |

**Phase 0 status: PASS — baseline recorded; evidence pending.**

PASS means the baseline is recorded. It does **not** mean the values are
evidenced (Section 4), and it does not resolve the conflicts in Section 6.

---

## 10. Next Step

Create an approved operating and safety governance file (`CLAUDE.md`) for
`rosandigit/ledsone-aios` as a separate, Owner-approved task, **before** any
further PPC asset is created in this repository (Limitation L14).
