

# Software Requirements Specification (SRS)  
## QuietWire / Civic AI Canon  
### GitHub Repository Management Platform

---

## 1. Introduction

### 1.1 Purpose
This Software Requirements Specification (SRS) defines the functional and non-functional requirements for the **GitHub Repository Management Platform** used by **QuietWire, CAP, Civic AI Canon, and related projects**.

The goal is to provide a **canonical, auditable, AI-friendly** layer on top of GitHub that standardizes:
- Repository taxonomy and structure
- Governance (branching, issues, PRs, releases)
- AI/agent integration (Athena, Queen Bee, Raasid, worker agents)
- Attestation and evidence flows (CAP / Ledger)

This SRS will be the reference for:
- System architect(s) (e.g., Ashraf)
- Maintainers and contributors
- Apprentices (e.g., Aya)
- AI companions (Athena, etc.), when interpreting the platform behavior.

### 1.2 Scope
The platform covers **how GitHub is used**, not GitHub itself as a product.

In scope:
- Repository lifecycle (creation, archiving, deprecation)
- Repository taxonomy and standard layouts
- Branching, tagging, issues, PR workflows
- CI/CD and automation patterns
- AI agent integration patterns
- Attestation and Ledger integration
- Documentation standards and governance

Out of scope:
- Implementation of GitHub itself
- Implementation details of external AI models
- Implementation of CAP / Ledger internals (treated as external systems)

### 1.3 Definitions, Acronyms, Abbreviations
- **Canon**: Civic AI Canon – the core conceptual and architectural layer.
- **CAP**: Civic Attestation Platform or related CAP components.
- **Ledger**: QuietWire / CAP ledger of events and evidences.
- **Attestation**: Human- and machine-readable proof of actions, evidence, and events.
- **AI Companions / Agents**: Athena, Queen Bee, Raasid, worker agents operating over GitHub.
- **Canonical Repo**: The official “source of truth” repository for a specific project or product.

### 1.4 Stakeholders
- **Ashraf (System Architect / Master Archivist)**  
  Defines canonical structures and approves standards.
- **Maintainers (Core Devs / Leads)**  
  Own specific repositories, approve PRs, enforce standards.
- **Contributors / Apprentices (Aya, interns, partners)**  
  Implement features and docs following templates and workflows.
- **AI Companions (Athena, Queen Bee, Raasid, worker agents)**  
  Read repos, generate docs, and support attestation.

---

## 2. Overall Description

### 2.1 System Vision
The platform must enable every repository to be:
- **Readable by humans in minutes**
- **Parsable by AI agents without chaos**
- **Traceable and attestable** for all important changes

New contributors (e.g., Aya) must be able to:
- Open a repo
- Read top-level docs
- Immediately understand:
  - What the repo is for
  - Who owns it
  - How to use it
  - How to contribute

### 2.2 System Context
The platform sits between:
- **GitHub Organizations** (quietwire, civic-ai-canon, internal orgs)
- **AI / LLM APIs** (OpenAI, Kimi, Minimax, etc.)
- **CAP / Ledger** as evidence and attestation backends

It defines:
- How repos are named, structured, and documented
- How automations and CI run
- How AI agents interact safely

### 2.3 User Classes and Characteristics
- **Admins** – Org-level control, manage access and global policies
- **Maintainers** – Repo-level owners, responsible for quality and structure
- **Contributors** – Submit changes via PRs
- **Apprentices** – Learning contributors, guided by templates and AI assistants
- **AI Agents** – Consume metadata, suggest changes, and produce documentation and attestations

### 2.4 Assumptions and Dependencies
- GitHub is available and stable as the primary code host.
- CAP and Ledger systems exist and are accessible via APIs or agreed integration patterns.
- AI APIs (OpenAI, Kimi, etc.) are available for agent operations.
- Organization-level permissions are managed by Admins.

---

## 3. System Architecture Overview

The platform is conceptualized as **four layers**:

1. **GitHub Organization Layer**  
   - One or more orgs: `quietwire`, `civic-ai-canon`, internal org(s).
   - Repos grouped by type: Product, Canon, KB/content, Apprenticeship/People, Infra.

