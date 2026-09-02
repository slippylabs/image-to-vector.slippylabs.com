# Image to Vector Converter

Trace a PNG, JPEG or BMP into real scalable geometry and download it as SVG, EPS or DXF. Contour tracing, colour quantisation and Bezier fitting, all in your browser.

**Live:** <https://image-to-vector.slippylabs.com/>

## What it does

- Trace a PNG, JPEG or BMP into real scalable geometry.
- Black & white, grayscale or full colour output, at four trace resolutions.
- Export as SVG, EPS or DXF, or copy the SVG source.

## How it works

The pipeline is colour quantisation, then contour tracing to get closed paths out of the pixel regions, then **Bézier curve fitting** over those contours — so the output is smooth curves rather than a staircase of one-pixel line segments dressed up as a vector file. The DXF and EPS writers emit the geometry directly, which is what makes the result usable in CAD and a cutter rather than just in a browser.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/image-to-vector.slippylabs.com.git
cd image-to-vector.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
