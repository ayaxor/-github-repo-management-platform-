
# Security / CAP Repository Template

This template is used for **security, threat analysis, and CAP** (Civic Analysis & Protection)
work within QuietWire and Civic AI Canon projects.

Replace `<placeholders>` with actual values.

---

## 1. Repository Identity

- **Repo name:** `<security-project-name>`
- **Focus area:** `<threat-intel / narrative-analysis / policy>`
- **Sensitivity level:** `<public / internal / restricted>`
- **Maintainer:** `<name>`

---

## 2. Purpose & Scope

Describe the purpose of this security or CAP repository:

- What are we securing or analyzing?
- What systems, narratives, or AI interactions are involved?
- Is this research, monitoring, documentation, or production security?

**Example:**

> This repository documents narrative risks and security posture associated with
> AI companion deployments, including threat surfaces and policy recommendations.

---

## 3. Recommended Folder Structure

```text
/README.md                     → Project overview
/SECURITY.md                   → Security posture, controls, restrictions
/THREAT_MODEL.md               → Structured threat model
/INCIDENT_LOG.md               → If incidents or anomalies are tracked
/POLICIES/
    access-control.md
    data-handling.md
    retention-policy.md
/EVIDENCE/
    logs/
    screenshots/
    references.md
/TOOLS/
    scripts/
    notebooks/


---

4. Threat Model Template

This file goes in: THREAT_MODEL.md

# Threat Model – <project-name>

## 1. Assets
What needs protecting?

## 2. Adversaries
Who might attack or manipulate the system?

## 3. Attack Surfaces
Where can attacks happen?
- Interface attacks
- Narrative injection
- Unauthorized access

## 4. Mitigations
- Safeguard 1
- Safeguard 2

## 5. Residual Risk
Short note about remaining unavoidable risks.


---

5. Policies

In /POLICIES/, include documents describing:

Data access rules

Retention expectations

What is forbidden

Escalation steps

Logging requirements


Example starter:

# Access Control Policy

Only authorized maintainers may modify SECURITY or THREAT_MODEL files.
All changes must be reviewed via pull request.


---

6. Incident Log Template

INCIDENT_LOG.md:

# Incident Log

## 2025-01-01
Description of incident, unusual behavior, or narrative shift.

Action Taken:
- Step 1
- Step 2

Status:
Resolved / Under Review


---

7. Definition of Done

A security or CAP repository is considered “ready” when:

[ ] README includes purpose and scope

[ ] SECURITY.md added and documented

[ ] THREAT_MODEL.md created

[ ] Policies folder exists with at least one policy

[ ] Evidence folder ready

[ ] If applicable, incident log started
