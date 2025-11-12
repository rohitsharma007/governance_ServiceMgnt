# Testing Controls — Control Area Mapping (Tabular)

Purpose: Provide a clear, presentable table view that maps controls to areas, roles, artefacts, and sources.

## Sources
- CSV: `docs/6.17.2025 System Development, Acquisition,Maintenance - testing Controls`
- Screenshots: Strategy, Plan, Execution, Standards 1–6, and `control_Area_Mapping.jpeg`

## Controls Overview
| Control ID | Control Name | Area | Role | Key/Non-key | Authority | Primary Artefacts | Sources |
|---|---|---|---|---|---|---|---|
| PRC.TS.01 | Requirements Analysis Review | Governance & QM; inputs to Plan | G&QM reviewers | Non-key | G&QM review/feedback | Testing Scope; Acceptance Criteria; Definition of Done; Estimates; Change Impact Analysis; Self-Assessment; Review Form; Charter | ADO; SNOW TMM; G&QM SharePoint |
| PRC.TS.02 | Requirements Analysis Approval | Plan (inputs) | Sponsors; App/Product Owners | Key | Formal approval prior to execution | Same artefacts as PRC.TS.01 plus documented approvals | ADO; SNOW TMM |
| PRC.TS.03 | Strategy Review for Escalated Events | Governance & QM; Strategy | G&QM reviewers | Non-key | G&QM review/feedback | Scope; Approach; Processes/Methodology; Infrastructure; Data Mgmt; Defect Mgmt; Automation; Reporting & Communication; Self-Assessment; Review Form; Charter | ADO; SNOW TMM; G&QM SharePoint |
| PRC.TS.04 | Strategy Approval | Strategy | Sponsors; App/Product Owners | Key | Formal approval prior to execution | Scope; Approach; Processes/Methodology; Infrastructure; Data Mgmt; Defect Mgmt; Automation; Reporting & Communication; documented approvals | ADO; SNOW TMM |
| PRC.TS.05 | Test Plan Review for Escalated Events | Governance & QM; Plan | G&QM reviewers | Non-key | G&QM review/feedback | Test Requirements; Approach/Processes; Traceability Approach; Infrastructure; Schedule/Effort; Methodologies; Domains; Tech & Tooling; stakeholder approvals; Self-Assessment; Review Form; Charter | ADO; SNOW TMM; G&QM SharePoint |
| PRC.TS.06 | Test Plan Approval | Plan | Sponsors; App/Product Owners | Key | Formal approval prior to execution | Test Requirements; Traceability Approach; Schedule/Effort; Methodologies; Domains; Tech & Tooling; documented approvals | ADO; SNOW TMM |

## Artefact → Area Map
| Artefact | Area | Related Controls |
|---|---|---|
| Testing Scope | Requirements Analysis; Strategy | PRC.TS.01, PRC.TS.02, PRC.TS.03, PRC.TS.04 |
| Acceptance Criteria | Requirements Analysis | PRC.TS.01, PRC.TS.02 |
| Definition of Done (Testing) | Requirements Analysis | PRC.TS.01, PRC.TS.02 |
| Estimates (Testing) | Requirements Analysis; Plan | PRC.TS.01, PRC.TS.02, PRC.TS.05, PRC.TS.06 |
| Change Impact Analysis | Requirements Analysis | PRC.TS.01, PRC.TS.02 |
| Test Approach/Processes/Methodology | Strategy; Plan | PRC.TS.03, PRC.TS.04, PRC.TS.05, PRC.TS.06 |
| Infrastructure | Strategy; Plan | PRC.TS.03, PRC.TS.04, PRC.TS.05, PRC.TS.06 |
| Test Data Management | Strategy | PRC.TS.03, PRC.TS.04 |
| Defect Management | Strategy; Execution governance | PRC.TS.03, PRC.TS.04 |
| Automation | Strategy; Execution | PRC.TS.03, PRC.TS.04 |
| Reporting & Communication | Strategy; Execution | PRC.TS.03, PRC.TS.04 |
| Traceability Approach | Plan | PRC.TS.05, PRC.TS.06 |
| Schedule & Effort | Plan | PRC.TS.05, PRC.TS.06 |
| Methodologies, Domains, Tech & Tooling | Plan | PRC.TS.05, PRC.TS.06 |
| Stakeholder Approvals | Plan | PRC.TS.05, PRC.TS.06 |
| G&QM Review Form; Charter; Self-Assessment | Governance & QM | PRC.TS.01, PRC.TS.03, PRC.TS.05 |

## Placement Guidance (Repositories)
| Repository | What to Store | Area | Controls |
|---|---|---|---|
| ADO Boards/Wikis | Strategy docs; Plan docs; links to work items | Strategy; Plan | PRC.TS.03–06 |
| SNOW TMM | Approval records; test case libraries | Strategy; Plan; Execution | PRC.TS.02, PRC.TS.04, PRC.TS.06 |
| SharePoint (G&QM) | Review forms; charters; self-assessments; escalated events | Governance & QM | PRC.TS.01, PRC.TS.03, PRC.TS.05 |

## Standards 1–6 (from screenshots)
| Standard | Focus | Area | Related Controls |
|---|---|---|---|
| S1 | Strategy completeness (scope, approach) | Strategy | PRC.TS.03, PRC.TS.04 |
| S2 | Strategy methodology/process | Strategy | PRC.TS.03, PRC.TS.04 |
| S3 | Plan traceability and structure | Plan | PRC.TS.05, PRC.TS.06 |
| S4 | Plan infra and scheduling | Plan | PRC.TS.05, PRC.TS.06 |
| S5 | Execution governance (defects, automation) | Execution | (post-approval execution) |
| S6 | Reporting & communication | Execution | (post-approval execution) |

## Assignment Rules (Quick Reference)
| If the artefact… | Put under Area | Controls |
|---|---|---|
| Describes how we test (approach, methodology, infra, data, automation, reporting) | Strategy | PRC.TS.03, PRC.TS.04 |
| Defines what/when we test (requirements, traceability, schedule/effort, domains, tech/tooling) | Plan | PRC.TS.05, PRC.TS.06 |
| Records independent review/feedback | Governance & QM | PRC.TS.01, PRC.TS.03, PRC.TS.05 |
| Records formal approval | Plan/Strategy (as applicable) | PRC.TS.02, PRC.TS.04, PRC.TS.06 |
| Shows testing done/results/issues | Execution | (execution artefacts; typically PRC.TS.07+ in extended catalog) |

Notes:
- Typos in CSV (e.g., “plants”, “desumentation”) are preserved in source but normalized here for clarity in table names.
- Tables are designed for presentation; cells with multiple items use semicolons for compact readability.