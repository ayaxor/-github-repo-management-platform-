
# QuietWire Repository Structure  
Canonical Folder Layout & Standards  
Prepared by: Eng. Aya Jamal  
Reviewed by: Ashraf Al-Haj – System Architect  

---

## 1. Purpose  
This document defines the **canonical folder structure** used across all QuietWire repositories.  
It ensures consistency, auditability, and clean integration with workflows, AI agents, and attestation systems.

---

## 2. High-Level Structure Diagram (ASCII)

QuietWire Repository (root) │ ├── docs/                ← Architectural & workflow documentation │   ├── ARCHITECTURE.md │   ├── REPO_STRUCTURE.md │   ├── AI_AGENTS.md │   ├── FLOW_OVERVIEW.md │   └── EVIDENCE_SPEC.md │ ├── src/                 ← Source code / modules │   ├── core/ │   ├── components/ │   └── utils/ │ ├── config/              ← Configuration files │   ├── settings/ │   └── environments/ │ ├── attestations/        ← Evidence + Ledger Zone │   ├── events/ │   └── ledger/ │ ├── templates/           ← Issue / PR / Release templates │   ├── ISSUE_TEMPLATE.md │   ├── PR_TEMPLATE.md │   └── RELEASE_TEMPLATE.md │ ├── .github/ │   └── workflows/       ← CI/CD pipelines │       ├── ci.yml │       ├── lint.yml │       ├── security.yml │       └── attest.yml │ └── README.md            ← Public-facing documentation

---

## 3. Directory Specifications

### 3.1 docs/  
Contains all enterprise documentation.  
AI agents (Athena / QueenBee) analyze this folder first.

Documents must follow QuietWire Canon:

- Clear headers  
- ASCII diagrams  
- Clean sections  
- No redundant text  

---

### 3.2 src/  
Main implementation zone of the repository.

Rules:
- No documentation-only files  
- No CI files  
- No attestation files  
- Organized by modules, not by features  

---

### 3.3 config/  
Repository configuration and environment-specific files.

Examples:

config/settings/ config/environments/dev.yml config/environments/prod.yml

---

### 3.4 attestations/  
Managed by **Raasid** and CI pipelines.  
Contains evidence needed for CAP → Ledger compliance.

Structure:

attestations/ events/   ← CAP human-readable ledger/   ← Machine integrity entries

---

### 3.5 templates/  
Standardized templates for the entire platform.

Required templates:
- ISSUE_TEMPLATE.md  
- PR_TEMPLATE.md  
- RELEASE_TEMPLATE.md  

All templates follow Canon formatting and include metadata fields.

---

### 3.6 .github/workflows/  
Contains all automation logic for:

- CI  
- Linting  
- Security scanning  
- Attestation exporting  

All workflows must:
- Enforce branch protection  
- Block commits with errors  
- Export evidence to attestations/  

---

### 3.7 README.md  
Public documentation of the repository.

Must include:
- Purpose  
- Architecture link  
- Workflow link  
- Maintainers  
- Contact information  

---

## 4. Canonical Rules

✔ No random folders  
✔ No files outside defined structure  
✔ No code in docs/  
✔ No docs in src/  
✔ All repos follow the same architecture  
✔ AI agents depend on this exact structure  

---

## 5. Maintainers  
**Eng. Aya Jamal** – Lead Maintainer  
**Ashraf Al-Haj** – System Architect / Final Reviewer


---
