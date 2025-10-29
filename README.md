# Governance Service Management — Compliance Demo

This repository hosts a lightweight, automation-ready demo focused on the compliance core of the cricket process flow. It demonstrates how to validate evidence against mapped controls and produce structured outputs that can be consumed by ServiceNow, SharePoint, Teams, or other systems.

## Contents
- `docs/lld_flow.html` — Interactive LLD flow diagram of the end-to-end process.
- `docs/validator_demo.html` — MVP web demo for compliance validation.
- `docs/mapping.json` — Sample controls→evidence mapping used by the demo.

## Quick Start
- Local preview (from the parent folder):
  - `python3 -m http.server 8000`
  - Open `http://localhost:8000/governance_ServiceMgnt/docs/validator_demo.html`
- Diagram preview:
  - `http://localhost:8000/governance_ServiceMgnt/docs/lld_flow.html`

## Validator Demo: What It Does
- Paste relevant document text (e.g., Test Plan/Strategy/Review Form) into the demo.
- Click `Run Validation` to check keywords/sections against `mapping.json`.
- Outputs:
  - `Export JSON` — Structured compliance result with `meta`, `summary`, and per-control details.
  - `Download CSV` — Flat table for quick review or ingestion.
  - `Copy ServiceNow Payload` — Compact object ready to post to ServiceNow via Record Producer or Scripted REST.
- Metadata inputs (top of the page):
  - `ProjectId`, `ChangeId`, `Ticket` — Used to tie a run to a ServiceNow record.

## JSON Structure
The JSON export and ServiceNow payload are built from the same core structure:
- `meta`:
  - `projectId`, `changeId`, `ticketNumber`, `runTimestamp`
- `summary`:
  - `totalControls`, `fully`, `partial`, `missing`
- `controls[]` (for each control):
  - `id`, `name`, `type`, `status` (`Fully Compliant` | `Partially Compliant` | `Missing Evidence`), `score` (0–1)
  - `evidence[]` → `{ name, found }`
  - `elements[]` → `{ name, found }`
  - `expectedSections[]` — guidance from mapping

## Mapping File Overview (`docs/mapping.json`)
- Top-level metadata: `projectId`, `changeId`
- `controls[]`:
  - `id`, `name`, `type`
  - `requiredEvidence[]`: each item with `name` and `keywords[]`
  - `controlElements[]`: expected elements/phrases to match
  - `documentSections[]`: optional guidance for expected sections

You can extend `mapping.json` to reflect your compliance framework, project taxonomy, and document structure.

## ServiceNow Integration (Example)
- Payload fields (`Copy ServiceNow Payload`):
  - `ticket_number`, `project_id`, `change_id`, `run_timestamp`, `summary`, `controls`
- Options:
  - Record Producer (portal) → create a “Compliance Run” record.
  - Scripted REST API → `POST` payload into a scoped table.
  - Flow Designer → receive payload, persist data, attach CSV/JSON to a ticket, notify via Teams/Email.
- Suggested minimal table schema:
  - Parent: `u_compliance_run` with `u_ticket_number`, `u_project_id`, `u_change_id`, `u_run_timestamp`, `u_summary_json`
  - Child: `u_compliance_control` with `u_run` (ref), `u_control_id`, `u_status`, `u_score`, `u_evidence_json`, `u_elements_json`

## GitHub Pages (Optional)
To publish `docs/*` via GitHub Pages:
- In GitHub → Settings → Pages → Source: select `main` and `/root` or `/docs`.
- The pages URL will be shown after enabling. You can then access `validator_demo.html` and `lld_flow.html` directly online.

## Production Path
- Replace simple keyword matching with robust parsing (SharePoint Syntex, Graph, Azure Document Intelligence).
- Automate triggers from ServiceNow on ticket creation/update (Flow Designer or webhooks).
- Persist results to SharePoint lists or ServiceNow tables; post Teams Adaptive Cards for reviewer approval.
- Add error handling, audit logs, retention/versioning in SharePoint.

## Notes
- The MVP focuses on compliance output quality and automation readiness.
- All outputs are self-contained (JSON/CSV) to make integration straightforward.
- Local server is sufficient to test the demo; no backend required.