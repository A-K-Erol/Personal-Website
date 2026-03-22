# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal portfolio website for Ansel K. Erol, built on the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme. Deployed via GitHub Pages on the `gh-pages` branch with the custom domain `ansel.fyi` (configured in `CNAME`). GitHub Actions (`.github/workflows/deploy.yml`) builds the Jekyll site and pushes the result to `gh-pages` automatically on push.

## Local Development

Requires Ruby + Bundler. From the repo root:

```bash
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`. Docker is also supported via `docker-compose.yml`.

## Key Files to Edit

| File | Purpose |
|------|---------|
| `_config.yml` | Site-wide settings, scholar config, feature toggles |
| `_pages/about.md` | Home page bio and profile configuration |
| `_data/socials.yml` | Social media links shown in header/footer |
| `_bibliography/papers.bib` | Publications (rendered by jekyll-scholar) |
| `_projects/*.md` | Individual project cards |
| `_news/*.md` | Announcements shown on the home page |
| `_pages/passions.md` | Custom passions page with inline HTML/CSS |
| `_pages/cv.md` | CV page (links to `assets/pdf/Ansel_Erol_Resume.pdf`) |

## Site Structure

- **Home** (`/`) — `_pages/about.md` — bio, news feed, selected publications
- **Publications** (`/publications/`) — auto-generated from `_bibliography/papers.bib` via jekyll-scholar
- **Projects** (`/projects/`) — cards from `_projects/`, categories: `research` and `software`
- **Passions** (`/passions/`) — custom page with travel, food, music, cats, poetry sections
- **CV** (`/cv/`) — links to resume PDF in `assets/pdf/`

## Assets

- Profile photo: `assets/img/prof_pic.jpg`
- Project images: `assets/img/projects_*.{png,jpg}`
- Travel/food/cat/music images: `assets/img/`
- Audio clips: `assets/audio/pie_jesu.mp3`, `assets/audio/quia_respexit.mp3`
- Resume PDF: `assets/pdf/Ansel_Erol_Resume.pdf`

The `images/` and `audio/` root directories are legacy copies from the old static site and are excluded from the Jekyll build.

## Publications

`_bibliography/papers.bib` uses standard BibTeX. The `scholar.last_name` / `scholar.first_name` fields in `_config.yml` bold the author's name automatically. Add `selected = {true}` to a BibTeX entry to feature it on the home page.

## Navbar Order

1. about (home)
2. publications
3. projects
4. passions
5. CV

All other pages in `_pages/` have `nav: false`.
