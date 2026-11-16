# ⚡ Performance and resource planning

## 📌 Current workload
The main notebook uses sparse word-level TF-IDF features with a configured cap of 5,000 terms and combines them with a small number of numeric features. Sparse matrices should remain sparse wherever possible.

## 🧠 Memory guidance
- Estimate matrix dimensions and dtype before allocating.
- Avoid converting TF-IDF matrices to dense arrays without calculating memory requirements.
- Reduce vocabulary size when debugging.
- Release intermediate matrices when they are no longer needed.
- Process permitted image data in bounded batches.
- Keep large generated artifacts outside Git.

## 🖼️ Image downloader caution
The current helper uses a fixed pool of 100 workers. This can create excessive request pressure, memory usage, and remote throttling. A future implementation should expose a conservative worker limit, timeouts, retry/backoff, caching, and structured failure reporting. Do not bypass provider limits.

## 📏 Benchmark discipline
Compare performance on the same data split and hardware. Record wall-clock time, peak memory, feature dimensions, model size, and validation SMAPE. Faster execution is not an improvement if it changes the split, drops records, or weakens validation quality.

## 🔮 Future optimization options
- Cache deterministic text preprocessing and feature matrices.
- Use sparse-compatible estimators where suitable.
- Profile preprocessing and model fit separately.
- Batch expensive transforms.
- Avoid downloading or embedding images unless the experiment demonstrates value under challenge rules.
