# image-includes

Replace inline image markup with named Jekyll includes so that adding, removing, or swapping images on content pages requires no knowledge of the template's CSS grid classes.

## Problem

Every image on a content page required knowing the HTML5 UP grid system (`col-4 col-12-narrower imp-narrower`, `gtr-50`, etc.) and whether to use float, a column div, or an inline style. This made adding or repositioning an image slow and error-prone.

## What changed

Two includes added to `_includes/`:

**`img-sidebar.html`** — right-column image alongside text (col-4 width, stacks on mobile)
- Required: `src` (filename from `images/`), `alt` (description)
- Optional: `caption` (text or HTML rendered below the image)

**`img-full.html`** — full-width image spanning the section container
- Required: `src`, `alt`

All existing inline image blocks updated to use the includes:
- `signs.html` — 3 sidebar images
- `orton-gillingham.html` — 1 full-width, 1 sidebar
- `index.html` — Celia sidebar with caption

`EDITING.md` updated with copy-paste templates for both patterns, plus instructions for updating an existing photo.

## Usage

```liquid
{% include img-sidebar.html src="photo.jpg" alt="Description" %}
{% include img-sidebar.html src="photo.jpg" alt="Description" caption="Caption text" %}
{% include img-full.html src="photo.jpg" alt="Description" %}
```
