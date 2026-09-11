# Project page — Lunar Analog CRPNVS (iSpaRo 2026)

Static GitHub Pages site for the paper "A Reproducible Reconstruction and Evaluation Framework for Photorealistic Lunar Analog Scene Reconstruction Toward Digital Twins."

## To do before publishing
- [ ] Add a real teaser image/GIF in `assets/` and replace the placeholder `.teaser` block in `index.html` with an `<img>` tag
- [ ] Fill in the paper link (arXiv or camera-ready PDF) — currently "coming soon" in two places (hero buttons + Resources section)
- [ ] Fill in the real BibTeX entry once the proceedings citation exists — currently a placeholder in the Citation section
- [ ] Double check author names/order and affiliations
- [ ] Review the rephrased abstract on the page against the camera-ready abstract for accuracy

## Publish under RoSE-Lab-Admin

1. Create the repo on GitHub under the org (via the web UI: github.com/organizations/RoSE-Lab-Admin/repositories/new), name suggestion: `lunar-crpnvs-page` — rename as you like.
2. From this folder, run: git init && git add -A && git commit -m "Add project page for iSpaRo 2026 paper" && git branch -M main && git remote add origin https://github.com/RoSE-Lab-Admin/lunar-crpnvs-page.git && git push -u origin main
3. In the new repo on GitHub: Settings > Pages > Source > Deploy from branch > `main` / `/ (root)` > Save.
4. Page will be live at: https://rose-lab-admin.github.io/lunar-crpnvs-page/
5. Optional: Settings > General > add a description and the same URL as the repo's "website" field so it shows up on the org's repo list.

## Updating later
Edit `index.html` directly, then: git add -A && git commit -m "Update project page" && git push
