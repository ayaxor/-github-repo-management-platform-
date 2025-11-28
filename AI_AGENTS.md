
# QuietWire – AI Agents Specification  
Prepared by: Eng. Aya Jamal  
Reviewed by: Ashraf Al-Haj – System Architect / Master Archivist  

---

## 1. Overview  
QuietWire uses a distributed AI-agent model to ensure documentation health, repo integrity, evidence traceability, and lifecycle automation.

This document defines:
- Agent roles  
- Operational behavior  
- Canon rules  
- Collaboration patterns  
- Attestation responsibilities  

---

## 2. Agents  
QuietWire currently uses **three core agents** and **worker bots**:

### 2.1 Athena  
Role: Documentation / Review / Structural Analysis  
Responsibilities:
- Scans repository for missing docs  
- Enforces structural consistency  
- Generates PR suggestions  
- Maintains architecture alignment  
- Helps contributor (Aya) during development  

---

### 2.2 QueenBee  
Role: Planning / Global State / Coordination  
Responsibilities:
- Oversees multi-repo consistency  
- Maintains platform-wide patterns  
- Ensures governance rules match Canon  
- Syncs workflows across repos  

---

### 2.3 Raasid  
Role: Evidence / Ledger / Attestation Integrity  
Responsibilities:
- Monitors CI logs, test results, SBOM  
- Packages evidence into CAP format  
- Creates ledger entries  
- Ensures traceability & compliance  
- Protects integrity of attestations folder  

---

### 2.4 Worker Bots  
Scoped task automation:
- Linting  
- Code formatting  
- Diagram integrity check  
- Test execution  
- Static analysis  

These bots never modify governance files.

---

## 3. AI Operational Workflow Diagram (ASCII)

+--------------------------------------+ |       AI Agent Operational Flow      | +--------------------------------------+ | v +--------------------------------------+ | 1. Athena scans repo structure & docs| +--------------------------------------+ | v +--------------------------------------+ | 2. Detects gaps (missing docs/tests)| +--------------------------------------+ | v +--------------------------------------+ | 3. Generates suggestions & templates | +--------------------------------------+ | v +--------------------------------------+ | 4. Opens PR (never commits directly)| +--------------------------------------+ | v +--------------------------------------+ | 5. Raasid collects CI evidence       | |    (logs, SBOM, tests, approvals)    | +--------------------------------------+ | v +------------------------------------------------+ | 6. Ledger entry created (CAP → Ledger align)   | +------------------------------------------------+

---

## 4. Canon Rules for AI Agents

✔ Agents never commit directly to main  
✔ All changes flow through PRs  
✔ Evidence must be exported before merge  
✔ Attestations are immutable  
✔ Ledger entries cannot be modified manually  
✔ AI agents cannot bypass governance rules  

---

## 5. Collaboration Model  
- Athena assists Aya during development  
- QueenBee aligns repo with global patterns used by Ashraf  
- Raasid safeguards compliance and traceability  
- Worker bots ensure cleanliness and code health  
- System Architect (Ashraf) performs the **final review**  

---

## 6. Maintainers  
**Eng. Aya Jamal** – Maintainer & Documentation Lead  
**Ashraf Al-Haj** – System Architect / Final Reviewer


---
