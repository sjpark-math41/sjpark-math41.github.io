# Changelog

## 2026-07-20 — Site-wide settings and portability

- Added Open Graph and social-card metadata.
- Added a default social preview image and favicon.
- Added `robots.txt` with the public sitemap location.
- Added back-to-top navigation and nested-page breadcrumbs.
- Refined site search configuration.
- Added external-link indicators.
- Restricted Quarto rendering to public `.qmd` content and excluded `templates/`.
- Prevented repository management Markdown files from becoming hidden website pages.
- Added `.editorconfig` and `.gitattributes` for consistent Windows/macOS editing.
- Added a practical repository `README.md`.

## 2026-07-20 — Teaching and seminars system

- Added automatic listings for Teaching and Seminars.
- Added shared directory metadata for teaching and seminar pages.
- Added reusable templates for course records and seminar presentations.
- Added a public Summer 2026 teaching-assistant record for Calculus and Vector Analysis (2).
- Added draft seminar records for Large Deviations Chapter 8 and Brownian Motion Chapter 3.
- Added a conservative public-materials policy for teaching content.
- Updated the content guide, roadmap, and site status.

## 2026-07-20 — Notes authoring system

- Added common defaults in `notes/_metadata.yml`.
- Added a reusable long-form mathematical note template.
- Added standard metadata, date, tag, folder, and draft conventions.
- Added reusable visual blocks for definitions, theorems, propositions, lemmas, corollaries, examples, remarks, and proofs.
- Added `CONTENT-GUIDE.md`.
- Added and updated project status and roadmap documentation.
- Restricted the Notes listing to note folders whose main document is `index.qmd`.

## 2026-07-20 — Profile integration

- Added the public academic profile of Sungjun Park.
- Added Korean and English name display.
- Added Yonsei University affiliation and public email.
- Added research interests and education history.
- Replaced the empty project section with a transparent research-in-development statement.
- Added centralized reusable values in `_variables.yml`.
- Refactored duplicated light/dark layout rules into `styles/_shared.scss`.
- Added a temporary profile placeholder pending the actual portrait file.

## 2026-07-20 — Initial rebuild

- Rebuilt the website as a Quarto project.
- Added Home, About, Research, Notes, Teaching, Seminars, and CV.
- Added light and dark themes.
- Added GitHub Pages deployment through GitHub Actions.
