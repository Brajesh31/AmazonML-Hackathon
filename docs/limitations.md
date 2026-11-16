# ⚠️ Current limitations and known risks

This document describes observed limitations, not hypothetical defects.

## 🧪 Modeling limitations
- The notebook contains an experimental pipeline, not a packaged inference workflow.
- Saved LightGBM output shows a TypeError for the `early_stopping_rounds` fit argument.
- No verified validation SMAPE is documented.
- The quantity parser relies on the last integer-like token and can confuse pack counts with model numbers or dimensions.
- The unit parser uses the first match and combines mass and volume into one feature.
- Text normalization removes non-ASCII characters.

## 🧰 Engineering limitations
- The notebook contains a developer-specific absolute Windows path.
- No pinned dependency lockfile is provided. `requirements.txt` contains version ranges only.
- No dedicated model/feature/submission unit-test suite is present.
- The image downloader uses 100 workers and lacks explicit timeout/retry/backoff handling.
- No experiment tracker, model registry, HTTP API, or hosted inference service exists.

## 🚦 Appropriate interpretation
The repository is a challenge/research workspace. It should not be represented as a production price-estimation service or as a completed, validated competition solution.

## 🔄 Resolution priorities
See [ROADMAP.md](../ROADMAP.md). Prioritize portable paths, compatible LightGBM callbacks, deterministic validation, feature parser tests, submission checks, and a reproducible environment before adding more model complexity.
