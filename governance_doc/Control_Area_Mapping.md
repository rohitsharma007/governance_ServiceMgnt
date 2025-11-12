# Testing Controls — Control Area Mapping

Purpose: Provide a clear, human-readable map of testing controls to control areas (Strategy, Plan, Execution, Governance/QM) so stakeholders can quickly understand responsibilities, artefacts, and approval points.

## Sources
- CSV: `docs/6.17.2025 System Development, Acquisition,Maintenance - testing Controls`
- Screenshots: `governance_doc/Test_Strategy.jpeg`, `Test_strategy_part2.jpeg`, `Test_strategy_part3.jpeg`, `TestPlan.jpeg`, `Test_execution.jpeg`, `control_Area_Mapping.jpeg`, `Test Standard1.jpeg`–`Test Standard6.jpeg`

## Control Areas
- Strategy: Defines overall testing approach, processes, infra, data, defect mgmt, automation, reporting.
- Plan: Documents test requirements, traceability, schedule/effort, domains, tech/tooling, approvals.
- Execution: Runs tests per plan and strategy; captures runs, defects, traceability, coverage, reports.
- Governance & Quality Management (G&QM): Independent review and feedback; escalated events; adherence to SDAM/quality practices.

## ID Differentiation (pattern in CSV)
- Each topic has two complementary controls:
  - Governance review (Non-key): G&QM reviews completeness and returns feedback if gaps remain.
  - Sponsor/Owner approval (Key): Sponsors/Application Owners formally approve artefacts prior to execution.
- Areas repeat with this pattern:
  - Requirements Analysis → PRC.TS.01 (G&QM review, Non-key) and PRC.TS.02 (Sponsor approval, Key)
  - Strategy → PRC.TS.03 (G&QM review, Non-key) and PRC.TS.04 (Sponsor approval, Key)
  - Plan → PRC.TS.05 (G&QM review, Non-key) and PRC.TS.06 (Sponsor approval, Key)

## Control-to-Area Mapping
- PRC.TS.01 — Requirements Analysis Review (G&QM, Non-key)
  - Area: Governance & QM + Inputs to Plan
  - Key artefacts: Testing Scope, Acceptance Criteria, Definition of Done, Estimates, Change Impact Analysis; Self-Assessment; G&QM Review Form; Charter
  - Sources: ADO, SNOW TMM, G&QM SharePoint

- PRC.TS.02 — Requirements Analysis Approval (Sponsors/Owners, Key)
  - Area: Plan (inputs) + Executive Sign-off
  - Key artefacts: Same as PRC.TS.01 plus documented approval by Sponsors and Application/Product Owners
  - Sources: ADO, SNOW TMM

- PRC.TS.03 — Strategy Review for Escalated Events (G&QM, Non-key)
  - Area: Governance & QM + Strategy
  - Key attributes: Scope, Approach, Processes/Methodology, Infrastructure, Data Mgmt, Defect Mgmt, Automation, Reporting & Communication; Self-Assessment; G&QM Review Form; Charter
  - Sources: ADO, SNOW TMM, G&QM SharePoint

- PRC.TS.04 — Strategy Approval (Sponsors/Owners, Key)
  - Area: Strategy + Executive Sign-off
  - Key attributes: Scope, Approach, Processes/Methodology, Infrastructure, Data Mgmt, Defect Mgmt, Automation, Reporting & Communication; documented approvals
  - Sources: ADO, SNOW TMM

- PRC.TS.05 — Plan Review for Escalated Events (G&QM, Non-key)
  - Area: Governance & QM + Plan
  - Key attributes: Test Requirements, Approach/Processes, Traceability Approach, Infrastructure, Schedule/Effort, Methodologies, Domains, Technology & Tooling; stakeholder approvals; Self-Assessment; G&QM Review Form; Charter
  - Sources: ADO, SNOW TMM, G&QM SharePoint

- PRC.TS.06 — Plan Approval (Sponsors/Owners, Key)
  - Area: Plan + Executive Sign-off
  - Key attributes: Test Requirements, Traceability Approach, Schedule/Effort; Methodologies/Domains/Tech & Tooling; documented approvals
  - Sources: ADO, SNOW TMM

## Execution Area (from screenshots)
- Indicative artefacts: Test case design, test runs/execution logs, defects lifecycle, traceability to requirements, coverage metrics, test data mgmt, environment readiness, reports/dashboards.
- Ownership: Project Testing Team executes; Governance reviews outcomes when escalated or per cadence.
- Note: Execution controls are typically numbered following planning controls (e.g., PRC.TS.07+). The provided CSV focuses on pre-execution approvals and reviews.

## Standards 1–6 (from screenshots)
- Standards references align across Strategy and Plan as quality gates:
  - S1–S2: Strategy completeness (scope, approach, methodology).
  - S3–S4: Plan completeness (traceability, infrastructure, schedule/effort).
  - S5–S6: Execution governance (defect mgmt, automation, reporting & communication).
- Recommendation: Tag artefacts in repositories (ADO/SNOW/SharePoint) with `Standard: S#` to simplify evidence retrieval.

## Practical Assignment Rules
- If artefact describes “how we test” → Strategy (PRC.TS.03/04).
- If artefact describes “what/when we test” → Plan (PRC.TS.05/06).
- If artefact records “testing done/results/issues” → Execution.
- If artefact records “independent review/feedback” → Governance & QM (PRC.TS.01/03/05).
- If artefact records “formal approval” → Sponsors/Owners (PRC.TS.02/04/06).

## Quick Visual Key
- Governance & QM (Non-key): PRC.TS.01, PRC.TS.03, PRC.TS.05
- Sponsors/Owners (Key): PRC.TS.02, PRC.TS.04, PRC.TS.06
- Strategy: PRC.TS.03, PRC.TS.04
- Plan: PRC.TS.05, PRC.TS.06
- Execution: Evidence generated post-approval; tracked in ADO/SNOW; reviewed per governance cadence.

## Placement Guidance (repositories)
- ADO Boards/Wikis: host Strategy and Plan; link work items to artefacts; tag with PRC.TS.* and S1–S6.
- SNOW TMM: store approval records and test case libraries; link to Plan and Strategy IDs.
- SharePoint (G&QM): store review forms, charters, self-assessments; maintain escalated event records.

## Notes
- Typos in CSV (e.g., “plants”, “desumentation”) are preserved in source but normalized here for clarity.
- This mapping document is explanatory; it does not alter code and can be published beside `control_Area_Mapping.jpeg` for an accessible text version.