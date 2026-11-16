# 🖼️ Image data and responsible handling

The challenge data includes `image_link` and suggests visual features as an option. The notebook currently does not implement image feature extraction or image-model training.

## 🧰 Existing helper
`src/utils.py` provides `download_image` and `download_images`. The collection helper starts 100 workers and uses `urlretrieve` without explicit timeouts, retry/backoff, checksums, or structured failure reporting. This is aggressive and risks throttling or partial downloads.

## 🛡️ Safe practice
- Confirm challenge rules and source terms before accessing images.
- Never use image URLs to obtain product prices.
- Do not bypass authentication, throttling, CAPTCHAs, or access controls.
- Prefer bounded concurrency, timeouts, exponential backoff, and caching in a revised downloader.
- Keep downloaded images and embeddings outside Git unless redistribution is permitted.
- Record missing-image handling and provenance.

## 🔬 Future experiments
A visual model must meet challenge licensing and parameter constraints and be evaluated on the same validation split as text/tabular candidates. No image-model score is claimed here.
