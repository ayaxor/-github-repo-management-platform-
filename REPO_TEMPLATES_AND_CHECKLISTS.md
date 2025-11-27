

# Repo Templates & Checklists

This document provides standard templates and checklists to align all QuietWire / Civic AI Canon repositories with the GitHub Repository Management Platform.

---

## 1. Repository Types

- Product Repo
- Canon / Meta Repo
- Knowledge Base / Content Repo
- People / Apprenticeship Repo
- Infra / DevOps Repo

---

## 2. Product Repo Template (e.g., cap-platform)

### 2.1 Recommended Folder Structure

- `/docs`
  - `architecture.md`
  - `runbook.md`
  - `api_reference.md`
- `/src` or `/backend`, `/frontend`
- `/config`
- `/scripts`
- `/tests`
- `/attestations` (if part of pilot or critical)

### 2.2 Required Top-Level Files

- `README.md`
- `CONTRIBUTING.md` (if external contributions allowed)
- `LICENSE`
- `.github/ISSUE_TEMPLATE/*.md`
- `.github/PULL_REQUEST_TEMPLATE.md`
- `.github/workflows/ci.yml`

### 2.3 README Template (Product Repo)

```markdown
# <Repo Name>

## 1. Purpose
Short, high-level description of what this repo is for.

## 2. Scope
What this repo covers, and what is explicitly out of scope.

## 3. Architecture Overview
Link to `/docs/architecture.md` and summarize main components.

## 4. How to Run
- Prerequisites
- Local development steps
- How to run tests

## 5. How to Contribute
- Link to `CONTRIBUTING.md`
- Branching model
- PR expectations

## 6. Relationship to Canon / CAP / Ledger
Explain how this repo connects to the wider ecosystem.


---

3. Canon / Meta Repo Template

3.1 Example Folder Structure

00_Meta_Layer/

index.md (entry point)

architecture_overview.md


Events/

Attestations/

Mesh/

People/

Processes/


3.2 README Template (Canon Repo)

# Civic AI Canon – <Subdomain or Focus Area>

## 1. Purpose
Describe the conceptual area this repo covers.

## 2. Meta Layer
Refer to `00_Meta_Layer/index.md` as the canonical entry point.

## 3. Structure
Brief explanation of each top-level folder.

## 4. Governance
Who maintains this repo, and how changes are proposed and approved.

## 5. Links
- Related product repos
- Related CAP / Ledger components


---

4. Knowledge Base / Content Repo Template

/articles

/examples

/datasets (if applicable)

/diagrams

README.md with:

How to navigate

How to contribute new content

Tagging/labeling conventions




---

5. Apprenticeship / People Repo Template

/profiles

/apprenticeship_plans

/reports

/logs

README.md explaining:

Purpose

How apprenticeship reports are stored

How AI companions can assist (e.g., summaries)




---

6. Checklists

6.1 Checklist – New Repo Creation

[ ] Choose repo type (Product / Canon / KB / People / Infra)

[ ] Apply correct folder structure

[ ] Add README.md with standard sections

[ ] Add LICENSE

[ ] Add .github folder with:

[ ] Issue templates

[ ] PR template

[ ] CI workflow


[ ] Register repo in global catalog (Canon meta repo)

[ ] Assign an owner/maintainer

[ ] Set visibility (public / private)

[ ] Add default labels (e.g., type:feature, type:bug, area:<...>)


6.2 Checklist – Adding a New Feature

[ ] Create issue with clear description and acceptance criteria

[ ] Label issue appropriately

[ ] Create feature/<short-name> branch

[ ] Implement change with tests

[ ] Update documentation if needed

[ ] Open PR referencing the issue (e.g., Fixes #123)

[ ] Ensure CI passes (tests + lint)

[ ] Address review comments

[ ] Merge via PR (no direct commit to main)

[ ] If critical, update attestation / CAP event


6.3 Checklist – Documentation Update

[ ] Identify affected docs (README, /docs/*, Canon meta files)

[ ] Ensure English version is updated

[ ] If Arabic mirror exists, update *_AR.md

[ ] Run doc validation CI (if configured)

[ ] Add ADR if this reflects a major decision


