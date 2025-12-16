
# Platform Project — Folder Structure Template

This template provides a recommended folder structure
for scalable platform projects and long-lived systems.

---

## Recommended Structure

. ├─ docs/ │  ├─ 00_index/ │  ├─ 01_requirements/ │  ├─ 02_architecture/ │  ├─ 03_protocol/ │  ├─ 04_security/ │  └─ 99_notes/ │ ├─ src/ │  ├─ core/ │  ├─ services/ │  ├─ adapters/ │  └─ utils/ │ ├─ tests/ │  ├─ unit/ │  ├─ integration/ │  └─ contract/ │ ├─ configs/ │  ├─ default.yaml │  └─ environments/ │ ├─ scripts/ │  └─ setup.sh │ ├─ README.md └─ LICENSE

---

## Folder Purpose

- `docs/` — Canonical documentation and specifications
- `src/` — Application source code
- `tests/` — Automated testing suites
- `configs/` — Configuration files by environment
- `scripts/` — Automation and setup scripts

---

## Starter Files (Optional)

- README.md
- LICENSE
- .gitignore
- CONTRIBUTING.md

---

## Notes

- Keep the root directory minimal
- Separate core logic from adapters
- Documentation should evolve alongside code

