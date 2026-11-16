# 🔁 Reproducibility

Record code SHA, dataset checksums, row counts, Python and package versions, hardware, random seeds, validation split, feature parameters, model parameters, target transformation, metric implementation, score, runtime, and artifact checksums.

```mermaid
flowchart LR
    A[Pin code] --> B[Pin data]
    B --> C[Recreate environment]
    C --> D[Freeze split]
    D --> E[Run experiment]
    E --> F[Record metrics]
    F --> G[Archive artifacts]
    G --> H[Repeat cleanly]
```

Current gaps include an absolute Windows path in the notebook, a stored LightGBM fit error, no pinned dependency lockfile, and old cell outputs that do not prove a current successful run. Use relative paths and a clean-kernel run.
