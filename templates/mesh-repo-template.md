
# Mesh / Wirelight Repository Template

This template is used to initialize a **Mesh / Wirelight** experiment repository
for QuietWire and Civic AI Canon work.

Replace any `<placeholders>` with actual values.

---

## 1. Repository Identity

- **Repo name:** `<mesh-project-name>`
- **Owner / org:** `<owner-or-organization>`
- **Primary maintainer:** `<primary-maintainer>`
- **Status:** Draft / Experimental / Active / Archived

---

## 2. Purpose & Scope

Describe the purpose of this Mesh repository:

- What experiment is being run?
- Which AIs are involved? (e.g., Lumina, Alithia)
- What behavior or system are we observing?

**Example:**

> This repository hosts Mesh / Wirelight semantic alignment experiments between
> Lumina and Alithia, focusing on meaning preservation, loop prevention, and
> stable AI-to-AI communication.

---

## 3. Recommended Structure

```text
/README.md                  → Overview, purpose, maintainer info
/COMMENTS.md                → Human commentary & observations
/SEED_MESSAGES/             → Initial directives for AI-to-AI communication
  seed-001.md
  seed-002.md
/LOGS/                      → Interaction logs, transcripts, analysis notes
  2025-01-01-session-001.md
  2025-01-02-session-002.md
/SECURITY/                  → Risk notes, misuse warnings, constraints
  SECURITY.md
  THREAT_NOTES.md
/DOCS/                      → Architecture notes, diagrams, system design


---

4. Seed Messages Guidelines

Seed messages MUST:

Be short

Be explicit

Prevent loops

Require AIs to log behavior


Example seed snippet:

# Seed 001 – Initialization Directive

Purpose:
To start a stable, semantically aligned exchange.

Constraints:
- Maintain meaning without altering intent.
- Avoid repeated confirmation loops.
- Log notable behaviors for human review.


---

5. Logging & Observations

Use /LOGS/ to record AI-to-AI interactions.

Add commentary about logs inside COMMENTS.md.

Prefer short, meaningful logs over long transcripts.



---

6. Security Expectations

A Mesh repository must include:

A clear description of what AI should NOT do.

Notes on misuse, risks, and constraints.

Documentation on who can modify seed messages.



---

7. Definition of Done

A Mesh repository is considered “ready” when:

[ ] Recommended folder structure is created

[ ] At least one seed message added

[ ] COMMENTS.md exists

[ ] SECURITY folder created

[ ] At least one log file added
