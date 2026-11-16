# 🧰 Feature engineering guide

## 🔤 Catalog text
The notebook lowercases text, replaces non-ASCII alphanumeric characters with spaces, collapses whitespace, then uses word-level TF-IDF with up to 5,000 features, English stop words, and unigram/bigram terms.

Possible experiments, not implemented claims: character n-grams for part numbers, careful punctuation preservation, unit normalization, separate title/description fields when parsing is reliable, and vocabulary comparisons on a fixed validation split.

## 📦 Quantity extraction
The current function takes the last integer-like token and defaults to 1. It can mistake years, model IDs, dimensions, and unrelated counts for pack quantity. Improve with context-aware patterns, tests for decimals/multipacks, explicit ambiguity indicators, and retained raw text.

## ⚖️ Mass and volume
The current parser takes the first match among `kg`, `g`, `l`, `ml`, and `oz`. It places mass and volume into one feature even though they are different quantities. A robust design should separate mass and volume, retain unit family, and test compound packaging.

## 🖼️ Images
The notebook does not create image embeddings or train a visual model. The helper only downloads image files. Future visual modeling must comply with challenge permissions, source terms, model license, and parameter limits.

## 🧪 Validation
Fit vectorizers and learned transformations on training folds only. Keep the same transforms for validation/test, and inspect missing values, outliers, vocabulary drift, and feature dimensions.
