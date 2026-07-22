# Apply the chapter-based Notes structure

This package is designed for the `main` branch of:

`sjpark-math41/sjpark-math41.github.io`

## Files included

- `_quarto.yml` — preserves the current site configuration and adds the Notes stylesheet and page navigation.
- `notes/index.qmd` — replaces the subject-based Notes landing page with a chapter-based landing page.
- `notes/filtrations-and-martingales/index.qmd` — new chapter page.
- `notes/filtrations-and-martingales/section-1-1/filtrations-right-continuity-completeness.qmd` — first published learning unit.
- `styles/notes-structure.css` — styles for chapter cards, section lists, and learning-unit pages.

## Apply in VS Code

1. Open the local repository folder.
2. Copy the contents of this package into the repository root.
3. Allow `_quarto.yml` and `notes/index.qmd` to be overwritten.
4. Delete the old placeholder directory:

   ```powershell
   Remove-Item -Recurse -Force notes/getting-started
   ```

5. Preview the site:

   ```powershell
   quarto preview
   ```

6. Check these routes:

   - `/notes/`
   - `/notes/filtrations-and-martingales/`
   - `/notes/filtrations-and-martingales/section-1-1/filtrations-right-continuity-completeness.html`

7. Commit and push to `main`. The existing GitHub Actions deployment should render the Quarto project and publish it.

## Recommended commit message

```text
Add chapter-based notes structure and first filtration unit
```

## Content model for later units

Create one `.qmd` file for each learning unit under the relevant section directory:

```text
notes/
└── filtrations-and-martingales/
    ├── index.qmd
    └── section-1-1/
        ├── filtrations-right-continuity-completeness.qmd
        ├── measurable-adapted-progressive.qmd
        └── regular-adapted-processes-progressive.qmd
```

When a planned unit is written, add its link to the unit row in the chapter `index.qmd` and change the status from `Planned` to `Published`.

## Math delimiter correction

Quarto/Pandoc math must use `$...$` for inline mathematics and `$$...$$` for display mathematics. This corrected package replaces the unsupported `\\(...\\)` and `\\[...\\]` delimiters that caused TeX commands such as `\\Omega`, `\\sigma`, `\\le`, and `\\infty` to disappear.
