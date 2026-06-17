# Stereograms

A small, dependency-free static webpage for viewing a recreated USGS-style stereogram. The page shows the original side-by-side stereograph, a thumbnail view, and an animated GIF version of the scene.

The project is based on the USGS stereograms multimedia gallery:

- https://www.usgs.gov/products/multimedia-gallery/stereograms
- https://www.easystereogrambuilder.com/

## Project Structure

```text
.
|-- index.html
|-- assets/
|   |-- animate_this_01.jpg
|   |-- animate_this_thumbnail.jpg
|   `-- animated.gif
`-- README.md
```

## How to Run

No build step or package install is required. Open `index.html` directly in a browser:

```powershell
start .\index.html
```

You can also use any local static server if you prefer:

```powershell
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## What the Page Does

- Displays the original stereograph from `assets/animate_this_01.jpg`.
- Switches to `assets/animate_this_thumbnail.jpg` when the thumbnail view is selected.
- Switches to `assets/animated.gif` when animation is enabled.
- Provides buttons to animate, show the thumbnail, stop animation, and return to the original image.

## Editing the Viewer

The project is intentionally contained in one file:

- HTML markup, page styles, and JavaScript are all in `index.html`.
- Image assets live in `assets/`.
- Button behavior is controlled by the `showOriginal`, `showThumbnail`, and `showAnimation` functions near the bottom of `index.html`.

To add another stereogram, place the new image files in `assets/` and update the `src` and `alt` attributes in `index.html`.

## Accessibility Notes

The images include descriptive `alt` text, the button group has an accessible label, and the animation notice warns that the GIF may flash. If you add new animated assets, keep that warning accurate for the new content.
