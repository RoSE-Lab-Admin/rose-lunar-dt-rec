# Project page — Lunar Analog CRPNVS (iSpaRo 2026)

Static GitHub Pages site for the paper "A Reproducible Reconstruction and Evaluation Framework for Photorealistic Lunar Analog Scene Reconstruction Toward Digital Twins."

This is already a local git repo (`git log` to see history).

## Assets

`assets/gifs/` and `assets/images/` hold the web-ready media the page links to:
- `rover_pov_in_reconstructed_dt_isaac_sim.mp4` (+ poster) — hero video, rover POV in the reconstructed DT
- `human_controlled_capture.mp4` (+ poster) — Method section, operator performing the human-controlled capture (replaces `n_shaped_camera_sweep.mp4`, which is no longer referenced)
- `pipeline_figure.jpg` — Method section, full pipeline diagram
- `training_metrics_misleading.jpg` — motivating figure right after the abstract
- `3_panel_crpnvs_comparison.jpg`, `coverage_score_explains_why_scene3_better_than_scene2.png` — Results section
- `conops_montage.mp4` (+ poster) — Simulation-Ready Digital Twins section, ball drop / splat vs mesh / lidar montage
- `sensor_sim_ros2_lidar.mp4` (+ poster) — Simulation-Ready Digital Twins section, Nova Carter lidar streamed to RViz over ROS 2
- `wheel_terrain_interaction.mp4` (+ poster) — Simulation-Ready Digital Twins section, rover on granular terrain with the splat DT as backdrop

Original `.gif`/`.pdf` source exports stay on disk but are gitignored (see `.gitignore`) — they're large and unused by the page directly, since it links the compressed `.mp4`/`.jpg`/`.png` versions instead. To add another figure: drop the source file in `assets/`, convert if needed (`ffmpeg` for gif→mp4, `pdftoppm -png -r 200 file.pdf out` for pdf→png), then reference it from `index.html` with a relative path inside a `.figure-card` (see existing `<figure>` blocks for the pattern).

## To do before publishing
- [ ] Fill in the paper link (arXiv or camera-ready PDF) — currently "coming soon" in two places (hero buttons + Resources section)
- [ ] Fill in the real BibTeX entry once the proceedings citation exists — currently a placeholder in the Citation section
- [ ] Double check author names/order and affiliations
- [ ] Review the rephrased abstract and figure captions against the camera-ready paper for accuracy

## Publish under RoSE-Lab-Admin

1. Create the repo on GitHub under the org (via the web UI: github.com/organizations/RoSE-Lab-Admin/repositories/new), name suggestion: `lunar-crpnvs-page` — rename as you like. Do not initialize it with a README/license (this repo already has one).
2. From this folder, run: git branch -M main && git remote add origin https://github.com/RoSE-Lab-Admin/lunar-crpnvs-page.git && git push -u origin main
3. In the new repo on GitHub: Settings > Pages > Source > Deploy from branch > `main` / `/ (root)` > Save.
4. Page will be live at: https://rose-lab-admin.github.io/lunar-crpnvs-page/
5. Optional: Settings > General > add a description and the same URL as the repo's "website" field so it shows up on the org's repo list.

## Updating later
Edit files, then: git add -A && git commit -m "Update project page" && git push
