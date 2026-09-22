---
layout: default
title: Site Fixes Checklist
description: A working checklist of SEO and configuration fixes needed for this Jekyll site, covering _config.yml, sitemaps, robots.txt, and per-page meta descriptions.
parent: Guides
nav_enabled: true
sitemap: false
---

# Site Fixes Checklist

A list of items to correct the issues found in this repository, covering SEO blockers, broken/stub content, and site configuration.

## Critical (site is misconfigured)

- [x] Fix `_config.yml`:
  - [x] Change `title` from "Just the Docs Template" to the real site name
  - [x] Change `url` from `https://just-the-docs.github.io` to `https://poglet.github.io`
  - [x] Write a real `description` (150–160 characters)
  - [x] Remove the `aux_links` entry pointing at the template repository
- [ ] Verify the site title, URL, and description render correctly after the config change (requires deploy)

## SEO basics

- [x] Add the `jekyll-sitemap` plugin (add to `Gemfile` and `plugins` in `_config.yml`)
- [x] Add a `robots.txt` that allows crawling and references the sitemap
- [x] Add a unique `description` front matter value to every guide page
- [x] Add `sitemap: false` (or complete/remove) stub pages so they are not indexed
- [ ] Verify canonical URLs and Open Graph tags render correctly with the theme's SEO tag (requires deploy)

## Google Search Console

- [ ] Create/verify a Google Search Console property for `poglet.github.io`
- [ ] Submit the sitemap (`/sitemap.xml`)
- [ ] Check the Coverage report and fix any errors or excluded pages
- [ ] Monitor Search Performance for indexed pages and impressions

## Content and page fixes

- [ ] Rename `SWAT4-multipalyer-setup.md` (fixes the "multipalyer" typo) to something like `swat-4-sef-multiplayer-setup.md`
- [ ] Update any internal links/front matter that reference the old SWAT 4 filename
- [ ] Fill or remove the `installation.md` stub (currently contains only "Blah blah")
- [ ] Complete or `nav_exclude` the `learning-to-solder.md` guide (empty placeholder sections)
- [ ] Flesh out thin guides with unique, detailed content (target 1,500+ words where possible)
- [ ] Add descriptive `alt` text to all images
- [ ] Add internal links between related guides (e.g., Windows 98 ↔ My Old Computer)
- [ ] Add keyword-focused titles and H1s for long-tail search terms per guide

## Technical SEO

- [ ] Confirm the site is served over HTTPS and loads quickly
- [ ] Compress large images (prefer WebP / under ~200KB)
- [ ] Confirm mobile-friendly rendering with the Just the Docs theme
- [ ] Fix any broken external links in existing guides

## Ongoing

- [ ] Publish new, genuinely useful guides regularly
- [ ] Build backlinks by sharing helpful guides where they are on-topic (e.g., relevant subreddits)
- [ ] Track rankings in Search Console and refine titles for pages that get impressions but few clicks
