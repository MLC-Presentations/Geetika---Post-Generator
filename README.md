# MLC Social Post Generator

A self-contained, browser-based tool for creating on-brand social media graphics for MLC Presentation Design Consulting. Open the HTML file in any modern browser — no server, no install, no internet connection required after the first download.

## What you can do

Build a post for any major social platform (LinkedIn square / portrait, Instagram square / portrait / story, Twitter, Facebook, YouTube thumbnail) starting from one of six on-brand templates. Then:

- **Edit every text element** directly on the canvas — drag to move, pull the corner to resize the wrap width, recolor from a five-swatch palette (black / yellow / white / grey / custom), toggle single-line vs auto-wrap.
- **Place a brand icon or illustration** from the 115-element library extracted from the MLC Brand Guidelines deck. Drag, scale, reorder.
- **Place a photo** from the company team-shoot library. Crop to rectangle, square, circle or rounded-square, pan and zoom inside the crop, or hit "Fit to post" to make it a full-bleed background.
- **Add a gradient overlay** that fades from 0% to 100% transparency in any color and direction — perfect for darkening a photo so text stays readable on top.
- **Reorder layers** in the Layers panel. Drag any element up to bring it forward or down to send it back. Eye icon hides/shows.
- **Align elements** — Shift+click two or more elements on the canvas and use the six alignment buttons (Left / Center / Right / Top / Middle / Bottom). With a single selection, align to the post edges; with multiple, the first selection is the reference.
- **Switch theme** Light / Dark — text colors auto-flip for readability while explicit user-set colors are preserved.
- **Undo / redo** every change with the buttons or Cmd/Ctrl+Z.
- **Export PNG** at the platform's native pixel size, ready to upload.

## How to use

1. Download (or `git clone`) this repository.
2. Keep all four files together in the same folder:
   - `mlc-social-post-generator.html`
   - `mlc-svg-library.js`
   - `mlc-image-library.js`
   - `html2canvas.min.js`
3. Double-click `mlc-social-post-generator.html` to open it in your browser.
4. Pick a platform size at the top of the left panel, then a template. Edit the text, add images, drag things around. Click **Download PNG** when you're done.

That's it. Nothing else needs to be installed.

## Brand identity

Visuals follow MLC's house style: white background, black as the structural workhorse, yellow (`#FFDB46`) as the signature accent — never more than ~20% of the visual weight. Gilroy is the primary typeface with Aptos as fallback. No emoji, no rainbow charts, no Office drop shadows.

## What's in the repository

| File | What it is |
|---|---|
| `mlc-social-post-generator.html` | The whole app — UI, rendering, state, export. |
| `mlc-svg-library.js` | 83 icons + 32 illustrations from the brand deck, base64-inlined. |
| `mlc-image-library.js` | 63 team photos, resized to 1200 px on the long edge and JPEG-encoded for offline use. |
| `html2canvas.min.js` | Bundled rendering library (v1.4.1) so the PNG export works offline. |
| `.gitignore` | Excludes the heavy source assets and the SSH setup. |
| `README.md` | This file. |

## Editing the libraries

If you want to add new icons, illustrations, or photos, the libraries are produced by short Python scripts. The originals are NOT in the repo (they're large and the inlined versions are sufficient at runtime). Ask Maurizio for the source folders.

## Browser compatibility

Chrome, Edge, Firefox, Safari — current versions all work. The PNG export uses the html2canvas library which renders the DOM to a canvas. Images, gradients, SVGs and the yellow highlighter scribble all render correctly to the exported PNG.

## License

Internal MLC tool. Not for redistribution outside the team.