2. **Repository Taxonomy Layer**  
   - **Product repos**: `cap-platform`, `quietwire-ledger-main`  
   - **Canon repos**: `civic-ai-canon-main`  
   - **KB/content repos**: `cap-bank-demo-kb`  
   - **People / Apprenticeship repos**: apprenticeship bundles, internal people frameworks  
   - **Infra repos**: CI/CD, deployment, infra-as-code

3. **Governance & Workflow Layer**  
   - Branch strategies, PR rules, labels, milestones, issue/PR templates
   - CI (GitHub Actions) and release processes

4. **AI & Attestation Layer**  
   - APIs for GitHub and LLMs  
   - AI companions scanning repos, generating docs, and emitting attestations  
   - Links to QuietWire ledger / CAP evidences

---

## 4. Functional Requirements

> NOTE: FR numbers directly map back to the original functional brief.

### 4.1 Repository Lifecycle Management

**FR-1 – New Repository Creation**  
The platform **shall provide** a standard process for creating new repositories:
- Choose type: Product / Canon / KB / People / Infra
- Apply appropriate template (folder structure, base files)
- Register the repo in a central catalog (Canon or internal meta repo)

**FR-2 – Mandatory Top-Level Files**  
Each repo **shall include**:
- `README.md` (English, mandatory)
- Optional `README_AR.md` (Arabic mirror)
- `CONTRIBUTING.md` if repo accepts external contributions
- `LICENSE` with appropriate legal text

**FR-3 – Archiving Repositories**  
The platform **shall support** archiving:
- Mark repo as `ARCHIVED` in GitHub description and catalog
- Set read-only mode where appropriate

**FR-4 – Deprecation & Replacement**  
When a repo is replaced:
- Old repo must clearly state: “Superseded by <new-repo>”
- New repo must reference: “Replaces <old-repo>”

### 4.2 Structure & Templates

**FR-5 – Standard Folder Layouts per Repo Type**  
For Product repos (e.g., `cap-platform`), recommended layout:

- `/docs` – architecture, runbooks, API docs  
- `/src` or `/backend`, `/frontend` – core code  
- `/scripts` – helper or demo scripts  
- `/config` – configs, infra definitions  
- `/tests` – automated tests  

For Canon / Content repos:
- `00_Meta_Layer` – global instructions & architecture
- Additional folders grouped by conceptual layers (Events, Attestations, Mesh, People, etc.)

**FR-6 – Repo Scaffolding Templates**  
The platform **shall provide**:
- README template (Purpose, Scope, Architecture, How to Run, How to Contribute)
- Issue templates (bug, feature, documentation, research)
- PR template

**FR-7 – AI-Friendly Templates**  
Templates **shall use** consistent file names, headings, and markers so AI agents can reliably detect them.

### 4.3 Branching & Versioning

**FR-8 – Branch Strategy**  
Standard branch patterns:
- `main` (canonical / production)
- `develop` (optional, integration)
- `feature/<short-name>`
- `hotfix/<short-name>`

**FR-9 – Tagging & Releases**  
Releases **shall use**:
- Semantic versioning: `vX.Y.Z` for product releases
- Date-based tags: `YYYY-MM-DD_<context>` for demos/snapshots (e.g., `2025-11-27_CAP_Demo`)

**FR-10 – Release Notes**  
Releases **shall**:
- Include release notes, ideally auto-generated from PRs
- Link to evidence or attestation files when available

### 4.4 Access Control & Permissions

**FR-11 – Repo Ownership**  
Each repo **must** have a clear owner (person or small team).

**FR-12 – Role Levels**  
The platform recognizes:
- Admin (org-wide)
- Maintainer (per repo)
- Contributor (PR-based contributions)
- Reader (read-only)

**FR-13 – Sensitive Repos**  
Sensitive repos **must**:
- Be private
- Have access maps documented in `/docs/governance/ACCESS.md`

**FR-14 – Access Changes Logging**  
Access changes (grant/revoke) **should** be logged in a Canon / internal admin log.

### 4.5 Issues, PRs & Workflow

**FR-15 – Issue Tracking**  
All work **should** be tracked via GitHub Issues with:
- Labels (e.g., `type:feature`, `type:bug`, `area:canon`, `difficulty:easy`, `status:blocked`)
- Assignee
- Clear description, acceptance criteria, and links to design docs

