# Young Minds Literacy & Learning

Website for [Young Minds Literacy & Learning](https://mexicoDyslexiaServices.github.io) — a dyslexia and literacy therapy practice offering assessment, therapy, and consultation services in Mexico, the U.S., and virtually worldwide.

## Pages

| File | URL | Description |
|------|-----|-------------|
| `index.html` | `/` | Home page — overview of services and team |
| `about.html` | `/about` | Meet the team |
| `services.html` | `/services` | Services and pricing |
| `signs.html` | `/signs` | Signs of dyslexia by age group |
| `orton-gillingham.html` | `/orton-gillingham` | What dyslexia is and how OG intervention works |
| `misconceptions.html` | `/misconceptions` | Common dyslexia myths (embedded Canva slides) |

## Making edits

See [EDITING.md](EDITING.md) for a plain-English guide to common updates (team bios, nav, contact info, etc.).

Site-wide settings like the contact email and Calendly link live in `_config.yml` — change them once and they update everywhere.

## Local development

This site uses [Jekyll](https://jekyllrb.com/) and is hosted on GitHub Pages. Jekyll processes the HTML templates before serving — you can't just open the files directly in a browser.

**First time setup** (requires Ruby):
```bash
bundle install
```

**Start the local server:**
```bash
bundle exec jekyll serve --livereload
```

Then open [http://localhost:4000](http://localhost:4000). The site will automatically reload when you save a file.

**To stop the server:** `Ctrl-C`

## Tech stack

- [Jekyll](https://jekyllrb.com/) — templating and build (hosted natively on GitHub Pages, no CI needed)
- [HTML5 UP "Twenty" theme](https://html5up.net/twenty) — base design template
- jQuery + Font Awesome — bundled in `assets/js/` and `assets/css/`
- Plain HTML pages — no React, no build step beyond Jekyll
