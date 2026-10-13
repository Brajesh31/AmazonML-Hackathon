# Data model

The challenge uses CSV files rather than a database. The core fields are:

| Field | Meaning |
| --- | --- |
| `sample_id` | Unique sample identifier |
| `catalog_content` | Product title, description, and item-pack quantity text |
| `image_link` | Public product-image URL |
| `price` | Training target; absent from test inputs |

Keep train and test schemas aligned except for the target. Do not infer price from external data. Preserve the provided sample output as the formatting reference.