**FR-16 – Pull Requests**  
PRs **must**:
- Reference at least one issue (e.g., `Fixes #123`)
- Use a PR template (Summary, Changes, Testing, Notes)
- Be reviewed by at least one maintainer (or required reviewers for critical repos)

**FR-17 – Protection Rules**  
For selected repos:
- No direct commits to `main` (except defined emergency hotfix paths)
- PR checks enforced (status checks such as tests and lint)

**FR-18 – Standard Workflows**  
The platform **shall define** standard workflows for:
- Adding new features
- Fixing bugs
- Writing documentation
- Refactoring / restructuring

### 4.6 Automation & GitHub Actions

**FR-19 – CI for Code Repos**  
For code repos, CI **shall**:
- Run on PRs and pushes to `main`
- At minimum: run tests and lint/format checks

**FR-20 – CI for Docs/Canon Repos**  
For documentation or Canon repos, CI **may**:
- Validate Markdown structure and links
- Optionally generate static sites or indexes

**FR-21 – Evidence Artifacts**  
Where applicable, CI **shall** export artifacts (logs, SBOMs, test reports) that can be used as evidence.

**FR-22 – Machine-Readable Outputs**  
CI **should** emit JSON/YAML outputs for AI agents.

### 4.7 Attestation & Ledger Integration

**FR-23 – CAP / Ledger Integration**  
The platform **shall** support:
- Evidence files generated from builds linked to CAP events
- Attestation files acting as human-readable side of CAP events

**FR-24 – Critical Changes Pattern**  
For critical changes (e.g., releases), a standard pattern **must** be documented:
- GitHub Release → CAP Event → Ledger Entry

**FR-25 – Pilot Repos**  
Repos used in pilots **must** include:
- `/attestations` or `/events` folder mirroring CAP events

### 4.8 AI / Agent Integration

**FR-26 – API-Level Access for Agents**  
The platform **shall** allow limited-scope API access for AI agents to:
- Read repo metadata, commits, issues, and PRs

**FR-27 – AI-Friendly Structure**  
Repos **shall** be structured so agents can:
- Identify `README`, `/docs/architecture`, `/docs/runbooks` quickly
- Walk folder tree and classify content types

**FR-28 – Agent Roles**  
Agent roles include:
- **“Queen Bee” / Master Agent**: cross-repo coordination & planning
- **Worker Agents**: per-repo tasks (refactors, doc generation, diagrams)

**FR-29 – Interaction Protocols**  
The platform **shall** define:
- QFF (Feature Frames)
- Handshake protocols
- Issue templates designed for AI-assisted tasks

### 4.9 Documentation & Knowledge Management

**FR-30 – Repo Self-Description**  
Every repo **must** explain:
- What it is
- What it is not
- How it fits into Canon / CAP ecosystem

**FR-31 – Global Repo Catalog**  
Canon/meta repos **must** maintain a global index of all repos:
- Description, owner, status, maturity, main links

**FR-32 – Bilingual Strategy**  
English is primary; key documents **may** include Arabic mirrors (`*_AR.md`).

**FR-33 – Decision History**  
The platform **shall** support Architecture Decision Records (ADRs) linked to issues/PRs.

---

## 5. Non-Functional Requirements (NFRs)

**NFR-1 – Security**
- Principle of least privilege
- Private repos, proper secret management (GitHub Secrets, no hard-coded keys)

**NFR-2 – Reliability**
- CI workflows stable and fast enough not to block development
- Workflows deterministic and documented

**NFR-3 – Observability & Traceability**
- Ability to answer:
  - Who changed what, when, and why?
  - Where is the evidence for this release or doc?

**NFR-4 – Usability (Humans + AI)**
- Simple, predictable repo layouts
- Low cognitive load for new contributors

**NFR-5 – Interoperability**
- No unnecessary lock-in to a single vendor pattern
- Structure compatible with local dev and other platforms

**NFR-6 – Consistency**
- Same patterns repeated across repos (folders, naming, labels, CI structure)

---

## 6. Documentation Deliverables

The platform will be complemented by:
- Repo taxonomy & catalog
- Repo templates & checklists
- Governance & workflow playbook
- AI integration protocol
- Attestation integration guide

---

## 7. Future Enhancements

- Automated checks for structural compliance (linting for repo layout)
- “One-click” CAP event + Ledger entry from GitHub actions
- Richer AI protocols for autonomous but supervised changes

