# Testing Controls - Comprehensive Area Mapping & Control ID Logic

## Document Purpose
This document provides a clear, logical mapping of Testing Controls to their respective Areas, explaining the control ID structure, differentiation logic, and how to determine which control belongs to which area.

---

## Control ID Numbering Logic & Pattern

### Understanding the Control ID Structure: `PRC.TS.XX`

**Pattern Identification:**
- **PRC** = Process Control
- **TS** = Testing Standard
- **XX** = Sequential Number (01-21+)

### Control Type Differentiation by Number Pattern

**ODD Numbers (01, 03, 05, 07, etc.) → NON-KEY CONTROLS**
- Purpose: **Governance & Quality Management Reviews**
- Trigger: "Review for Escalated Major Events"
- Authority: SDLC G&QM Team
- Nature: Independent review/feedback before formal approval
- Repository: SDLC G&QM SharePoint

**EVEN Numbers (02, 04, 06, 08, etc.) → KEY CONTROLS**
- Purpose: **Formal Approvals & Execution Activities**
- Authority: Project Sponsors / Application-Product Owners / Testing Team
- Nature: Decision-making, approvals, execution
- Repository: ADO / SNOW TMM

---

## Complete Control-to-Area Mapping

### AREA 1: Test Requirement Analysis
**Phase:** Requirements Definition
**Focus:** What needs to be tested and why

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.01** | Test Requirements Analysis Review for Escalated Major Events | NON-KEY | SDLC G&QM | Independent review of testing scope, acceptance criteria, definition of done, estimates, change impact |
| **PRC.TS.02** | Test Requirements Analysis | KEY | Project Sponsors & App/Product Owners | Formal approval of test requirements before strategy development |

**Key Artifacts:**
- Testing Scope
- Acceptance Criteria  
- Definition of Done (Testing)
- Testing Estimates
- Change Impact Analysis
- G&QM Review Forms (for .01)
- Documented Approvals (for .02)

**Decision Logic:** "If it defines WHAT to test and WHY" → Area 1

---

### AREA 2: Test Strategy Development
**Phase:** Strategic Planning
**Focus:** HOW testing will be conducted (approach, methodology, infrastructure)

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.03** | Test Strategy Review for Escalated Major Events | NON-KEY | SDLC G&QM | Independent review of testing approach, processes, methodology, infrastructure, data management, defect management, automation, reporting |
| **PRC.TS.04** | Test Strategy Development | KEY | Project Sponsors & App/Product Owners | Formal approval of test strategy before plan development |

**Key Artifacts:**
- Testing Scope (strategic view)
- Test Approach
- Test Processes and Methodology
- Test Infrastructure
- Test Data Management
- Defect Management Strategy
- Testing Automation Strategy
- Reporting and Communication Plan
- G&QM Review Forms (for .03)
- Documented Approvals (for .04)

**Decision Logic:** "If it describes HOW to test (approach, method, tools)" → Area 2

---

### AREA 3: Test Plan Development
**Phase:** Detailed Planning
**Focus:** WHEN and with WHAT resources testing will happen

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.05** | Test Plan Review for Escalated Major Events | NON-KEY | SDLC G&QM | Independent review of test requirements, approach, traceability, infrastructure, schedule, methodologies, domains, technology |
| **PRC.TS.06** | Test Plan Development | KEY | Project Sponsors & App/Product Owners | Formal approval of detailed test plan before execution |

**Key Artifacts:**
- Test Requirements (detailed)
- Test Approach and Processes
- Test Traceability Approach
- Test Infrastructure (detailed)
- Test Schedule and Effort
- Testing Methodologies
- Testing Domains
- Testing Technology and Tooling
- Stakeholder Approvals
- G&QM Review Forms (for .05)
- Documented Approvals (for .06)

**Decision Logic:** "If it details WHEN to test and SCHEDULES/RESOURCES" → Area 3

---

### AREA 4: Test Design Development
**Phase:** Design & Preparation
**Focus:** Creating test cases, scenarios, and test data

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.07** | Test Design Development | KEY | Testing Team | Creation and documentation of test cases, scenarios, test data |

**Key Artifacts:**
- Test Cases
- Test Scenarios
- Test Data Sets
- Test Scripts
- Expected Results Documentation

**Decision Logic:** "If it involves creating test cases and scenarios" → Area 4

---

### AREA 5: Test Environment Configuration
**Phase:** Environment Setup
**Focus:** Setting up and managing test environments

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.08** | Test Environment Separation | KEY | Infrastructure Team | Ensuring proper environment isolation |
| **PRC.TS.09** | Test Environment Configuration | KEY | Infrastructure Team | Configuring test environments to match requirements |
| **PRC.TS.10** | Test Environment Configuration Exceptions | KEY | Infrastructure Team / G&QM | Managing approved exceptions to standard configurations |

