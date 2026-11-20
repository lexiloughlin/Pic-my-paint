# 🖌️ Paint My Photo

Upload one of your photos, choose how many colors you want to paint with, and get:

- a **simplified reference image** in just those colors
- **matching swatches**, numbered, with a color name and hex code
- a **printable paint-by-number template**: outlines with a number in every shape, plus a color key page

Everything runs in the browser. Photos never leave your device.

## Use it

Open `index.html`, or visit the GitHub Pages site for this repo once Pages is turned on
(Settings → Pages → Deploy from a branch → `main`).

1. Drop in a photo (or try the sample picture).
2. Pick the number of colors (3 to 30) and a detail level.
3. Click a swatch to see where that color goes.
4. Print the template and color key, or download them as PNGs.

## How it works

1. The photo is scaled down and its colors are grouped with k-means clustering in Lab color space, so the groups match how eyes see color.
2. A smoothing pass turns speckle into clean shapes, and shapes too small to paint are folded into their neighbors.
3. Each shape gets its number at the roomiest spot inside it.

It is a single file with no dependencies.
