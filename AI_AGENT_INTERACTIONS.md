
# 🤖 AI Agent Interaction Specification

Defines how Athena, QueenBee, and Raasid interact with QuietWire repositories.

---

## 1. Agents
### Athena  
- Documentation  
- Structure review  
- Detects missing patterns  
- Generates suggestions  

### QueenBee  
- Global planning  
- Cross-repo state  
- Canon alignment  

### Raasid  
- Evidence collection  
- Attestation packaging  
- Ledger integrity  

---

## 2. Interaction Flow (ASCII Diagram)

```
Athena → scans repo → detects gaps → creates PR
          │
          ▼
QueenBee → validates global impact → governance checks
          │
          ▼
Raasid → extracts CI evidence → creates CAP event → ledger entry
```

---

## 3. Rules
- No agent commits directly  
- All agent actions logged  
- PR only  
- Evidence must pass Raasid validation


---
