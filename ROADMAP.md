# 🗺️ Project roadmap

This roadmap separates corrective work from optional research ideas. Items are proposals until implemented and validated.

## 🚧 Priority 1: Make the current workflow reproducible
- [ ] Replace machine-specific notebook paths with repository-relative configuration.
- [ ] Resolve the LightGBM early-stopping API compatibility error and execute the notebook from a clean kernel.
- [ ] Pin a tested environment or publish a lockfile.
- [ ] Add deterministic seeds and a documented validation split.
- [ ] Implement a standalone SMAPE function with a documented zero-denominator convention.
- [ ] Add tests for quantity parsing, unit parsing, and submission validation.
- [ ] Replace the random demonstration predictor with an explicitly labeled baseline only after a real model is implemented.

## 🧰 Priority 2: Improve feature quality
- [ ] Make quantity parsing context-aware.
- [ ] Separate mass and volume features.
- [ ] Add robust missing/ambiguous parse indicators.
- [ ] Compare word and character TF-IDF representations.
- [ ] Audit duplicate records and validation leakage.
- [ ] Add bounded, timeout-aware image retrieval only if permitted by challenge rules.

## 🔬 Priority 3: Research extensions
- [ ] Compare text-only, structured-only, and combined models.
- [ ] Evaluate permitted image embeddings against the same validation split.
- [ ] Track experiment parameters, metrics, runtime, and artifacts.
- [ ] Add error analysis by price band and product category where labels permit.

## 🧹 Repository maintenance
- [ ] Remove tracked notebook checkpoints and bytecode in a dedicated cleanup change.
- [ ] Keep generated images, models, caches, and feature matrices out of Git.
- [ ] Review dependencies and workflow permissions periodically.

> No target score, model improvement, or completion date is promised by this roadmap.
