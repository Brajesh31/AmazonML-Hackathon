# 📊 Data dictionary and governance

| Field | Train | Test | Meaning |
| --- | --- | --- | --- |
| `sample_id` | Yes | Yes | Unique sample identifier |
| `catalog_content` | Yes | Yes | Product title, description, and pack information |
| `image_link` | Yes | Yes | Product image URL |
| `price` | Yes | No | Prediction target |

The challenge brief describes roughly 75,000 records per split. Verify actual local row counts before publishing statistics.

## 🔎 Data quality checks
- Validate expected columns and data types.
- Check missing and duplicate `sample_id` values.
- Inspect blank catalog text and missing image links.
- Check training target nulls, non-finite values, and non-positive values.
- Measure duplicate descriptions and train/test overlap.
- Inspect text lengths and measurement patterns.
- Confirm consistent preprocessing across train, validation, and test.

## 🚫 Leakage and prohibited information
The challenge rules prohibit external price lookup, including price scraping and pricing APIs. Do not add online prices, private price databases, or manually researched labels. Fit learned preprocessing on training folds only.

## 💾 Storage policy
Keep raw CSV files unchanged. Store temporary downloads, embeddings, caches, fitted models, and predictions in a local output directory. Do not publish data or images unless redistribution rights are established.
