# Architecture

The repository is an experiment workspace:

```text
train.csv ─┐
           ├─► notebook preprocessing ─► TF-IDF + numeric features ─► regressor ─► test_out.csv
test.csv ──┘

image_link ─► optional permitted downloader in src/utils.py ─► external image features
```

The current notebook imports TF-IDF, Ridge, LightGBM, sparse feature composition, and train/test splitting. `sample_code.py` is independent and produces a random format baseline.
