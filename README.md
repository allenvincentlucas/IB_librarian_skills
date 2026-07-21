# IB Librarian Skills for Academic Success

A single, complete Jekyll site: professional development plan, skills overview, research
scaffolding matrix, all eleven gap-research tracks, and the MLA citation record — in the
"Reading Room" design (persistent left sidebar, serif/sans pairing, forest-green + brass
palette).

Every citation and video reference renders as a short labeled link (**View source ↗**,
**Watch video ↗**, **View PDF ↗**, **View DOI record ↗**) rather than a raw URL printed
in the page text, so pages stay clean and readable.

## Site structure

```
_config.yml            site settings — url/baseurl already set for this repo name
_layouts/default.html  shared sidebar layout (nav, favicon, footer)
assets/css/style.css   the "Reading Room" visual theme
assets/img/favicon.svg the open-book favicon (green/brass), on every page
index.md               overview page — sidebar carries the actual navigation
pd-plan.md             core PD Plan (Pre-Term \u2192 Term 3 + Gap-Fill Addendum)
skills-overview.md     IB Secondary Librarian Skills & Resources
scaffolding-matrix.md  IB Research Skills Scaffolding Matrix (MYP 1 \u2192 DP 2)
gaps/                  all 11 gap-research pages (01\u201311)
citations/             index.md + two Works Cited subpages (PD Plan, Gaps 1\u20137)
```

Gaps 1\u20137 and their consolidated citation pages come from the original research thread.
Gaps 8\u201311 (Follett Destiny Administration, Copyright & Fair Use, Accreditation
Frameworks, and Using Claude/AI as a Librarian Workflow Tool) were researched directly
for this site and carry their own numbered Works Cited list at the end of each page.

## Publishing to GitHub Pages

1. Create a fresh repository named **`IB_librarian_skills`** and push this folder's
   contents to it (this matters: `_config.yml`'s `baseurl` is already set to
   `/IB_librarian_skills` to match — repo names are case-sensitive in the URL).
2. In the repo, go to **Settings \u2192 Pages**, and under "Build and deployment" choose
   **Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Wait for the **Actions** tab to show a successful "pages build and deployment" run,
   then visit the URL shown on the Settings \u2192 Pages screen.

**If you ever rename the repo or move to a `username.github.io` root site:** update both
`baseurl` and `url` in `_config.yml` to match, or every internal link, the stylesheet, and
the favicon will resolve one path segment off (this is the bug that broke the site
earlier).

## Running locally (optional, to preview before pushing)

Requires Ruby and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Adding new content later

- **New gap page:** add a Markdown file to `gaps/` with the same front-matter pattern
  (`layout`, `title`, `permalink: /gaps/your-slug/`), then add a sidebar entry for it in
  `_layouts/default.html`'s Gap Research nav-group.
- **New top-level page:** add a `.md` file at the repo root with the same front matter,
  then add a link to it in the sidebar.
- The favicon and theme (colors, type, sidebar) live in `assets/img/favicon.svg` and
  `assets/css/style.css` \u2014 edit those once and every page updates.
- If you add Works Cited entries by hand later, keep URLs out of visible text: wrap them
  as `[View source \u2197](https://example.com)` (or `Watch video \u2197` / `View PDF \u2197` /
  `View DOI record \u2197` as fits) so pages stay uncluttered.

## Source

Content originates from the "IB Librarian Skills for Academic Success" research thread
and companion notes, compiled July 2026.
