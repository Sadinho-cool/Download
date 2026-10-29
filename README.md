# Y2Betok

**Y2Betok** is a clean, minimalist browser-based media-to-MP3 converter prototype.

## Current MVP
- Responsive interface with file picker and drag-and-drop
- Browser-side conversion using FFmpeg WebAssembly
- Progress feedback and MP3 download
- Media is not uploaded to a Y2Betok server

## Important boundaries
Y2Betok does **not** extract audio directly from YouTube URLs. Only convert media you own or are authorized to download and convert. For your own uploads, check whether download is available through [YouTube Studio](https://studio.youtube.com/). Respect copyright, permissions, and platform terms.

## Run locally
Serve this folder over HTTP (rather than opening the file with a `file://` URL). If Python is installed:

```bash
python -m http.server 8000
```

Visit http://localhost:8000.

## Publish with GitHub Pages
1. Open repository **Settings → Pages**.
2. Choose **Deploy from a branch**.
3. Select branch `main` and folder `/ (root)`.
4. Save and wait for deployment.

## Notes
- Internet is required to load FFmpeg WebAssembly from the CDN.
- Large files may be slow or exceed device memory.
- Conversion is client-side; this MVP does not require a Cloudflare Worker for media processing.
- Review dependency versions and licenses before production use.

## Files
- `index.html` — page structure
- `style.css` — responsive styling
- `script.js` — file selection and conversion logic
- `assets/favicon.svg` — Y2Betok icon