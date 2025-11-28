
# QuietWire – Canon Rules  
Prepared by: Eng. Aya Jamal  
Reviewed by: Ashraf Al-Haj – System Architect / Master Archivist  

---

## 1. Introduction  
The **Canon** is the master set of rules that govern all QuietWire repositories.

It defines:
- How repos must be structured  
- How workflows must operate  
- How documentation must look  
- How evidence and attestation must be handled  
- How AI agents must behave  
- How consistency across the entire ecosystem is maintained  

This document describes the **unbreakable standards** required for QuietWire.

---

## 2. Canon Philosophy  
The Canon ensures:

✔ Predictability  
✔ Readability  
✔ Auditability  
✔ Traceability  
✔ AI compatibility  
✔ Engineering integrity  
✔ Enterprise structure  

Nothing inside a QuietWire repo is random.  
Everything follows Canon.

---

## 3. Canon Rule Groups

### 3.1 Structural Rules  
These rules define how the repository MUST be organized.

✔ docs/ folder mandatory  
✔ .github/workflows/ mandatory  
✔ attestations/ mandatory  
✔ templates/ recommended  
✔ README must exist  
✔ No random folders allowed  
✔ No duplication of docs  
✔ All files must serve a clear function  

---

### 3.2 Documentation Rules  
✔ All docs must follow QuietWire formatting  
✔ Sections must be clear and labeled  
✔ Diagrams must be ASCII or Mermaid (if supported)  
✔ English is primary documentation language  
✔ Arabic/French/Spanish optional mirrors  
✔ No long paragraphs without structure  
✔ All docs must be AI-friendly  

---

### 3.3 Governance Rules  
✔ No direct commits to `main`  
✔ All changes flow through PRs  
✔ Every PR must reference an Issue  
✔ CI must pass before merging  
✔ Review from Aya and/or Ashraf is mandatory  
✔ Protected branches must remain protected  
✔ No bypassing governance through automation  

---

### 3.4 Attestation Rules  
✔ Every merge → evidence must be collected  
✔ Every release → must generate CAP event  
✔ Attestations must be stored under `attestations/`  
✔ Ledger entries are immutable  
✔ Evidence must reference PR & commit SHA  
✔ No manual editing of evidence folders  

---

### 3.5 AI Agent Behavior Rules  
✔ Athena may analyze and suggest  
✔ QueenBee may coordinate globally  
✔ Raasid must generate ledger entries  
✔ Worker bots perform scoped tasks  
✔ No AI agent commits directly to `main`  
✔ AI must open PRs for all changes  
✔ AI actions must be logged and referenced  

---

### 3.6 Naming Rules  
✔ Branches must follow:

feature/<name> hotfix/<name> docs/<name>

✔ Files must use lowercase  
✔ No spaces in folder/file names  
✔ Use hyphens `-` for spacing  
✔ Timestamps must be UTC format  
✔ Attestation folders use YYYY-MM-DD  

---

### 3.7 Repository Identity Rules  
Every QuietWire repo must have:

- README.md  
- Architecture file (ARCHITECTURE.md)  
- Workflow file (WORKFLOW_OVERVIEW.md / PLAYBOOK)  
- Evidence spec  
- Attestation model  
- AI agents spec  
- Governance rules  
- Security file  
- Changelog  
- Labels file  
- Proper folder structure  

If a repo misses any required element →  
**It is not Canon-compliant.**

---

## 4. Canon Enforcement  
Canon is enforced by:

### ✔ Aya (Maintainer)  
- Ensures files & structure are correct  
- Maintains documentation quality  
- Rejects non-compliant PRs  
- Works with Athena for corrections  

### ✔ Ashraf (System Architect)  
- Final reviewer  
- Oversees Canon evolution  
- Approves exceptions  
- Maintains architectural purity  

### ✔ AI Agents  
- Athena: checks structure  
- QueenBee: checks ecosystem alignment  
- Raasid: ensures attestation compliance  

---

## 5. Canon Guarantees  
Following these rules ensures:

✔ Predictable repo behavior  
✔ Fast onboarding  
✔ AI-friendly analysis  
✔ Perfect auditability  
✔ Ledger traceability  
✔ Enterprise readiness  

---

## 6. Maintainers  
**Eng. Aya Jamal** – Canon Compliance Lead  
**Ashraf Al-Haj** – System Architect / Final Reviewer


---
