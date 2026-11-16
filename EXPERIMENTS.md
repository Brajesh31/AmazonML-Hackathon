# 🧪 Experiment log

This file is a structured record of verified experiments. Do not enter hypothetical or copied scores as results.

## 📌 Current status
No reproducible validation score is claimed for the checked-in notebook. Its saved LightGBM output contains an error for the `early_stopping_rounds` fit argument. The random predictor in `sample_code.py` is a format demonstration, not a baseline-quality model.

## 🗂️ Experiment register

| ID | Code revision | Features | Model | Split | Validation SMAPE | Status |
| --- | --- | --- | --- | --- | --- | --- |
| EXP-000 | Existing notebook state | TF-IDF + heuristic quantity/unit features | LightGBM attempt | Random 90/10 in notebook | Not verified | Compatibility error |

## 📝 New experiment template

Copy this block for each completed run:

```text
Experiment ID:
Date:
Git commit:
Dataset checksums:
Python version:
Dependency versions:
Hardware:
Train/validation strategy:
Random seed:
Feature pipeline:
Target transformation:
Model and parameters:
Metric implementation:
Validation SMAPE:
Runtime:
Peak memory:
Artifact path and checksum:
Known limitations:
Reproduction command:
```

## 🚦 Reporting rules
- Only publish metrics from completed runs.
- Use the same validation rows when comparing candidates.
- Keep test labels unavailable during model selection.
- Record failed runs as failures rather than silently deleting them.
- Document any change in preprocessing, target transform, or metric convention.
