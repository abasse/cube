# Isometric Cube Builder

A zero-dependency, single-file HTML tool for building and exporting isometric cube diagrams. Runs entirely in the browser — no build step, no server, no installation required.

## Features

### Cubes
- Add up to **64 cubes**
- Auto-arrange into the smallest fitting supercube, or choose a stacking direction (horizontal X, depth Y, vertical Z)
- **Custom position mode** — place each cube at any `[X, Y, Z]` coordinate on the isometric grid for sparse or freeform layouts
- **Remove individual cubes** from any position without losing the rest
- **Gap slider** — control the spacing between cubes uniformly across all three dimensions
- **Scale slider** — zoom the entire scene in or out

### Appearance
- **Per-cube color** — set the top face color with a color picker; left and right face shading is derived automatically to simulate 3D lighting
- **Flat shading** — disable automatic shading and use the same color on all three faces
- **Stroke width** — control the edge line thickness (0 removes strokes entirely)
- **Stroke color** — choose any color for the edges
- **Rounded corners** — smooth the parallelogram corners with a radius slider
- **Shadow** — toggle a soft blurred drop shadow that follows the cube shape
- **Background color** — set the canvas background to any color

### Text Labels
- Add a text label to any cube
- Use `_` as a line break — `Content_Store` renders as two lines
- Choose which face the text appears on: **Left**, **Right**, **Top**, or **All sides**
- **Text size slider** — global font size applied to all cubes
- Text color automatically switches between black and white based on the face's luminance (WCAG contrast)
- **Auto number** — automatically fill each cube's label with its number (1, 2, 3…)

### Interaction
- **Click a cube** to select it — highlights it in the scene and scrolls to its entry in the sidebar
- **Double-click** or use the **Deselect all** button to clear the selection
- **Drag to reorder** cube entries in the sidebar using the `⠿` handle

### Persistence & Export
- All settings are **automatically saved** to `localStorage` and restored on page load
- **Save JSON** — export the full configuration to a `.json` file
- **Load JSON** — restore a configuration from a saved `.json` file
- **Export SVG** — save the rendered scene as a scalable `.svg` file
- **Clear saved settings** — reset everything to defaults (with confirmation)

## Usage

1. Open `index.html` in any modern browser
2. Use the sidebar to configure cubes, colors, labels, and layout
3. Export as SVG when done

No internet connection required. No dependencies.

## Sidebar Reference

| Control | Description |
|---|---|
| Cubes | Number of cubes (1–64) |
| Stack | Auto / Horizontal X / Depth Y / Vertical Z arrangement |
| Custom positions | Enable per-cube X/Y/Z coordinate inputs |
| Gap | Spacing between cubes (0–1) |
| Text | Global font size for labels (4–40px) |
| Scale | Scene zoom (0.2×–3×) |
| Auto number | Pre-fill cube labels with their index |
| Stroke | Edge line width (0 = no stroke) |
| Stroke color | Edge line color |
| Rounded | Corner radius for cube faces |
| Flat shading | Disable automatic face shading |
| Shadow | Soft drop shadow behind cubes |
| Background | Canvas background color |

## Per-Cube Controls

Each cube entry in the sidebar has:

| Control | Description |
|---|---|
| `⠿` handle | Drag to reorder |
| Color swatch | Top face color (sides derived automatically) |
| `✕` button | Remove this cube |
| Text input | Label text (`_` = line break) |
| Face dropdown | Which face(s) to show the label on |
| X / Y / Z inputs | Custom grid position (visible in custom mode) |

## File Structure

```
index.html   — the entire application (HTML + CSS + JS, single file)
README.md    — this file
```

## Browser Support

Works in any modern browser (Chrome, Firefox, Safari, Edge). No polyfills needed.
