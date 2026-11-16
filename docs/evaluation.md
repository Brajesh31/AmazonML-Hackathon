# 📏 Evaluation and validation

## 🧮 SMAPE
```text
SMAPE_i = 2 * abs(prediction_i - actual_i) / (abs(actual_i) + abs(prediction_i))
SMAPE = mean(SMAPE_i) * 100
```
This matches the challenge's formula. The brief states a range of 0% to 200%, with lower being better.

## ⚠️ Zero denominator
When both actual and predicted values are zero, the denominator is zero. The challenge brief does not define a local implementation convention. Document the choice and confirm the official evaluator's behavior if possible.

## 🧪 Validation protocol
1. Split labeled training data only.
2. Fix and record the split seed and strategy.
3. Fit text vectorizers and learned preprocessing on training folds only.
4. Compare candidates on identical validation rows.
5. Report overall SMAPE and useful error slices.
6. Keep the hidden test set for final predictions only.

## 📊 Report more than one number
Record data/code revision, feature and model parameters, metric implementation, SMAPE, runtime, memory use, and invalid prediction count. Audit duplicate leakage, target inversion, and split drift before trusting a low score.
