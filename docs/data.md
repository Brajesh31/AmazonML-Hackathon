# 📊 Data documentation

| Field | Train | Test | Purpose |
| --- | --- | --- | --- |
| `sample_id` | Yes | Yes | Stable identifier |
| `catalog_content` | Yes | Yes | Product description and pack details |
| `image_link` | Yes | Yes | Image URL |
| `price` | Yes | No | Target |

The challenge brief estimates about 75k records per split; verify local row counts before publishing exact statistics.

Check schema, dtypes, nulls, duplicate IDs, duplicated descriptions, target validity, train/test overlap, text length, and unit patterns. External price lookup and price scraping are prohibited. Fit learned transformations on training folds only. Keep raw CSVs immutable and generated artifacts outside Git.
