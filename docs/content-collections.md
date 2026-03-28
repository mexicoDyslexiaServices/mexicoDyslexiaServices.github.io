# content-collections

Extract hardcoded content from HTML pages into Jekyll Collections so that team bios, services, and article cards can be edited as simple Markdown files without touching any HTML.

## Problem

Team bios, service bullet points, and article cards were hardcoded in HTML pages. Adding a team member or updating pricing meant editing raw HTML, and the "Discover more" article cards on the home page were entirely copy-pasted with no shared structure.

## What changed

Three Jekyll Collections added, each as a folder of Markdown files:

**`_team/`** — one file per team member
- `featured: true` marks the owner (Celia), who gets a distinct layout on the About page
- Bio prose goes in the Markdown body; a `<!-- break -->` comment splits the col-8 bio from the full-width closing paragraph
- Specialists (Tica, Ellie) loop into a two-column grid automatically
- Adding a new member = drop a new `.md` file in the folder

**`_services/`** — one file per service (Assessment, Therapy, Consultation)
- `summary` list feeds the home page preview cards
- `details` list feeds the full Services page
- `icon` holds the Font Awesome class used in both places
- Updating pricing = edit one line in one file

**`_articles/`** — one file per "Discover more" card on the home page
- `external: true` adds `target="_blank" rel="noopener noreferrer"` automatically
- Cards loop in pairs into rows; adding a new card = new file, no HTML changes

`_config.yml` updated to register all three collections with `output: false` (no individual pages generated).

`EDITING.md` updated with plain-English instructions for all three collections.

`.gitignore` added to exclude Jekyll build artifacts (`_site/`, `.jekyll-cache/`, `.sass-cache/`) and macOS metadata (`.DS_Store`). Both `.DS_Store` files were removed from git tracking.
