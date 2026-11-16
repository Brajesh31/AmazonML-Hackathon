# 🧯 Troubleshooting

**Dataset path error:** notebook contains a developer-specific Windows path. Run Jupyter at the repo root and load files from `Path("dataset")`.

**LightGBM TypeError:** saved output says `LGBMRegressor.fit() got an unexpected keyword argument 'early_stopping_rounds'`. Use the supported callback API for the installed version, or remove early stopping for a simple compatibility run. Re-execute the notebook.

**Import errors:** install packages into the active notebook kernel environment, then restart the kernel.

**Memory pressure:** reduce TF-IDF feature count during debugging and avoid dense conversion without a memory estimate.

**Image download failures:** current helper runs 100 workers without retry/timeout controls. Reduce concurrency, cache results, and respect source throttling.

**Submission rejected:** verify columns, row count, unique test ID coverage, finite values, and positive prices.
