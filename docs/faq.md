# FAQ

## Is `sample_code.py` a real model?

No. It returns random prices between 5 and 500 and exists only to demonstrate the expected output shape.

## What metric should I optimize?

The challenge uses SMAPE. Lower values are better; implement a stable local evaluator and document how zero or near-zero targets are handled.

## Can I scrape prices from product pages?

No. External price lookup and price-related web scraping are explicitly prohibited by the challenge.

## Should notebook checkpoints be committed?

No. Checkpoints and `__pycache__` files are transient and are ignored by the repository policy. Keep reproducible source notebooks and scripts instead.
