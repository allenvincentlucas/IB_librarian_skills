# IB Librarian Skills for Academic Success

A complete revision of the site into **seven thematic modules** instead of flat topic
pages — the "Reading Room" theme (sticky top navigation bar, dropdown menus,
forest-green + brass palette, serif/sans pairing) carries over unchanged; only the
content architecture changed.

## Site structure

```
_config.yml            site settings — baseurl already set to /IB_librarian_skills
_layouts/default.html   shared top-nav layout (Home / Modules dropdown / Citations)
assets/css/style.css    the "Reading Room" visual theme
assets/img/favicon.svg  the open-book favicon, on every page
index.md                homepage — "The IB Library as the Academic Hub"
modules/                the seven module pages
citations/index.md      links straight to each module's Works Cited section
```

## The seven modules

1. **IB Frameworks & Pedagogy** — ATL integration, IB Standards & Practices, the AASL/ISTE crosswalk
2. **High-Stakes Research & The Extended Essay** — MYP Personal Project, May 2027 EE changes, the research scaffolding matrix, Elicit/Scite/Zotero
3. **Academic Integrity & Generative AI** — the IB's AI policy and citation mechanics
4. **Student Life & Pastoral Care Librarianship** — Third Place theory, bibliotherapy, sensory rooms, inclusive clubs
5. **Collection Development & Diverse Literacies** — Scarborough's Reading Rope, SSST/multilingualism, CREW/MUSTIE weeding
6. **Systems, Makerspaces & PD Timeline** — makerspace budgeting, automation, the full Pre-Term → Term 3 plan, professional communities
7. **Systems & Emerging Practice** — Follett Destiny administration, copyright & fair use, accreditation frameworks (CIS/NEASC/WASC), using Claude/AI as a librarian workflow tool

Each module carries its own numbered in-text citations `[n]` matched to a Works Cited
list at the end of the page — every citation renders as a short labeled link
(**View source ↗**, **Watch video ↗**, **View PDF ↗**, **View DOI record ↗**) rather
than a raw URL in the page text.

## Publishing to GitHub Pages

This repo's `_config.yml` already has:
```yaml
baseurl: "/IB_librarian_skills"
url: "https://allenvincentlucas.github.io"
```

Replace the contents of the existing `IB_librarian_skills` repo with this folder's
contents, commit, and wait for the **Actions** tab to show a successful
"pages build and deployment" run. The live site stays at:

`https://allenvincentlucas.github.io/IB_librarian_skills/`

**If you ever rename the repo again:** update both `baseurl` and `url` in
`_config.yml` to match exactly (case-sensitive), or every internal link, the
stylesheet, and the favicon will resolve one path segment off.

## Running locally (optional)

Requires Ruby and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Adding new content later

- **New module:** add a Markdown file to `modules/` with the same front-matter pattern
  (`layout`, `title`, `permalink: /modules/your-slug/`), add it to the `Modules`
  dropdown in `_layouts/default.html`, and add a link to it on the homepage and on
  `citations/index.md`.
- The favicon and theme (colors, type, nav bar) live in `assets/img/favicon.svg` and
  `assets/css/style.css` — edit those once and every page updates.
- If you add Works Cited entries by hand later, keep URLs out of visible text: wrap
  them as `[View source ↗](https://example.com)` (or `Watch video ↗` / `View PDF ↗` /
  `View DOI record ↗` as fits) so pages stay uncluttered.
- Each module's in-text citation numbers and its own Works Cited list are
  self-contained (no shared numbering across modules) — if you add or remove a
  citation, renumber only within that one page.

## Source

Content originates from the "IB Librarian Skills for Academic Success" research
thread and two reference documents outlining the module structure and video resource
directory, compiled and reorganized July 2026.
