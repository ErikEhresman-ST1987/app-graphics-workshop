# Sprite Factory — Feasibility Prototype 01

This repository replaces the abandoned App Graphics Workshop working tree. Previous code remains accessible in Git history at commit `bb8a90d145c900ae30ffe3f170e71af20c8698b5`.

## Goal
On an iPad, import a white-background illustration, remove white areas connected to the image border, fit into an exact-size canvas, and export a **verified** WebP file with transparency.

## Limitations
This is a technical experiment, not the finished Sprite Factory. Edge-connected flood fill can leave halos, remove white regions connected to the outside, and cannot clean complex shadows. It preserves enclosed white details. The browser's WebP encoder is feature-detected and the resulting RIFF/WEBP signature is checked. If Safari cannot encode WebP, the test reports failure instead of silently substituting PNG. No batch processing, presets, offline service worker, or alpha-channel validation is implemented yet.

## Acceptance test
1. Open the GitHub Pages site in iPad Safari.
2. Import a ChatGPT-generated illustration with white background.
3. Process at 512 × 512, inspect checkerboard edges.
4. Download; verify the image opens, has transparent background, and matches requested dimensions.
5. Report success or the exact failure message.

No existing code was retained in the working tree; the prior commit history remains available.
