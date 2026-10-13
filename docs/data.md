# Data documentation

The challenge provides approximately 75,000 training products and 75,000 test products. Training data includes `price`; test data does not. The catalog text may contain quantities and units, which the notebook parses into derived `quantity` and `weight` features.

## Quality checks

- Confirm `sample_id` uniqueness and train/test overlap expectations.
- Inspect missing text and image links.
- Normalize units consistently and record assumptions.
- Check target outliers and positive-value constraints.
- Avoid fitting transformations on the hidden test target or using prohibited external prices.

Keep downloaded images and intermediate feature matrices outside source control.
