# Sungjun Park — Academic Website

Personal academic website built with Quarto and deployed to GitHub Pages.

- Live site: <https://sjpark-math41.github.io>
- Repository: <https://github.com/sjpark-math41/sjpark-math41.github.io>

## Main tools

- Quarto
- GitHub Pages
- GitHub Actions
- Bootstrap 5
- Custom SCSS
- MathJax

## Local preview

Open the repository folder in VS Code and run:

```text
quarto preview
```

Stop the preview server with:

```text
Ctrl + C
```

Before publishing, a full local render may be checked with:

```text
quarto render
```

## Routine workflow on Windows and macOS

### Before editing

1. Open GitHub Desktop.
2. Select this repository.
3. Click `Fetch origin`.
4. Click `Pull origin` if it appears.
5. Open the repository in VS Code.

### After editing

1. Save all files in VS Code.
2. Run `quarto preview`.
3. Check the affected pages in light and dark mode.
4. Stop the preview.
5. Review changed files in GitHub Desktop.
6. Write a concise commit summary.
7. Click `Commit to main`.
8. Click `Push origin`.
9. Confirm that the GitHub Actions deployment succeeds.

Do not edit the same files independently on both computers before syncing.

## Primary source files

```text
_quarto.yml        Global website settings
_variables.yml     Reusable profile and education information
index.qmd          Home page
about.qmd          About page
research/          Research section
notes/             Mathematical notes
teaching/          Teaching records
seminars/          Seminar records
cv/                Web CV
styles/            Light, dark, and shared SCSS
templates/         Source templates; not rendered as public pages
```

## Adding content

Detailed conventions are recorded in:

```text
CONTENT-GUIDE.md
```

Current implementation status is recorded in:

```text
SITE-STATUS.md
ROADMAP.md
CHANGELOG.md
```

These management files are repository documentation and are excluded from website rendering.

## Deployment

A push to the `main` branch triggers:

```text
.github/workflows/publish.yml
```

The workflow renders the Quarto project and deploys `_site` to GitHub Pages.

## Generated files

The following are generated locally and should not be committed:

```text
_site/
.quarto/
```

They are excluded through `.gitignore`.
