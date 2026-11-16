# 🤝 Contributing

Thank you for helping improve the AmazonML Hackathon workspace. Contributions should improve correctness, reproducibility, clarity, or responsible use of the supplied challenge data.

## 🧭 Before opening a change
- Read the root [README](README.md), [data guide](docs/data.md), [methodology guide](docs/methodology.md), and [security rules](SECURITY.md).
- Understand the challenge's fair-play restrictions.
- Keep raw datasets immutable.
- Do not introduce external product prices, price scraping, pricing API results, manually researched price labels, or other prohibited price-derived information.
- Check licenses and parameter limits before adding pretrained models.

## 🧪 Engineering expectations
- Prefer small, focused changes.
- Use repository-relative paths, explicit configuration, and deterministic seeds.
- Put reusable helpers in `src/`.
- Add tests for parsing, feature construction, metrics, and submission validation when changing those areas.
- Fit learned preprocessing only on training folds.
- Record data/code revision, split, model parameters, validation SMAPE, runtime, and memory use.
- Keep images, caches, model checkpoints, embeddings, and generated matrices outside Git.

## 📓 Notebook changes
- Restart the kernel and execute changed cells in order.
- Remove stale error outputs or clearly document unresolved failures.
- Avoid machine-specific paths.
- Do not report stored cell output as a fresh run.

## 🔀 Pull request checklist
- [ ] The change is scoped and explained.
- [ ] Challenge rules and data permissions are respected.
- [ ] Relevant tests or checks were run.
- [ ] Validation split and metric are documented for model changes.
- [ ] No secrets, private data, or unnecessary generated artifacts are included.
- [ ] README and technical docs reflect actual behavior.
