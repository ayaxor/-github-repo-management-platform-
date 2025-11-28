
# QuietWire – Security Model  
Prepared by: Eng. Aya Jamal  
Reviewed by: Ashraf Al-Haj – System Architect / Master Archivist  

---

## 1. Purpose  
This document defines the **security rules, policies, and protections** inside the QuietWire GitHub Repository Platform.

It ensures:
- No leaks  
- No unauthorized commits  
- No broken workflows  
- Full compliance with Canon governance  
- Protection of all sensitive assets  

---

## 2. Security Principles  

### ✔ Principle of Least Privilege  
Every user, workflow, and agent receives minimum permissions only.

### ✔ No Direct Commits to main  
All changes must go through PRs.

### ✔ No Secrets in Repos  
Never store:
- API keys  
- Passwords  
- Tokens  
- Credentials  
- Private data  

Secrets must ONLY be stored in:

GitHub → Settings → Secrets & Variables

### ✔ CI Safety  
All CI pipelines must:
- Run in isolated environments  
- Never expose secret values in logs  
- Export evidence safely  
- Follow Canon attestation rules  

---

## 3. Protected Branch Rules  

### main branch is protected:  
- No force-push  
- No direct commits  
- No merge without CI  
- No merge without review  
- PR must reference an Issue  

### develop branch (if used)  
- Must remain stable  
- No broken code allowed  
- Used for safe integration  

---

## 4. User Permission Levels  

| Role        | Permissions                                   |
|-------------|-----------------------------------------------|
| Admin       | Repo settings / secrets / protection rules     |
| Maintainer  | Approve PRs / enforce Canon / manage workflows |
| Contributor | Create PRs / Issues                            |
| Reader      | Read-only                                      |

**Eng. Aya Jamal = Maintainer**  
**Eng. Ashraf = System Architect (Final Reviewer)**

---

## 5. AI Agent Permissions  

### Athena  
- Can read everything  
- Can open PRs  
- Cannot merge  
- Cannot push directly

### QueenBee  
- Can access multiple repos  
- Ensures governance alignment  
- Cannot bypass protection

### Raasid  
- Can write to `attestations/`  
- Cannot modify ledger manually  
- Cannot overwrite human decisions  

### Worker Bots  
- Limited to linting / testing / formatting  

---

## 6. Security Workflow Diagram (ASCII)

+-----------------------------------------------------------+
|                 QUIETWIRE SECURITY WORKFLOW               |
+-----------------------------------------------------------+
                            |
                            v
+-----------------------------------------------------------+
| 1. Developer creates PR                                   |
+-----------------------------------------------------------+
                            |
                            v
+-----------------------------------------------------------+
| 2. CI pipeline runs                                       |
|    - Lint                                                 |
|    - Test                                                 |
|    - Security scan                                        |
+-----------------------------------------------------------+
                            |
                            v
+-----------------------------------------------------------+
| 3. Review required (Aya + Ashraf)                          |
|    - Governance rules checked                              |
|    - Canon compliance verified                             |
+-----------------------------------------------------------+
                            |
                            v
+-----------------------------------------------------------+
| 4. Merge only if:                                          |
|    - CI passed                                             |
|    - Review approved                                       |
|    - No security issues                                    |
+-----------------------------------------------------------+
                            |
                            v
+-----------------------------------------------------------+
| 5. Release created → Evidence exported                     |
+-----------------------------------------------------------+
                            |
                            v
+-----------------------------------------------------------+
| 6. CAP event + Ledger entry (immutable)                    |
+-----------------------------------------------------------+

---

## 7. Incident Response  

### If a security issue is discovered:
1. Report through `SECURITY.md` instructions  
2. Ashraf reviews severity  
3. Patch created under:

hotfix/security/<issue-id>

4. Evidence must be attached  
5. Ledger entry required  

---

## 8. Forbidden Actions  

❌ Storing secrets inside repo  
❌ Copying private keys  
❌ Direct commits to protected branches  
❌ Changing ledger entries manually  
❌ Bypassing CI pipeline  
❌ Removing evidence files  
❌ Disabling workflows  

Any violation breaks Canon.

---

## 9. Maintainers  
**Eng. Aya Jamal** – Security & Governance Lead  
**Ashraf Al-Haj** – System Architect / Final Reviewer

