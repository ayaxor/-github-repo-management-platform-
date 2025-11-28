

# AI Integration Protocol  
## Athena / Queen Bee / Raasid / Worker Agents

---

## 1. Agent Roles

- **Queen Bee / Master Agent**
  - Global understanding of repo ecosystem.
  - Cross-repo planning.
  - High-level summaries and roadmaps.

- **Athena**
  - Per-repo analysis.
  - Generates documentation, checklists, and reports.
  - Helps apprentices (e.g., Aya) interpret and apply the standards.

- **Worker Agents**
  - Narrow tasks within a single repo:
    - Refactor documentation.
    - Generate diagrams.
    - Classify files.
    - Extract requirements.

---

## 2. Access Model

- Agents access GitHub via:
  - Personal Access Tokens (PAT) with minimal scopes.
  - Or GitHub Apps with limited permissions.

- Allowed operations:
  - Read repository contents and metadata.
  - Open issues.
  - Propose PRs with changes.
  - Comment on issues/PRs.

- Forbidden operations:
  - Direct commits to `main`.
  - Deleting repos.
  - Changing access permissions.

---

## 3. Interaction Protocol

### 3.1 Handshake

1. Agent identifies itself in comments (e.g., “Athena Agent vX.Y”).
2. Agent declares:
   - What repo it is acting on.
   - What task it is performing.
   - What files it will touch.

### 3.2 QFF – QuietWire Feature Frames (Example)

A QFF may include:
- Feature name
- Context
- Affected components
- Acceptance criteria
- Risks and dependencies

Agents can:
- Generate QFF drafts.
- Attach QFF to issues and PR descriptions.

---

## 4. Logging & Attestation of Agent Actions

- Every agent action must be:
  - Visible in GitHub (issue, comment, PR).
  - Logged in a structured way when possible (JSON/YAML embedded or attached).

- No “silent” file changes:
  - All modifications must go through PR.
  - Human review is mandatory.

---

## 5. Example Flows

### 5.1 Athena Assisting Aya

1. Aya opens an Issue: “Standardize README for repo X”.
2. Athena:
   - Scans repo.
   - Suggests new README content in a PR.
   - Adds comments explaining structure.
3. Aya reviews, edits, and merges.

---

