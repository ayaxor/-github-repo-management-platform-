
# Library Project — Folder Structure Template

This template is designed for reusable libraries,
SDKs, and packages intended for distribution.

---

## Recommended Structure

. ├─ src/ │  └─ library_name/ │     ├─ init.py │     ├─ core.py │     └─ utils.py │ ├─ tests/ │  ├─ unit/ │  └─ integration/ │ ├─ docs/ │  ├─ usage.md │  ├─ api.md │  └─ changelog.md │ ├─ examples/ │  └─ basic_usage.md │ ├─ README.md ├─ LICENSE └─ pyproject.toml

---

## Folder Purpose

- `src/` — Library source code
- `tests/` — Automated tests
- `docs/` — Usage guides and API reference
- `examples/` — Practical usage examples
- `pyproject.toml` — Packaging and build configuration

---

## Notes

- Public APIs should be clearly documented
- Semantic versioning is recommended
- Examples should remain minimal and runnable

