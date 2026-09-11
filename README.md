# Project page — Lunar Analog CRPNVS (iSpaRo 2026)

Static GitHub Pages site for the paper "A Reproducible Reconstruction and Evaluation Framework for Photorealistic Lunar Analog Scene Reconstruction Toward Digital Twins."

This is already a local git repo (`git log` to see history). Add images/gifs here, then push it to GitHub.

## Adding images / gifs

Drop files into `assets/images/` or `assets/gifs/`, then reference them in `index.html` with a relative path, e.g. `<img src="assets/images/reconstruction-compare.png" alt="...">`.

The header currently uses a CSS placeholder (`.hero-figure`) standing in for a teaser figure. To swap in a real teaser image or GIF, replace this block in `index.html`:
```html
<div class="hero-figure" role="img" aria-label="..."></div>
```
with:
```html
<img class="hero-figure" src="assets/gifs/teaser.gif" alt="Qualitative reconstruction comparison across traversal conditions">
```
(the `.hero-figure` CSS class already sets width/height/border — an `<img>` with that class will fill the same slot; add `object-fit:cover` to the class if the media's aspect ratio doesn't match).

Keep images web-sized (compress PNGs, keep GIFs short/small — GitHub Pages has no CDN optimization) so the page loads fast.

## To do before publishing
- [ ] Add real images/GIFs to `assets/` and wire them into `index.html` (teaser figure at minimum)
- [ ] Fill in the paper link (arXiv or camera-ready PDF) — currently "coming soon" in two places (hero buttons + Resources section)
- [ ] Fill in the real BibTeX entry once the proceedings citation exists — currently a placeholder in the Citation section
- [ ] Double check author names/order and affiliations
- [ ] Review the rephrased abstract on the page against the camera-ready abstract for accuracy

## Publish under RoSE-Lab-Admin

1. Create the repo on GitHub under the org (via the web UI: github.com/organizations/RoSE-Lab-Admin/repositories/new), name suggestion: `lunar-crpnvs-page` — rename as you like. Do not initialize it with a README/license (this repo already has one).
2. From this folder, run: git branch -M main && git remote add origin https://github.com/RoSE-Lab-Admin/lunar-crpnvs-page.git && git push -u origin main
3. In the new repo on GitHub: Settings > Pages > Source > Deploy from branch > `main` / `/ (root)` > Save.
4. Page will be live at: https://rose-lab-admin.github.io/lunar-crpnvs-page/
5. Optional: Settings > General > add a description and the same URL as the repo's "website" field so it shows up on the org's repo list.

## Updating later
Edit files, then: git add -A && git commit -m "Update project page" && git push
