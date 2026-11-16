# ✅ Model and submission validation checklist

## 🧪 Before training
- [ ] Challenge rules and dataset terms reviewed.
- [ ] Raw input files remain unchanged.
- [ ] Schema, IDs, missing values, duplicates, and target values inspected.
- [ ] Validation split and seed fixed.
- [ ] Preprocessing is fit only on training folds.

## 🌲 Before accepting a model
- [ ] Training completed without hidden exceptions.
- [ ] Validation predictions are finite.
- [ ] Target transformation is inverted correctly.
- [ ] SMAPE implementation is tested and documented.
- [ ] Model and feature parameters are recorded.
- [ ] Results are compared on the same validation records.
- [ ] Error analysis and known limitations are recorded.
- [ ] Model license and challenge parameter limits are checked.

## 📤 Before submission
- [ ] Exactly `sample_id,price` columns in the required order.
- [ ] Test row count matches output row count.
- [ ] Test IDs appear exactly once.
- [ ] No missing, unexpected, or duplicate IDs.
- [ ] Prices are finite and strictly positive.
- [ ] Output was read back and validated.
- [ ] Methodology description reflects actual implementation.
- [ ] No external price lookup or prohibited enrichment occurred.
- [ ] Code revision, experiment record, and output checksum are saved.
