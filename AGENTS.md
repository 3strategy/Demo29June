# Project Agent Notes

## Site Purpose

This repository is a small Hebrew educational website built with Jekyll, GitHub Pages, and the pinned remote theme `just-the-docs/just-the-docs@v0.12.0`.

## Content Layout

- Main pages live at the repository root, such as `index.md` and `about.md`.
- Lesson pages live in `lessons/`.
- The lessons landing page is `lessons/index.md` and uses `has_children: true`.
- Local styling overrides belong in `_sass/custom/custom.scss`.
- GitHub Pages deployment lives in `.github/workflows/pages.yml`.

## Required Front Matter

Every Markdown page must include front matter. Typical root page:

```yaml
---
title: Page title
layout: default
nav_order: 1
permalink: /page-url/
---
```

Typical lesson page:

```yaml
---
title: כותרת השיעור
layout: default
parent: שיעורים
nav_order: 1
permalink: /lessons/example/
---
```

## Hebrew and RTL

- The site is primarily Hebrew and right-to-left.
- Keep prose, headings, tables and navigation readable in RTL.
- Keep code blocks, terminal commands, filenames, URLs, inline code and technical tokens left-to-right.
- Use `relative_url` for internal links so the GitHub project-site base path works.

## Theme Boundaries

- Do not fork, clone or copy the full Just the Docs theme into this repository.
- Do not copy theme layouts or assets unless a small targeted override is truly required.
- Keep `remote_theme` pinned to an explicit version; do not use the theme's `main` branch.

## Privacy and Safety

- Do not commit private student, parent, staff or school data.
- Do not commit secrets, tokens, credentials or private deployment data.
- Public repository visibility does not automatically license the teacher's original content for reuse.

## Verification

- Every meaningful change must leave the GitHub Pages build passing.
- Required workflow: edit files, commit, push, and inspect the GitHub Actions deployment result.
- Local WSL, Ruby, Bundler, Jekyll, `gem`, `bundle`, and `bundle exec jekyll serve` are not part of this workshop repository's required workflow.
- Do not run WSL, Ruby, Bundler, Jekyll or related installers for this project unless the user explicitly changes the workshop constraint.

## Git Guidance

After this initial setup, future agents may read the repository but must not commit, pull or push unless the user explicitly asks.

## Notifications

After each user prompt, run:

```powershell
& 'C:\Users\3stra\.codex\notify.ps1' -Title "Codex - Demo29June - " -Message "<prompt title> Finished"
```
