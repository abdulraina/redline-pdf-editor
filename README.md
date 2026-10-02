# Redline PDF Editor

A free PDF editor that runs entirely in the browser. Files never leave the user's device.

## Features

- **Edit existing text** with automatic font, weight, style and color detection
- **Add text** in 37 font families (embedded in the saved PDF)
- Draw, highlight, white-out, rectangles, ellipses, lines and arrows
- Insert images and add signatures (drawn or typed)
- Reorder, rotate, duplicate, delete and insert pages; merge other PDFs
- Undo/redo, zoom, keyboard shortcuts, mobile layout, light and dark themes

## Deploy on Render (free)

1. Push this folder to a GitHub repository.
2. In the [Render dashboard](https://dashboard.render.com), choose **New → Blueprint**.
3. Connect the repository. Render reads `render.yaml` and creates a static site.
4. Click **Apply**. Your editor goes live at `https://redline-pdf-editor.onrender.com`
   (or a similar URL if the name is taken).

Every push to the main branch redeploys automatically.

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

Opening `index.html` directly from disk will not load the fonts; use a local server.

## Project layout

| Path         | Contents                                                      |
|--------------|---------------------------------------------------------------|
| `index.html` | The whole editor (HTML, CSS and JavaScript)                   |
| `lib/`       | PDF.js 3.11.174, pdf-lib 1.17.1, @pdf-lib/fontkit 1.1.1       |
| `fonts/`     | TrueType files for the 34 embeddable font families            |
| `render.yaml`| Render static-site configuration                              |

## Licenses

- Editor code: MIT (see `LICENSE`)
- PDF.js, pdf-lib, fontkit: Apache 2.0 / MIT, by their respective authors
- Fonts: SIL Open Font License 1.1 or Apache 2.0 (Google Fonts)
