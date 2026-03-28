# jekyll-conversion

Convert the site from plain copy-pasted HTML files to Jekyll so that shared elements (header, nav, footer, contact CTA) only exist in one place and site-wide settings (email, Calendly URL) are defined once.

## Problem

Every page duplicated the same header, footer, contact section, and script tags. Changing the nav or email address meant editing every file individually.

## What changed

- `_layouts/default.html` — single template wrapping all pages (head, header, footer, scripts)
- `_includes/header.html`, `footer.html`, `cta.html` — shared components edited once
- `_config.yml` — site-wide settings (email, Calendly link, title)
- All 6 pages converted to use Jekyll front matter; only their unique content remains
- `Gemfile` added for local development via `bundle exec jekyll serve --livereload`
- `EDITING.md` added as a plain-English guide for non-technical content updates
- `README` renamed to `README.md` with site overview and dev instructions
