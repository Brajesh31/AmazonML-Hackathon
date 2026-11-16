# 🗃️ Data storage model

## 📌 No database service
The project does not use a relational database, document database, or ORM. Challenge inputs and outputs are CSV files; experiments use pandas dataframes and sparse matrices.

## 🧾 Logical records
| Record | Key | Fields |
| --- | --- | --- |
| Training row | `sample_id` | `catalog_content`, `image_link`, `price` |
| Test row | `sample_id` | `catalog_content`, `image_link` |
| Submission row | `sample_id` | `price` |

## 🔐 Data integrity
Keep raw inputs immutable. Preserve identifiers through transformations. Validate uniqueness and row alignment before exporting predictions. Do not put prohibited external data into derived datasets.

## 🔮 Future consideration
Experiment metadata storage may be useful later, but it is not part of the current repository.
