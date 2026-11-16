# 🧯 Troubleshooting

## 📁 Dataset not found
The notebook contains a developer-specific Windows absolute path. Run Jupyter from the repository root and load files with `Path("dataset") / "train.csv"` and `Path("dataset") / "test.csv"`.

## 🌲 LightGBM fit TypeError
The saved notebook output records `LGBMRegressor.fit() got an unexpected keyword argument 'early_stopping_rounds'`. Check the installed LightGBM version and use its supported callback API, or disable early stopping for a minimal compatibility test. Re-run the cell and save fresh output.

## 📦 Import errors
Install packages into the same environment used by the Jupyter kernel, then restart the kernel.

## 🧠 Memory pressure
Sparse TF-IDF matrices can be large. Reduce feature count for debugging and avoid dense conversion without estimating memory use.

## 🖼️ Image download failures
The current helper uses 100 workers and has no explicit timeout/retry controls. Reduce concurrency in a revised implementation, cache successful downloads, and respect source throttling.

## 📤 Submission rejected
Verify exact columns, row count, unique test ID coverage, finite numeric values, and strictly positive prices.
