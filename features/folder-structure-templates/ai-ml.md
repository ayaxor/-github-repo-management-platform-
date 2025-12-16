
# AI / ML Project — Folder Structure Template

This template is designed for machine learning and AI projects,
including experimentation, training, and evaluation.

---

## Recommended Structure

. ├─ data/ │  ├─ raw/ │  ├─ processed/ │  └─ external/ │ ├─ notebooks/ │  └─ exploration.ipynb │ ├─ src/ │  ├─ models/ │  ├─ training/ │  ├─ evaluation/ │  └─ utils/ │ ├─ experiments/ │  ├─ configs/ │  └─ results/ │ ├─ docs/ │  ├─ problem.md │  ├─ dataset.md │  ├─ methodology.md │  └─ ethics.md │ ├─ tests/ │  └─ model-tests/ │ ├─ README.md └─ LICENSE

---

## Folder Purpose

- `data/` — Datasets (raw, processed, external)
- `notebooks/` — Exploration and analysis notebooks
- `src/` — Training, evaluation, and model code
- `experiments/` — Experiment configurations and results
- `docs/` — Problem definition, datasets, and ethics
- `tests/` — Model validation and sanity checks

---

## Notes

- Keep raw data immutable
- Track experiments and results carefully
- Document ethical considerations explicitly

