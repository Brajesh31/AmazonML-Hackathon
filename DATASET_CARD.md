# 📊 Dataset card

## 📌 Dataset identity
The repository contains CSV files under `dataset/` for the Smart Product Pricing challenge:
- `train.csv`: labeled examples.
- `test.csv`: examples without the target.
- `sample_test.csv`: small input-format example.
- `sample_test_out.csv`: output-format example.

The challenge brief describes approximately 75,000 training and 75,000 test records. This is descriptive context, not a substitute for measuring the checked-in files.

## 🧾 Schema
| Field | Train | Test | Description |
| --- | --- | --- | --- |
| `sample_id` | Yes | Yes | Sample identifier |
| `catalog_content` | Yes | Yes | Product title, description, and item-pack information |
| `image_link` | Yes | Yes | Product image URL |
| `price` | Yes | No | Target value |

## 🏷️ Provenance and rights
The files are associated with the challenge dataset supplied to participants. This repository does not establish independent ownership or redistribution rights for the challenge data or linked images. Review the challenge terms before copying, redistributing, or using the files outside the permitted competition context.

## 🚫 Prohibited enrichment
The challenge rules prohibit external price lookup. Do not append scraped retail prices, pricing API responses, manually researched prices, private price labels, or other external price-derived information.

## 🧪 Recommended quality checks
- Confirm schema, dtypes, row counts, nulls, and duplicate identifiers.
- Check target values for missing, non-finite, or non-positive values.
- Inspect duplicate catalog records and train/test overlap.
- Validate URL availability only where permitted.
- Keep preprocessing fitted on training folds.
- Preserve raw files and record checksums for experiments.

## 🔐 Storage and privacy
Do not commit credentials, private user data, cookies, or unrelated personal information. Keep temporary image downloads and derived artifacts outside Git unless the challenge and source terms permit redistribution.

## ⚠️ Known unknowns
This card does not independently verify dataset collection methodology, population coverage, demographic representation, image licensing, or long-term availability of source URLs. Consult the official challenge documentation for authoritative data terms.
