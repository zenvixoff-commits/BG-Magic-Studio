# BG Magic Studio

An independent browser-based AI background remover.

## Features
- Upload JPG/JPEG, PNG and WEBP (up to 15 MB), or drag and drop
- AI background removal in the browser
- Full-image preview with contain sizing (no preview crop)
- Transparent PNG export, JPG with a selected solid background, and WEBP export
- Quality control for JPG/WEBP
- Progress feedback, validation and errors
- No app backend, login, database, paid API or API key

## Run locally
Open this repository with VS Code and use a local web server such as Live Server. Browser ES modules work best on localhost or HTTPS.

## Deploy with GitHub Pages
In the repository, open **Settings → Pages**. Select **Deploy from a branch**, choose **main** and **/(root)**, then save. GitHub Pages will publish the root `index.html`.

## AI engine and performance
Uses `@imgly/background-removal` 1.5.5 in the browser. The Faster quantized model is about 40 MB; the Detailed model is about 80 MB. The first run may take time while model assets download. Later runs may be faster when browser cache is retained. Speed depends on the device and image dimensions. The app does not upload selected photos to an app server.

## Important
- PNG preserves transparency. JPG cannot, so the app composites it onto the selected background colour.
- WEBP can preserve transparency in compatible viewers.
- AI segmentation may still miss fine hair, sheer fabric or low-contrast edges on some images.
- The background-removal package is licensed under AGPL-3.0. Review its terms before public or commercial use: https://github.com/imgly/background-removal-js
