# API

There is no HTTP API. The local Python interfaces are:

- `src.utils.download_image(image_link, savefolder)` downloads one image URL when permitted.
- `src.utils.download_images(image_links, download_folder)` downloads a collection using multiprocessing.
- `sample_code.predictor(sample_id, catalog_content, image_link)` returns a baseline price.

The downloader should be treated as an external-network utility with throttling, licensing, and challenge-rule implications.
