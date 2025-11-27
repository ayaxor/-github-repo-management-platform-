

# Governance & Workflow Playbook  
## QuietWire / Civic AI Canon – GitHub Repository Management Platform

---

## 1. Branching Strategy

- `main`
  - Canonical, production-ready state.
  - Protected branch (no direct commits).
- `develop` (optional)
  - Integration branch for upcoming releases.
- `feature/<short-name>`
  - Used for implementing new features.
- `hotfix/<short-name>`
  - Used for urgent fixes to production.

---

## 2. Issue Workflow – “From Idea to Release”

1. **Idea / Request**
   - Raised as a GitHub Issue.
   - Tagged with appropriate `type:*` and `area:*` labels.

2. **Planning**
   - Add acceptance criteria.
   - Link any design docs (Canon or `/docs`).

3. **Implementation**
   - Create `feature/<short-name>` branch.
   - Work committed with clear messages.

4. **Pull Request**
   - PR references the issue (`Fixes #<id>`).
   - Uses standard PR template.

5. **Review**
   - At least one maintainer review.
   - CI checks must pass.

6. **Merge & Release**
   - Merge into `main` (or `develop` then `main`).
   - Create release tag if appropriate.
   - Trigger CAP / Ledger attestation if relevant.

---

## 3. Labels & Milestones

### 3.1 Standard Labels

- `type:feature`
- `type:bug`
- `type:doc`
- `type:refactor`
- `area:canon`
- `area:cap-platform`
- `area:ledger`
- `difficulty:easy`
- `difficulty:medium`
- `difficulty:hard`
- `status:blocked`
- `status:needs-review`

### 3.2 Milestones

Milestones can represent:
- Releases (e.g., `v1.0`, `v1.1`)
- Pilots (e.g., `Bank Demo Pilot`)
- Internal phases (e.g., `Q1-2026 Roadmap`)

---

## 4. Roles & Responsibilities

- **Admin**
  - Manages org-level settings.
  - Configures branch protection, SSO, teams.

- **Maintainer**
  - Owns repo quality and structure.
  - Approves PRs.
  - Ensures compliance with this playbook.

- **Contributor / Apprentice**
  - Works through issues and PRs.
  - Follows templates and checklists.
  - Uses AI agents as assistants, not as silent actors.

- **AI Agents**
  - Propose, never impose.
  - Operate via PRs and Issues, not direct commits.

---

## 5. Example Workflow: Idea → Issue → PR → Release → CAP Event

1. New feature idea for `cap-platform`.
2. Issue created: `type:feature`, `area:cap-platform`.
3. Feature designed and documented in `/docs/architecture.md`.
4. Branch created: `feature/cap-auth-improvements`.
5. Work implemented + tests + docs.
6. PR opened, CI passes, review done.
7. PR merged into `main`, release `v1.2.0` created.
8. CI generates test reports and SBOM.
9. Attestation and evidence linked to a CAP event.
10. Ledger updated with event and references to GitHub release.

---
