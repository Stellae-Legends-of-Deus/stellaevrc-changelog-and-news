# stellaevrc-changelog-and-news

News posts and map changelogs for [stellaevrc.website](https://stellaevrc.website). The site reads this repo directly: push a file to `main` and it shows up on the site within a few minutes (admins can also press Refresh content in the admin panel).

## News

One Markdown file per post in `news/`, named `YYYY-MM-DD-slug.md`. The slug becomes the URL: `news/2026-11-16-welcome.md` is shown at `stellaevrc.website/news/welcome`.

```markdown
---
title: Welcome to Stellae
summary: One or two sentences shown in news lists.
author: Sketch494
cover: images/welcome.webp      # optional, path in this repo or an https URL
tags: [announcement]            # optional
draft: false                    # optional, true hides the post
---

Post body in Markdown.
```

## Map changelogs

One file per release in `changelog/<map>/`, named `YYYY-MM-DD-version.md`. The folder name is the map's ID.

```markdown
---
map: The Hub                    # display name of the map
version: 0.1.0
title: First public build       # optional
---

### Added
- New thing

### Changed
- Changed thing

### Fixed
- Fixed thing
```

## Images

Put images in `images/` and reference them as `images/name.webp` in front matter or `![alt](images/name.webp)` in the body. Keep them under 1 MB.

## Rules

- Dates come from the filename unless the front matter sets `date: YYYY-MM-DD`.
- Files whose name starts with `_` are ignored, so `_template.md` is safe to keep around.
