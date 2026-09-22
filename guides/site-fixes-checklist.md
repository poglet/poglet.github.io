---
layout: default
title: Site Fixes Checklist
parent: Guides
nav_enabled: true
---

# Site Fixes Checklist

A list of items to correct the issues found in this repository, covering SEO blockers, broken/stub content, and site configuration.

## Critical (site is misconfigured)

- [ ] Fix `_config.yml`:
  - [ ] Change `title` from "Just the Docs Template" to the real site name
  - [ ] Change `url` from `https://just-the-docs.github.io` to `https://poglet.github.io`
  - [ ] Write a real `description` (150–160 characters)
  - [ ] Remove the `aux_links` entry pointing at the template repository
- [ ] Verify the site title, URL, and description render correctly after the config change

## SEO basics

- [ ] Add the `jekyll-sitemap` plugin (add to `Gemfile` and `plugins` in `_config.yml`)
- [ ] Add a `robots.txt` that allows crawling and references the sitemap
- [ ] Add a unique `description` front matter value to every guide page
- [ ] Add `sitemap: false` (or complete/remove) stub pages so they are not indexed
- [ ] Verify canonical URLs and Open Graph tags render correctly with the theme's SEO tag

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
