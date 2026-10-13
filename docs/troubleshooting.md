# Troubleshooting

## Notebook cannot find the dataset

The notebook contains a machine-specific absolute path. Replace it with a path based on the repository root, such as `Path("dataset") / "train.csv"`.

## LightGBM is unavailable

Install the project dependencies in the active virtual environment and confirm the notebook kernel uses that environment. If LightGBM is not required for an experiment, remove or isolate the import rather than silently changing the model.

## Output is rejected

Compare the output with `dataset/sample_test_out.csv`. Check exact column names, row count, ID coverage, duplicate IDs, missing values, finite values, and positive prices.

## Image downloads are slow or fail

Use only permitted URLs, reduce concurrency, add retries with backoff, cache results outside Git, and stop when the source requests throttling. The challenge forbids external price lookup.
