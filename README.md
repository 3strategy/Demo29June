# מרחב למידה בעברית

This repository contains a small Hebrew educational website built with Jekyll, GitHub Pages, and the pinned remote theme `just-the-docs/just-the-docs@v0.12.0`.

The intended workshop workflow is:

1. Edit Markdown files in this Windows folder.
2. Commit and push to GitHub.
3. Let GitHub Actions build and deploy the site to GitHub Pages.

Local Ruby, Bundler, Jekyll, WSL, or `bundle exec jekyll serve` are not required for this repository.

## Add a New Lesson

Create a new Markdown file in `lessons/`, for example `lessons/new-topic.md`.

Use this front matter:

```markdown
---
title: כותרת השיעור
layout: default
parent: שיעורים
nav_order: 3
permalink: /lessons/new-topic/
---
```

Then write the lesson content below the front matter. Keep the teaching text in Hebrew and use left-to-right text for commands, filenames, code, and technical tokens.

## Navigation

Navigation is controlled by each page's front matter:

- `title` sets the visible page title.
- `nav_order` controls ordering in the sidebar.
- `parent: שיעורים` places a lesson under the lessons section.
- `permalink` gives each page a stable URL.

The `lessons/index.md` page is marked with `has_children: true`, so lesson pages can appear beneath it.

Use Liquid's `relative_url` filter for internal links so the GitHub project-site base path works:

```markdown
[דף הבית]({{ '/' | relative_url }})
```

## Deployment

The workflow at `.github/workflows/pages.yml` builds the Jekyll site and deploys it to GitHub Pages whenever `main` is pushed.

To inspect a failed deployment:

1. Open the GitHub repository.
2. Select the `Actions` tab.
3. Open the latest `Deploy Jekyll site to GitHub Pages` run.
4. Expand the failing job and step.

Fix the repository files, commit, and push again. The deployment should be made green before considering a meaningful content change complete.

## Theme Version

The theme is pinned in `_config.yml`:

```yaml
remote_theme: just-the-docs/just-the-docs@v0.12.0
```

Change this version deliberately only after checking the Just the Docs release notes and confirming the GitHub Pages build still passes. Do not point the theme at `main`.

## Licensing Note

This public repository can be viewed by others, but public visibility does not automatically define a reuse license for the teacher's original content.

Third-party theme information is documented in `THIRD_PARTY_NOTICES.md`.

## Optional Local Preview

Advanced users who already have Ruby and Bundler working may choose to preview Jekyll locally, but that is not part of this workshop repository's required workflow. Do not spend workshop time installing or repairing Ruby, Bundler, Jekyll, WSL, or Linux packages for this project.
