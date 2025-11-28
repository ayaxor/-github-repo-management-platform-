
# 📝 QuietWire – Code Review Guidelines  
Prepared by: Eng. Aya Jamal  
Reviewed by: Ashraf Al-Haj – System Architect & Final Reviewer  

---

## 1. Purpose  
This document defines the **code review standards** used across all QuietWire, CAP, and Canon repositories.

The goal is to ensure:
- High-quality code  
- Consistent structure  
- Governance compliance  
- Security protection  
- Evidence integrity  
- Clean collaboration between humans + AI agents  

---

## 2. Review Requirements

### ✔ All PRs MUST follow:
- Linked Issue  
- PR Template  
- Proper labels  
- Passing CI/CD  
- No direct commits to `main`  
- No missing documentation  

---

## 3. Review Checklist (Aya + Reviewers)

### 🔹 **A. Functionality**
- Does the code work as intended?  
- Does it break any existing features?  
- Are tests included and passing?  

### 🔹 **B. Readability**
- Clean, clear, and easy to understand  
- Good variable naming  
- No unnecessary complexity  

### 🔹 **C. Structure**
- Files placed in correct folder  
- Template rules respected  
- Canon structure alignment  

### 🔹 **D. Documentation**
- README updated  
- Function comments included  
- Architecture updates reflected (if needed)  

### 🔹 **E. Security**
- No secrets  
- No sensitive data  
- No vulnerabilities introduced  
- Permissions safe  

### 🔹 **F. Evidence**
- CI logs exported  
- Test results valid  
- Attestation ready for CAP/Ledger  

---

## 4. Review Flow (Step-by-Step)

1. Contributor opens PR


2. Athena scans structure + documentation


3. Worker Bots run CI/CD


4. Raasid validates evidence


5. Aya reviews


6. Ashraf reviews (critical repos)


7. Merge → Release → CAP Event → Ledger Entry



---

## 5. Reviewer Responsibilities

### **Aya (Maintainer)**
- Primary reviewer  
- Enforces Canon + governance rules  
- Ensures documentation completeness  
- Blocks insecure PRs  
- Approves final merge (except critical repos)

### **Ashraf (Architect)**
- Final reviewer for all core repos  
- Ensures architectural correctness  
- Validates attestation logic  
- Signs off major changes  

### **Athena (AI Agent)**
- Structural and documentation analyzer  
- Template enforcement  

### **Raasid**
- Evidence validator  
- Ledger chain integrity  

---

## 6. Common Review Failures

| Failure | Reason | Fix |
|---------|--------|------|
| Missing tests | Code not validated | Add tests |
| Wrong folder | Structure deviation | Move files |
| CI failed | Errors in code/tests | Fix errors |
| Documentation missing | Repo incomplete | Update docs |
| Security issue | Vulnerability or secret | Patch immediately |

---

## 7. Review Labels

Use labels to classify PRs:

| Label | Meaning |
|--------|----------|
| type:feature | New feature |
| type:bug | Fix |
| type:security | Security-related change |
| type:docs | Documentation update |
| type:refactor | Structure cleanup |
| status:needs-review | Waiting for review |
| status:changes-requested | Fixes needed |
| status:approved | Ready to merge |

---

## 8. Review Timing

- Small PRs: **within 24h**  
- Medium PRs: **48h**  
- Large PRs / Architectural PRs: **72h**  

Critical PRs → Reviewed by **Aya + Ashraf** only.

---

## 9. Merge Rules

### ❌ Forbidden:
- No merge without passing CI  
- No merge without approval  
- No self-merge (except emergency hotfix)  
- No merge with warnings  
- No skipping evidence  

### ✔ Allowed only when:
- CI passes  
- Documentation updated  
- Governance rules applied  
- Evidence folder updated  
- CAP event ready  

---

## 10. Final Notes  
Code review is a **governance process**, not just a technical step.  
It protects:  
- QuietWire reputation  
- CAP reliability  
- Ledger integrity  
- Aya’s engineering standards  
- Ashraf’s architectural rules  

---

## 11. Status  
**Version:** v1.0  
**Maintainer:** Eng. Aya Jamal  
**Final Reviewer:** Ashraf Al-Haj


---
