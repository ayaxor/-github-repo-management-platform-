
# Documentation Project — Folder Structure Template

This template is designed for documentation-heavy repositories,
architecture specifications, and ADR-first projects.

---

## Recommended Structure

. ├─ docs/ │  ├─ 00_index/ │  │  ├─ DOC_INDEX.md │  │  ├─ ADR_INDEX.md │  │  └─ GLOSSARY.md │  │ │  ├─ 00_registry/ │  │  └─ agents.md │  │ │  ├─ 01_requirements/ │  ├─ 02_architecture/ │  │  ├─ diagrams/ │  │  └─ README.md │  │ │  ├─ 03_protocol/ │  │  └─ schemas/ │  │ │  ├─ 04_security/ │  ├─ 07_ops/ │  ├─ 08_testing/ │  ├─ 09_delivery/ │  └─ 99_notes/ │ ├─ README.md └─ LICENSE

---

## Folder Purpose

- `docs/00_index/` — Canonical entry points and indexes
- `docs/00_registry/` — Identity and registry records
- `docs/01_requirements/` — System requirements
- `docs/02_architecture/` — Architecture descriptions and diagrams
- `docs/03_protocol/` — Protocol specifications and schemas
- `docs/04_security/` — Security documentation
- `docs/07_ops/` — Operations and observability
- `docs/08_testing/` — Testing strategy and criteria
- `docs/09_delivery/` — Implementation and delivery plans
- `docs/99_notes/` — Raw notes and historical context

---

## Notes

- Documentation is treated as a first-class artifact
- ADRs must be indexed and preserved
- Diagrams should use Mermaid where possible


---