**Key Artifacts:**
- Environment Setup Documentation
- Environment Topology Diagrams
- Access Control Lists
- Environment Equivalence Documentation
- Exception Requests and Approvals (for .10)

**Decision Logic:** "If it involves setting up or configuring test environments" → Area 5

---

### AREA 6: Minimum Testing Requirements
**Phase:** Compliance & Standards
**Focus:** Ensuring minimum testing standards are met

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.11** | Minimum Testing Requirements | KEY | Testing Governance | Ensuring minimum testing criteria are met per program type |
| **PRC.TS.19** | Minimum Testing Requirements Annual Review | KEY | Testing Governance | Annual review and update of minimum testing standards |

**Key Artifacts:**
- Minimum Testing Standards Documentation
- Testing Coverage Reports
- Program Type Classification
- Annual Review Reports (for .19)

**Decision Logic:** "If it ensures minimum standards compliance" → Area 6

---

### AREA 7: Test Execution and Results
**Phase:** Execution
**Focus:** Conducting tests and documenting results

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.12** | Testing Execution and Results Review for Escalated Major Events | NON-KEY | SDLC G&QM | Independent review of test execution and results |
| **PRC.TS.13** | Testing Execution and Results | KEY | Testing Team | Executing tests and documenting results |

**Key Artifacts:**
- Test Execution Logs
- Test Results Reports
- Test Coverage Reports
- Pass/Fail Status
- Environment Usage Summary
- Defect Summary
- G&QM Review Forms (for .12)

**Decision Logic:** "If it involves running tests and recording results" → Area 7

---

### AREA 8: Testing Defect Remediation
**Phase:** Issue Management
**Focus:** Managing and resolving testing defects

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.14** | High/Critical Testing Defect Remediation Review for Escalated Major Events | NON-KEY | SDLC G&QM | Review of high/critical defect resolution approach |
| **PRC.TS.15** | High/Critical Testing Defect Remediation | KEY | Development Team | Resolution of high/critical severity defects |
| **PRC.TS.16** | Medium/Low Testing Defect Remediation Review for Escalated Major Events | NON-KEY | SDLC G&QM | Review of medium/low defect resolution approach |
| **PRC.TS.17** | Medium/Low Testing Defect Remediation | KEY | Development Team | Resolution of medium/low severity defects |

**Key Artifacts:**
- Defect Reports
- Defect Remediation Plans
- Root Cause Analysis
- Retest Results
- Defect Metrics
- G&QM Review Forms (for .14, .16)

**Decision Logic:** "If it involves fixing or reviewing defects" → Area 8

---

### AREA 9: Vendor Testing Evidence
**Phase:** Third-Party Validation
**Focus:** Managing testing evidence from external vendors

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.19** | Vendor Testing Evidence | KEY | Vendor Management / Testing Team | Collection and validation of testing evidence from vendors |

**Key Artifacts:**
- Vendor Test Reports
- Third-Party Certifications
- Vendor Testing Documentation
- Evidence Validation Records

**Decision Logic:** "If it involves third-party/vendor testing validation" → Area 9

---

### AREA 10: Data Protection and Security Exceptions
**Phase:** Security & Compliance
**Focus:** Managing exceptions to data protection and security requirements

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.20** | Data Protection and Security Exceptions Request | KEY | Security Team / Testing Team | Managing approved exceptions for test data and security |

**Key Artifacts:**
- Exception Request Forms
- Risk Assessments
- Approval Documentation
- Compensating Controls Documentation

**Decision Logic:** "If it involves data security exceptions during testing" → Area 10

---

### AREA 11: Vulnerability Remediation
**Phase:** Security Testing
**Focus:** Managing security vulnerabilities found during testing

| Control ID | Control Name | Type | Responsible Party | Key Activity |
|------------|--------------|------|-------------------|--------------|
| **PRC.TS.21** | Vulnerability Remediation | KEY | Security Team / Development Team | Resolution of security vulnerabilities identified |

**Key Artifacts:**
- Vulnerability Scan Reports
- Penetration Test Results
- Remediation Plans
- Vulnerability Closure Reports

**Decision Logic:** "If it involves security vulnerability management" → Area 11

---

## Control Placement Decision Tree

