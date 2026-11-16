# ❓ Frequently asked questions

## Is this a production pricing API?
No. It is a notebook-led machine-learning challenge workspace. No HTTP API or deployed inference service is implemented.

## Is `sample_code.py` a trained model?
No. It generates random prices solely to demonstrate the expected output format.

## Does the notebook train LightGBM successfully?
The saved notebook output contains a TypeError for the supplied `early_stopping_rounds` argument. Resolve compatibility and rerun before relying on the result.

## Does this repository contain image-model code?
No. It contains an image downloader helper, but no image feature extraction or image-model training.

## Can external product prices be collected?
No. The challenge brief explicitly prohibits external price lookup and scraping.

## Is a database used?
No. The project uses CSV datasets and in-memory pandas/SciPy processing.

## What is the evaluation metric?
SMAPE. See [evaluation](evaluation.md).

## Where should generated artifacts go?
Use a local output/cache directory. Keep downloaded images, model checkpoints, feature matrices, and temporary files out of Git.
