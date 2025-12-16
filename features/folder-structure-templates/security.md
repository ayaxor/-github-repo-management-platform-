
# Security Project — Folder Structure Template

This template is designed for security-focused repositories,
including threat modeling, audits, and security tooling.

---

## Recommended Structure

. ├─ docs/ │  ├─ threat-model/ │  │  ├─ overview.md │  │  ├─ assets.md │  │  ├─ threats.md │  │  └─ mitigations.md │  │ │  ├─ policies/ │  │  ├─ auth.md │  │  ├─ encryption.md │  │  └─ data-protection.md │  │ │  ├─ audits/ │  │  ├─ findings.md │  │  └─ remediation.md │  │ │  └─ compliance/ │     ├─ standards.md │     └─ evidence.md │ ├─ src/ │  └─ tools/ │ ├─ tests/ │  └─ security/ │ ├─ README.md └─ LICENSE

---

## Folder Purpose

- `docs/threat-model/` — Threat identification and analysis
- `docs/policies/` — Security policies and controls
- `docs/audits/` — Audit results and remediation
- `docs/compliance/` — Compliance mapping and evidence
- `src/tools/` — Security tooling and scripts
- `tests/security/` — Security-related tests

---

## Notes

- Threat models should be updated with system changes
- Audit findings must be traceable to remediation
- Documentation precedes tooling

