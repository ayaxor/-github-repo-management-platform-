

# Attestation Integration Guide  
## GitHub ↔ CAP ↔ Ledger

---

## 1. Purpose

This guide describes how GitHub repositories interact with the CAP / Ledger stack to support:
- Evidence generation
- Attestation documents
- Traceable links between releases, events, and evidences

---

## 2. Key Concepts

- **Evidence Artifact**  
  Any log, report, SBOM, or generated file that proves some action or test occurred.

- **Attestation File**  
  Human-readable document stored in the repo that describes:
  - What happened
  - When
  - Who was involved
  - Links to evidence files and CAP events

---

## 3. Standard Pattern for Critical Changes

1. Change merged into `main`.
2. New release created in GitHub (e.g., `v1.2.3`).
3. CI workflow:
   - Runs tests.
   - Generates evidence artifacts (logs, SBOM, test reports).
   - Packages these into a structured folder (e.g., `/attestations/v1.2.3/`).
4. CAP event created, referencing:
   - GitHub release
   - Evidence artifacts
   - Attestation file
5. Ledger entry recorded referencing the CAP event.

---

## 4. Repo-Level Structure

Recommended:
- `/attestations/`
  - `v1.2.3/`
    - `attestation.md`
    - `test-report.json`
    - `sbom.json`
    - `links.json` (references to CAP event IDs, Ledger IDs, GitHub release URL)

---

## 5. Example Attestation Document

```markdown
# Attestation – Release v1.2.3

## 1. Context
- Repo: cap-platform
- Release: v1.2.3
- Date: 2025-11-27
- Owner: <maintainer-name>

## 2. Summary
Describe the main changes included in this release.

## 3. Evidence
- Test logs: `test-report.json`
- SBOM: `sbom.json`
- CI run URL: <link>

## 4. CAP / Ledger Links
- CAP Event ID: <id>
- Ledger Entry ID: <id>


---