```
START: New Control Needs to be Classified
│
├─ Does it involve G&QM independent review?
│  ├─ YES → NON-KEY Control (Odd Number)
│  └─ NO → Continue
│
├─ Does it involve formal approval or execution?
│  ├─ YES → KEY Control (Even Number)
│  └─ NO → Re-evaluate control type
│
├─ What phase does it belong to?
│  ├─ Requirements → Area 1 (PRC.TS.01-02)
│  ├─ Strategy → Area 2 (PRC.TS.03-04)
│  ├─ Planning → Area 3 (PRC.TS.05-06)
│  ├─ Design → Area 4 (PRC.TS.07)
│  ├─ Environment → Area 5 (PRC.TS.08-10)
│  ├─ Standards → Area 6 (PRC.TS.11, 19)
│  ├─ Execution → Area 7 (PRC.TS.12-13)
│  ├─ Defects → Area 8 (PRC.TS.14-17)
│  ├─ Vendor → Area 9 (PRC.TS.19)
│  ├─ Security Exception → Area 10 (PRC.TS.20)
│  └─ Vulnerability → Area 11 (PRC.TS.21)
```

---

## Repository Placement Guide

### ADO (Azure DevOps) / SNOW TMM
**Use for:** KEY Controls (Even Numbers)
- Formal approvals
- Test plans and strategies
- Test execution records
- Defect tracking

### SDLC G&QM SharePoint
**Use for:** NON-KEY Controls (Odd Numbers)
- Review forms
- Charters
- Self-assessments
- Escalated events documentation

---

## Testing Lifecycle Flow with Controls

```
Phase 1: Requirements
  ↓ PRC.TS.01 (G&QM Review)
  ↓ PRC.TS.02 (Formal Approval)
  
Phase 2: Strategy  
  ↓ PRC.TS.03 (G&QM Review)
  ↓ PRC.TS.04 (Formal Approval)
  
Phase 3: Planning
  ↓ PRC.TS.05 (G&QM Review)
  ↓ PRC.TS.06 (Formal Approval)
  
Phase 4: Design
  ↓ PRC.TS.07 (Test Design Creation)
  
Phase 5: Environment Setup
  ↓ PRC.TS.08 (Environment Separation)
  ↓ PRC.TS.09 (Environment Configuration)
  ↓ PRC.TS.10 (Exception Management)
  
Phase 6: Execution
  ↓ PRC.TS.11 (Minimum Standards Check)
  ↓ PRC.TS.12 (G&QM Review of Execution)
  ↓ PRC.TS.13 (Test Execution)
  
Phase 7: Issue Management
  ↓ PRC.TS.14 (G&QM Review High/Critical Defects)
  ↓ PRC.TS.15 (High/Critical Defect Remediation)
  ↓ PRC.TS.16 (G&QM Review Medium/Low Defects)
  ↓ PRC.TS.17 (Medium/Low Defect Remediation)
  
Parallel/Continuous:
  → PRC.TS.19 (Vendor Evidence)
  → PRC.TS.20 (Security Exceptions)
  → PRC.TS.21 (Vulnerability Remediation)
```

---

## Quick Reference: Control ID Assignment Logic

| If the control is about... | Assign to Area | Use Control ID Range |
|----------------------------|----------------|---------------------|
| Defining test scope and requirements | Test Requirement Analysis | PRC.TS.01-02 |
| Testing approach and methodology | Test Strategy Development | PRC.TS.03-04 |
| Detailed scheduling and planning | Test Plan Development | PRC.TS.05-06 |
| Creating test cases | Test Design Development | PRC.TS.07 |
| Setting up test environments | Test Environment Configuration | PRC.TS.08-10 |
| Ensuring minimum standards | Minimum Testing Requirements | PRC.TS.11, 19 |
| Running tests | Test Execution and Results | PRC.TS.12-13 |
| Fixing defects | Testing Defect Remediation | PRC.TS.14-17 |
| Vendor testing | Vendor Testing Evidence | PRC.TS.19 |
| Test data security exceptions | Data Protection Exceptions | PRC.TS.20 |
| Security vulnerabilities | Vulnerability Remediation | PRC.TS.21 |

---

## Notes & Guidelines

1. **Escalated Major Events:** These are events identified through risk assessment that require additional G&QM oversight
   
2. **Review vs Approval:**
   - **Review (Odd #):** Independent assessment by G&QM team, provides feedback
   - **Approval (Even #):** Decision-making authority, must approve before proceeding

3. **Sequential Nature:** Controls generally follow the testing lifecycle sequence in their numbering

4. **Exception Handling:** Some controls (like PRC.TS.19) appear multiple times as they serve different purposes in different areas

5. **Risk-Based Application:** Not all controls apply to all projects - application is based on risk and impact assessment

---

## Document Version Control

- **Version:** 1.0
- **Date:** November 12, 2025
- **Purpose:** Provide clear control-to-area mapping logic for testing governance
- **Source:** Based on SDAM Testing Standards and Quality Engineering Practice Framework
