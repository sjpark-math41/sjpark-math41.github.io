# Content Guide

This file records the minimum rules for adding and maintaining site content.

## 1. General naming rules

Use lowercase English folder names with hyphens.

```text
good:
large-deviations
thermodynamic-limit
continuous-time-markov-chains

avoid:
Large Deviations
새 노트
note 1
```

The public title may contain spaces, capitalization, Korean, and mathematical notation. Only the file and folder names follow the English slug rule.

## 2. Adding a mathematical note

### Step 1 — Copy the template

Copy:

```text
templates/note/
```

to a destination such as:

```text
notes/large-deviations/thermodynamic-limit/
```

The final source file must be:

```text
notes/large-deviations/thermodynamic-limit/index.qmd
```

### Step 2 — Edit metadata

At the top of `index.qmd`, edit:

```yaml
title:
description:
date:
date-modified:
categories:
status:
draft:
```

Use `draft: true` while the note is not ready to appear publicly. Change it to `draft: false` when publishing.

### Step 3 — Write and preview

Run:

```text
quarto preview
```

Check the table of contents, equations, links, light mode, dark mode, and narrow mobile width.

### Step 4 — Publish

In GitHub Desktop:

```text
Fetch/Pull → Commit → Push
```

## 3. Adding a teaching record

Copy:

```text
templates/teaching-course/
```

to:

```text
teaching/<course-slug>-<year>-<term>/
```

Record the institution, term, role, overview, responsibilities, and only publicly distributable materials.

Do not publish:

- Student names, email addresses, grades, or submissions
- Internal announcements
- Restricted textbook scans or substantial exercise collections
- Answer keys not intended for public release

## 4. Adding a seminar record

Copy:

```text
templates/seminar/
```

to:

```text
seminars/<year>/<presentation-slug>/
```

Use the presentation date in ISO format and keep `draft: true` while materials are under preparation.

After the presentation:

1. Update `status` from `Scheduled` to `Completed`.
2. Update `date-modified`.
3. Add slides, handouts, or related notes.
4. Change `draft` to `false` when the page is ready to publish.

## 5. Standard subject names

Use these category names consistently:

- Probability Theory
- Stochastic Processes
- Large Deviations
- Interacting Particle Systems
- Real Analysis
- Algebra
- Research Notes
- Site Guide

A note may have one primary subject and several narrower topic tags.

Example:

```yaml
categories:
  - Large Deviations
  - Gibbs Measures
  - Thermodynamic Limit
```

## 6. Date policy

- `date`: first public or substantive creation date, or the scheduled presentation date
- `date-modified`: most recent meaningful content revision
- Do not update `date-modified` for a typo-only edit

Use the ISO format:

```text
YYYY-MM-DD
```

## 7. Mathematical writing

Use inline mathematics with:

```text
\(X_t\)
```

Use displayed mathematics with:

```text
$$
I(x)=\sup_{\theta\in\mathbb{R}}
\{\theta x-\Lambda(\theta)\}.
$$
```

Use ordinary headings in hierarchical order:

```text
## Section
### Subsection
#### Small subdivision
```

Do not skip heading levels for visual effect.

## 8. Definitions, theorems, and remarks

Use the reusable blocks included in the note template:

```markdown
::: {.definition}
### Definition

...
:::
```

Available classes:

- `definition`
- `theorem`
- `proposition`
- `lemma`
- `corollary`
- `remark`
- `example`
- `proof-box`
- `note-status`

These provide visual consistency but do not create automatic theorem numbering. Ordinary numbered section headings remain the primary navigation system.

## 9. Images and files

Store item-specific files next to the source page:

```text
notes/subject/note-slug/
├── index.qmd
├── images/
└── files/
```

The same convention applies to teaching and seminar records.

Use descriptive image names and always supply alt text.

```markdown
![Description of the mathematical diagram](images/diagram-name.svg)
```

## 10. Links

Use relative project links.

```markdown
[Related note](../other-note/index.qmd)
```

After moving or renaming a page, check all inbound links before pushing.

## 11. Working across Windows and macOS

At the beginning of work:

```text
GitHub Desktop → Fetch origin → Pull origin
```

At the end of work:

```text
Save → Commit → Push origin
```

Do not edit the same page independently on both computers before syncing.

## 12. Content that should not be duplicated

- Profile and education: `_variables.yml`
- Global navigation and site metadata: `_quarto.yml`
- Shared visual styling: `styles/`
- Note-wide defaults: `notes/_metadata.yml`
- Teaching-wide defaults: `teaching/_metadata.yml`
- Seminar-wide defaults: `seminars/_metadata.yml`

Change the central source rather than copying the same information into several pages.
