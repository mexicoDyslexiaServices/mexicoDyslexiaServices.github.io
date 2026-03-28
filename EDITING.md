# Editing Guide

## Site-wide settings (email, Calendly link, site name)
Edit `_config.yml` — changes here apply everywhere automatically.

## Navigation (header links)
Edit `_includes/header.html`

## Contact CTA section (the "Contact us" block at the bottom of every page)
Edit `_includes/cta.html`

## Footer logos
Edit `_includes/footer.html`

## Page content
Each page is its own file at the root:
- `index.html` — Home page
- `about.html` — About / Meet the Team
- `services.html` — Services and pricing
- `signs.html` — Signs of dyslexia
- `orton-gillingham.html` — What is Orton-Gillingham
- `misconceptions.html` — Dyslexia misconceptions

Each page starts with a small block at the top (called "front matter") that looks like:
```
---
layout: default
title: Page Title
---
```
Don't edit that block — just edit the HTML content below it.

## Adding a new team member
Open `about.html` and copy one of the existing team member blocks (between `<!-- Tica -->` and `<!-- Ellie -->`).

## Images
Drop new image files into the `images/` folder, then reference them as `/images/your-file.jpg` in the HTML.
