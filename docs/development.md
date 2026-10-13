# Development

Use small, reviewable experiments and keep raw data unchanged. Extract reusable feature functions into `src/`, record random seeds, and prefer scripts or notebooks that accept an explicit data directory.

Validate every submission with:

1. Exact output columns `sample_id` and `price`.
2. Equal row count to `dataset/test.csv`.
3. No missing or duplicate IDs.
4. Positive finite predictions.
5. A documented validation SMAPE.

Do not compare models using the hidden test set. Use a fixed training validation split or cross-validation and document the choice.
