
# QuietWire Repository Platform – Architecture Overview

This document provides a high-level architecture view of the GitHub Repository Management Platform.

## Layers

1. **Organization Layer**  
   GitHub Orgs: quietwire / civic-ai-canon / internal

2. **Repository Layer**  
   Product repos, Canon repos, KB repos, Infra repos, People/Apprenticeship repos.

3. **Governance Layer**  
   Issues, PRs, branching strategy, labels, CI/CD, release rules.

4. **AI & Attestation Layer**  
   Athena + QueenBee + Raasid + CAP Events + Ledger.

## Diagram (add later when repo becomes public)

```mermaid
flowchart TD
    A[GitHub Orgs] --> B[Repo Types]
    B --> C[Governance Rules]
    C --> D[AI Agents]
    D --> E[Attestation Flow]

---
