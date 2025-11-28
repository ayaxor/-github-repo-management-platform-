
# 👥 QuietWire – Contributor Roles & Responsibilities  
Prepared by: Eng. Aya Jamal  
Reviewed by: Ashraf Al-Haj – System Architect  

---

## 1. Purpose
This document defines the **roles, responsibilities, and permissions** of every participant in the QuietWire, CAP, and Canon GitHub ecosystem.

It ensures:
- Clear division of responsibilities  
- Proper governance  
- Accountability  
- Transparent workflows  
- Secure usage of repositories  

---

## 2. Role Categories

┌─────────────────────────────────┐ │        System Architect         │ │            (Ashraf)             │ └─────────────────────────────────┘ │ ▼ ┌─────────────────────────────────┐ │            Maintainer           │ │            (Aya)                │ └─────────────────────────────────┘ │ ▼ ┌─────────────────────────────────┐ │            Contributors          │ │      (Developers, Interns)       │ └─────────────────────────────────┘ │ ▼ ┌─────────────────────────────────┐ │            AI Agents             │ │ Athena • Raasid • QueenBee • Bots│ └─────────────────────────────────┘

---

## 3. Full Role Definitions

### ⭐ **1. System Architect (Ashraf Al-Haj)**  
Highest authority in QuietWire GitHub operations.

Responsibilities:
- Approves global architecture  
- Reviews critical PRs  
- Defines Canon & CAP standards  
- Validates attestation logic  
- Ensures full compliance across all repos  
- Signs off final releases  

Permissions:
- Admin on core repos  
- Final reviewer  
- Merge authority for critical branches  

---

### ⭐ **2. Maintainer (Eng. Aya Jamal)**  
Primary engineer responsible for day-to-day repository management.

Responsibilities:
- Enforce governance rules  
- Review and merge PRs  
- Maintain repo structure  
- Ensure CI/CD remains operational  
- Ensure documentation completeness  
- Coordinate with AI agents  
- Validate alignment with architecture  

Permissions:
- Approve PRs  
- Manage labels  
- Manage templates  
- Open architecture changes (with approval)  
- Trigger releases  

---

### ⭐ **3. Contributors (Developers / Interns)**

Responsibilities:
- Implement features  
- Fix bugs  
- Write documentation  
- Follow templates & structure rules  
- Provide evidence  
- Use Issues for all work  

Permissions:
- Create branches  
- Open PRs  
- Comment & suggest  

Limitations:
- Cannot merge PRs  
- Cannot push to `main`  
- Cannot modify governance files  

---

### ⭐ **4. AI Agents**

#### 🤖 **Athena**
- Structural analysis  
- Documentation enforcement  
- Suggests improvements  

#### 🤖 **Raasid**
- Evidence validator  
- Ledger alignment  
- Handles CAP integration  

#### 🤖 **QueenBee**
- Orchestration + planning  
- Cross-repo coordination  

#### 🤖 **Worker Bots**
- Testing  
- Linting  
- Security checks  

**All AI agents:**
- Cannot merge PRs  
- Cannot push directly  
- Must create PRs only  
- Must log all actions  

---

## 4. RACI Matrix (Roles Map)

| Task | Aya | Ashraf | Contributor | AI Agents |
|------|-----|---------|-------------|-----------|
| Create Issues | R | C | R | C |
| Open PRs | R | C | R | R |
| Review PRs | R | A | C | C |
| Merge PRs | R | A | — | — |
| Update Architecture | C | A | — | C |
| Evidence Validation | C | A | — | R (Raasid) |
| Documentation QA | R | C | — | R (Athena) |
| Governance Rules | R | A | — | C |
| Release Creation | R | A | — | C |
| Ledger Entry | C | A | — | R (Raasid) |

**A = Accountable | R = Responsible | C = Consulted**

---

## 5. Code of Conduct
All contributors must:
- Follow Canon rules  
- Respect repo structure  
- Provide complete PR descriptions  
- Never bypass CI/CD  
- Maintain professional collaboration  

---

## 6. Status
**Version:** v1.0  
**Maintainer:** Eng. Aya Jamal  
**Reviewer:** Ashraf Al-Haj


---
