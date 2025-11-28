

---

## 7. Visual Workflow Diagrams

Below are visual diagrams that summarize the main operational workflows of the QuietWire GitHub Repository Management Platform.

### 7.1 Repository Lifecycle – From Idea to Ledger

```mermaid
flowchart LR
    A[Idea or Request] --> B[GitHub Issue Created]
    B --> C[Design & SRS Reference]
    C --> D[Feature Branch Created]
    D --> E[Development & Local Tests]
    E --> F[Pull Request Opened]
    F --> G[CI/CD Checks<br/>(tests, lint, security)]
    G --> H{All Checks Pass?}
    H -- No --> E
    H -- Yes --> I[Review & Approval by Maintainer]
    I --> J[Merge to main]
    J --> K[GitHub Release]
    K --> L[CAP Event Created]
    L --> M[Ledger Entry Written<br/>(Evidence & Attestation)]

7.2 Governance & Compliance Workflow

graph TD
    A[Governance Rules] --> B[Branch Protection]
    A --> C[Required Reviews]
    A --> D[Status Checks Required]
    A --> E[Security Policies]

    B --> B1[No direct commits to main]
    C --> C1[At least 1 maintainer review]
    D --> D1[CI must succeed before merge]
    E --> E1[Security scanning & disclosure rules]

7.3 AI Integration & Attestation Flow

sequenceDiagram
    participant Dev as Contributor / Aya
    participant GH as GitHub Repo
    participant Athena as Athena (AI Agent)
    participant CAP as CAP Platform
    participant Ledger as QuietWire Ledger

    Dev->>GH: Push commits / Open PR
    GH->>Athena: Request analysis (structure, docs, gaps)
    Athena->>GH: Comments, doc suggestions, checklists
    Dev->>GH: Apply fixes & update docs
    GH->>GH: Run CI/CD (tests, lint, SBOM)
    GH->>CAP: Send release & evidence metadata
    CAP->>Ledger: Record attested event & proofs
    Ledger->>GH: Reference hash / event ID

> These diagrams provide a quick, high-level view of how repositories, governance, AI agents, and the CAP/Ledger stack work together inside the QuietWire ecosystem.


