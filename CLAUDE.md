# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

A [Hugo](https://gohugo.io) static site (digital garden) using the [PaperMod](https://github.com/adityatelange/hugo-PaperMod/) theme, hosted on GitHub Pages at https://andGarc.github.io/ag/.

## Common Commands

```bash
# Run local dev server (includes draft posts)
hugo server -D

# Create a new post
hugo new content/posts/my-post-name.md

# Build the site (output goes to public/)
hugo
```

## Architecture

- `hugo.yaml` — site configuration (base URL, theme, menus, params)
- `content/posts/` — all blog posts as Markdown files with TOML front matter
- `content/archives.md` and `content/search.md` — special pages for the Archive and Search nav items
- `archetypes/default.md` — template used when creating new posts with `hugo new`
- `themes/PaperMod/` — theme as a git submodule (do not modify directly)
- `public/` — built output (committed to `gh-pages` branch via CI)

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yaml`, which builds the site with Hugo and pushes the output to the `gh-pages` branch. The `public/` directory in `main` is the local build output and is not used for deployment.

## Post Front Matter

Posts use TOML front matter. The full template is in `content/posts/template.md`:

```toml
+++
title = 'Post Title'
date = 2024-01-01T00:00:00-05:00
draft = true
tags = ['']
Description = ''
ShowToc = false
weight = 0
+++
```

Set `draft = false` to publish. Use `weight = 1` for pinned/featured posts.
