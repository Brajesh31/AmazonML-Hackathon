# 🧪 Modeling methodology and experiment protocol

## 🎯 Objective
Predict the positive numeric `price` target from challenge-provided product information. Model selection must use labeled training data and internal validation only.

## 🔍 Existing notebook workflow
The checked-in notebook loads train/test CSVs, extracts quantity using the last integer-like token, parses the first recognized mass/volume token, normalizes catalog text, fits word-level TF-IDF (up to 5,000 features, unigrams/bigrams), combines text and numeric features, applies `log1p` to the target, and creates a random 90/10 split before attempting LightGBM regression.

The stored execution output contains a TypeError because `early_stopping_rounds` is passed directly to `LGBMRegressor.fit`. Treat the notebook as experimental, not a verified end-to-end run. Ridge is imported but no completed Ridge experiment is established.

## 🧪 Recommended experiments
- Establish a median/constant sanity baseline.
- Freeze a deterministic train/validation split.
- Compare TF-IDF + Ridge, structured-only, and combined features.
- Compare raw-target and log-target training separately.
- Add feature groups one at a time.
- Use identical validation records for every candidate.
- Record parameters, SMAPE, runtime, and memory.

## 🧯 Avoid misleading comparisons
Do not tune on the challenge test set. Fit preprocessing inside training folds. Record split, seed, target transform, and feature parameters. Investigate duplicates and leakage before interpreting an unusually low score.

## 📝 Experiment record
| Field | Record |
| --- | --- |
| Experiment ID | Unique run name |
| Code revision | Git SHA |
| Data revision | Checksums and row counts |
| Split | Strategy, seed, fold manifest |
| Features | Text, quantity, units, image, other |
| Target | Raw or transformed |
| Model | Family and parameters |
| Metric | SMAPE implementation and result |
| Resources | Runtime, hardware, memory |
| Notes | Failures and next action |
