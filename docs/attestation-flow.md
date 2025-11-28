
# 🔐 Attestation Flow – GitHub → CAP → Ledger

This document explains how evidence flows through the attestation pipeline.

---

## 1. Overview
The attestation system ensures traceability and accountability across all releases.

---

## 2. ASCII Attestation Flow Diagram

```
              GitHub CI Pipeline
   ┌──────────────────────────────────┐
   │ Tests │ Lint │ Build │ Evidence │
   └───────────────┬──────────────────┘
                   ▼
         ┌────────────────────────┐
         │ Evidence Packaged (Raasid) │
         └───────────────┬────────┘
                         ▼
          CAP Event Created (Signed)
                         ▼
           Ledger Entry Generated
       ┌────────────────────────────────┐
       │ Immutable Attestation Record   │
       └────────────────────────────────┘
```

---

## 3. Evidence Included:
- SBOM  
- Test results  
- Build artifacts  
- PR history  
- Reviewer approvals  

Raasid ensures integrity, CAP signs the event, Ledger stores the proof.


