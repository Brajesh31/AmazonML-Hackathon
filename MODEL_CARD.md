# 🧠 Model card

## 📌 Model status
**No validated trained model is currently documented as a release artifact in this repository.** The main notebook contains exploratory text/tabular modeling code, but its stored LightGBM execution output includes a fit-argument TypeError. The separate `sample_code.py` predictor returns random values and is not a model.

## 🎯 Intended task
Estimate the positive numeric product `price` from challenge-provided catalog text and metadata.

## 🧱 Current experimental components
- Word-level TF-IDF text representation, up to 5,000 features.
- Heuristic quantity extraction from catalog text.
- First-match mass/volume parsing.
- LightGBM regression attempt with a log-transformed target.

These components are not a validated, packaged inference pipeline.

## 📏 Performance
No verified validation SMAPE, benchmark, leaderboard result, or model artifact is claimed in this card. Add results only with the code revision, data revision, fixed split, metric implementation, and reproducible run details.

## ⚠️ Known risks and limitations
- Heuristic parsing can confuse pack quantity, model numbers, and dimensions.
- Mass and volume are conflated in one feature.
- Text normalization removes non-ASCII characters.
- The notebook uses a machine-specific absolute path.
- The saved LightGBM fit call is incompatible with the installed API represented in its output.
- No independent fairness, robustness, or subgroup analysis is recorded.

## 🚦 Appropriate use
Do not use this repository as a production pricing system or for real-world price setting. It is a competition/research workspace. Any future model card must identify intended use, validation data, limitations, model license, parameter count where applicable, and known failure modes.

## 🔄 Update policy
Update this file whenever a trained model becomes reproducible and a model artifact is intentionally released. Never replace the current status with an unverified score.
