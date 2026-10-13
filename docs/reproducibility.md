# Reproducibility

Record the Python version, package versions, operating system, random seeds, dataset checksums, feature parameters, model parameters, validation split, and SMAPE result for each experiment.

Avoid absolute paths such as the one currently embedded in `AmazonML.ipynb`. Use `pathlib.Path` and a configurable repository root. Save model artifacts and downloaded images outside Git, and keep a small manifest of generated outputs so another contributor can reproduce a run without access to private state.
