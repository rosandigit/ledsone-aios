# Phase 1 Operational Workflow

## 1. Purpose

Defines the documentation-only operating workflow for the LEDSone Amazon PPC AIOS during Phase 1.

The workflow supports evidence-based PPC analysis and DRAFT recommendations. It does not authorize Amazon Ads API access, application code, automation, or live Amazon changes.

## 2. Scope

This workflow covers:

1. Evidence collection and verification.
2. PPC data analysis.
3. DRAFT recommendation preparation.
4. Human review and approval.
5. Manual execution by an authorized human.
6. Change logging.
7. Weekly reporting.

The AIOS does not execute Amazon Ads changes and does not send email.

## 3. Source of Truth

* Business values and PPC baseline: `phase-0/PHASE_0_BASELINE.md`
* Operating and safety rules: `CLAUDE.md`
* Formal approvals and governance decisions: `decisions/`
* Evidence metadata: `evidence/`
* Executed change records: `change-log/`
* Weekly report template and sent-log records: `reports/weekly/`

If documents conflict, the approved baseline and applicable governance rules take precedence.

## 4. Workflow

### Stage 1 — Evidence

Collect the required Amazon PPC source reports outside this public repository.

Create an evidence metadata record in `evidence/` containing:

* source;
* report name;
* export date;
* date range;
* exporter;
* approved storage reference.

Do not commit Amazon exports, screenshots of export contents, commercial figures, customer data, credentials, or access links to this repository.

### Stage 2 — Analysis

Analyse the supplied PPC evidence against the approved Phase 0 baseline.

The analysis must:

* use the available evidence;
* identify the relevant campaign, ad group, keyword, target or other level;
* avoid invented values;
* identify `[VERIFY]` items where evidence is incomplete;
* remain within the approved AIOS scope.

### Stage 3 — DRAFT Recommendation

Prepare DRAFT recommendations only.

Each recommendation must identify:

* proposed action;
* relevant evidence;
* applicable rule or approval authority;
* required approval tier or approver;
* safety constraints;
* `[VERIFY]` items, where applicable.

A DRAFT recommendation is not an executed Amazon change.

### Stage 4 — Human Approval

A human reviews the DRAFT recommendation and provides the required approval under the applicable approved rule or decision.

No Amazon change may be treated as approved merely because the AIOS produced a recommendation.

If required approval is unavailable, the recommendation remains unapproved.

### Stage 5 — Manual Execution

An authorized human manually executes an approved change in Amazon.

The AIOS does not:

* connect to Amazon Ads;
* use Amazon credentials;
* call Amazon APIs;
* automatically change bids, budgets, keywords, targets or campaign settings.

### Stage 6 — Change Record

After an approved change is manually executed, record the execution in:

`change-log/CHANGE_<YYYY-MM-DD>_<TOPIC>.md`

The record must identify the applicable approval or authority, executor, change, evidence, result and rollback information.

Do not record exact bid or budget amounts in the public repository while the sensitive-value `[VERIFY]` item in `change-log/README.md` remains unresolved.

### Stage 7 — Weekly Report

Prepare the weekly PPC report using:

`reports/weekly/TEMPLATE_WEEKLY_REPORT.md`

The completed report is stored outside this public repository in the approved storage location.

The AIOS may draft the report. A human reviews and sends it.

After sending, create the applicable:

`reports/weekly/SENT_<YYYY-MM-DD>.md`

sent-log record.

## 5. Safety Controls

The following remain in force:

* AIOS outputs DRAFT recommendations only.
* Human approval is required before live changes.
* AIOS never applies Amazon Ads changes.
* Amazon exports and commercially sensitive data remain outside this public repository unless separately approved.
* `[VERIFY]` values are never guessed.
* Approved baseline values are not changed by this workflow.
* Any application code, Amazon API access or automation requires a separate approved decision and task.

## 6. Roles

| Role                  | Responsibility                                                          |
| --------------------- | ----------------------------------------------------------------------- |
| Coordinator           | Maintains the workflow and coordinates evidence, analysis and reporting |
| Business Owner / MD   | Provides required business approval and escalation                      |
| Technical Reviewer    | Reviews technical and safety compliance                                 |
| Queryability Reviewer | Reviews whether required evidence can be queried and traced             |
| Executing Human       | Manually performs an approved Amazon change                             |
| AIOS                  | Analyses supplied evidence and prepares DRAFT recommendations only      |

Current role assignments and approval authorities are governed by the approved Phase 0 baseline and applicable decision records.

## 7. Audit Trail

For each recommendation or executed change, maintain traceability:

`Evidence → Analysis → DRAFT Recommendation → Human Approval → Manual Execution → Change Record → Weekly Report`

Where a stage does not apply, record the reason rather than inventing a value.

## 8. Open Items

Any unresolved governance item remains `[VERIFY]` until confirmed through the applicable approved process.

This document does not resolve or replace any `[VERIFY]` item in the Phase 0 baseline, `CLAUDE.md`, or decision records.

## 9. Status

Created as an explicitly approved Phase 1 operational documentation task.

This document changes no Amazon setting, baseline value, approval rule, budget, bid, keyword, targeting setting or campaign.
