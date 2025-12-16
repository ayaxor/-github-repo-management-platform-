
# Scoring Model — Repo Health Checker

This document defines how the **Repository Health Score**
is calculated using the checklist results.

The score is **informational**, not a judgment of quality.

---

## Scoring Philosophy

- The score highlights improvement opportunities
- Missing items do NOT imply a bad repository
- Documentation and clarity are weighted higher than activity

---

## Score Categories

Each repository is evaluated across four categories:

### 1. Documentation (40%)
- README presence and clarity
- Usage or setup instructions

### 2. Governance (25%)
- LICENSE
- CONTRIBUTING
- SECURITY guidance

### 3. Structure (20%)
- Logical folder layout
- Clean root directory

### 4. Maintenance Signals (15%)
- Recent activity
- Ownership clarity

---

## Calculation Method

- Each checklist item = 1 point
- Points are grouped by category
- Category score = (points earned / total points) × category weight
- Final score = sum of category scores

---

## Score Interpretation

- **90–100**: Excellent baseline health
- **70–89**: Good, minor improvements recommended
- **50–69**: Fair, documentation or structure gaps exist
- **Below 50**: Early-stage or incomplete setup

---

## Important Notes

- Scores are not comparable across different project types
- Early-stage projects may score lower by design
- The score should be used as guidance only


--
