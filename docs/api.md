# 🔌 Local Python interfaces

This repository does not expose a network API, web server, or hosted prediction endpoint.

## 🖼️ Image helpers
- `src.utils.download_image(image_link, savefolder)`: attempts to download one image if it is not already present. Failures are printed rather than returned as structured results.
- `src.utils.download_images(image_links, download_folder)`: processes links using a multiprocessing pool of 100 workers. This is aggressive and should be replaced with bounded concurrency, timeouts, retries/backoff, and structured results before routine use.

## 🧪 Demonstration predictor
`sample_code.predictor(sample_id, catalog_content, image_link)` returns a random float between 5 and 500. It does not load a trained model.

## 🚫 Not implemented
There are no REST/GraphQL routes, authentication endpoints, database interfaces, model-serving API, or batch inference service.
