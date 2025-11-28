
# 🧭 QuietWire – Governance Matrix  
Prepared by: Eng. Aya Jamal  
Reviewed by: Ashraf Al-Haj – System Architect  

---

## 1. Purpose  
This Governance Matrix defines **how decisions are made, who has authority, and how responsibilities are distributed** across QuietWire, CAP, Canon, and related repositories.

It ensures:
- Discipline  
- Structure  
- Accountability  
- Secure workflows  
- Transparent review cycles  

---

## 2. Governance Model Overview

┌───────────────────────────────┐ │     System Architect (Ashraf) │ └──────────────┬────────────────┘ │ oversees ┌──────────────▼────────────────┐ │         Maintainer (Aya)       │ └──────────────┬────────────────┘ │ coordinates ┌──────────────▼────────────────┐ │     Contributors & AI Agents   │ └────────────────────────────────┘

---

## 3. Governance Areas

### The system governs:
- Branch strategy  
- Issue lifecycle  
- Pull request rules  
- Documentation standards  
- AI agent permissions  
- CI/CD requirements  
- Release approvals  
- Attestation → CAP → Ledger  
- Repo structural consistency  
- Evidence quality  

---

## 4. RACI Governance Matrix  
*(R = Responsible • A = Accountable • C = Consulted • I = Informed)*

| Area | Aya | Ashraf | Contributor | Athena | Raasid | QueenBee |
|------|-----|---------|-------------|---------|---------|-----------|
| Repo Structure | R | A | C | R | I | C |
| Documentation | R | C | R | R | I | C |
| Code Review | R | A | C | C | I | C |
| Merge Approval | R | A | — | I | I | I |
| PR Creation | I | I | R | C | C | C |
| Architecture Updates | C | A | — | C | I | R |
| Attestation | C | A | — | I | R | C |
| Ledger Entry | I | A | — | I | R | C |
| Evidence Validation | C | A | — | I | R | I |
| Release Creation | R | A | — | I | I | C |
| Governance Enforcement | R | A | I | C | I | C |
| Security Policy | R | A | — | C | I | C |
| CI/CD | R | A | C | I | I | I |
| Risk Management | R | A | — | C | I | C |

---

## 5. Authority Levels

### **Highest Authority — Ashraf**
- Architecture  
- Canon standards  
- Attestation logic  
- Critical merges  
- Final approval on releases  

### **Operational Authority — Aya**
- Daily governance enforcement  
- CI validation  
- PR approvals  
- Repo structure and sanity  
- Communication with agents  

### **Contributor Authority**
- Create Issues  
- Open PRs  
- Suggest improvements  

### **AI Agent Authority**
- Athena → structure / docs  
- Raasid → evidence / ledger  
- QueenBee → high-level orchestration  
- Worker bots → lint/test/build  

**All AI agents must ALWAYS be reviewed by Aya or Ashraf.**

---

## 6. Governance Rules

### 🔹 Rule 1 — Protected Branches
- `main` locked  
- No direct commits  
- All changes go through PRs  

### 🔹 Rule 2 — Mandatory Reviews
- Aya review  
- Ashraf review for core repos  

### 🔹 Rule 3 — Issue Linking
PR **must** reference Issue:

Fixes #123

### 🔹 Rule 4 — Evidence Requirements
Every merge requires:
- CI logs  
- Test results  
- SBOM  
- Attestation  

### 🔹 Rule 5 — Documentation Enforcement
Missing docs = PR reject.

---

## 7. Governance Flow Diagram

Contributor → PR → Athena → CI → Raasid → Aya → Ashraf → Merge → Release → CAP → Ledger

---

## 8. Non-Compliance Handling

| Violation | Action |
|-----------|---------|
| Direct commit to main | PR rollback + warning |
| Missing documentation | Reject PR |
| No evidence | Block merge |
| Failed CI | Reject PR |
| Misaligned architecture | Full review by Ashraf |
| Ledger mismatch | Hotfix + attestation review |

---

## 9. Status  
**Version:** v1.0  
**Maintainer:** Eng. Aya Jamal  
**Reviewer:** Ashraf Al-Haj
