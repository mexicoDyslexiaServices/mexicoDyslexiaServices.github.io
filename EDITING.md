# Editing Guide

## Site-wide settings (email, Calendly link, site name)
Edit `_config.yml` — changes here apply everywhere automatically.

## Navigation (header links)
Edit `_includes/header.html`

## Contact CTA section (the "Contact us" block at the bottom of every page)
Edit `_includes/cta.html`

## Footer logos
Edit `_includes/footer.html`

---

## Team members (`_team/`)

Each person on the About page is a file in `_team/`. To edit someone's bio, open their file and edit the text below the `---` line. The front matter (between the `---` lines at the top) holds their name, title, and photo filename.

**To add a team member:**
1. Drop their photo into the `images/` folder
2. Copy any existing `_team/` file, rename it with the next number prefix (e.g. `04-newperson.md`)
3. Update the name, credentials, photo filename, and bio

**To remove a team member:**
1. Delete their file from `_team/`
2. Delete their photo from `images/`

## Services (`_services/`)

Each service (Assessment, Therapy, Consultation) is a file in `_services/`. The `summary` list appears on the home page; the `details` list appears on the Services page. Edit either list by adding, removing, or changing the `- "..."` lines.

**To update pricing:** find the relevant `details` entry and change the price text at the end of the line.

## Articles / "Discover more" cards (`_articles/`)

Each card in the "Discover more about learning differences" section on the home page is a file in `_articles/`. The blurb text goes below the `---` line; the image, link, and title are in the front matter above.

**To add a new card:** create a new file like `05-new-topic.md` with the same structure as the others. The number prefix controls the order.

**To link to an external site:** add `external: true` to the front matter.

---

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

## Images

**Step 1 — Add the file:** drop the photo into the `images/` folder.

**Step 2 — Add it to a page** using one of these copy-paste templates:

### Image on the right, text on the left
```liquid
<div class="row gtr-50">
  <div class="col-8 col-12-narrower aln-left">

    Your text content here.

  </div>
  {% include img-sidebar.html src="your-photo.jpg" alt="Describe the photo here" %}
</div>
```

### Image on the right with a caption beneath it
```liquid
<div class="row gtr-50">
  <div class="col-8 col-12-narrower aln-left">

    Your text content here.

  </div>
  {% include img-sidebar.html src="your-photo.jpg" alt="Describe the photo" caption="Caption text here" %}
</div>
```

### Full-width image (spans the whole section)
```liquid
<div class="row gtr-50">
  {% include img-full.html src="your-photo.jpg" alt="Describe the photo here" %}
</div>
```

**To update an existing photo:** replace the file in `images/` with the new one using the same filename, or update the filename in the relevant `_team/`, `_articles/`, or page file.
