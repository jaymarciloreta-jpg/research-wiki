---
title: "How this wiki works"
tags: [reference, meta]
date: 2026-06-04
---

> Workflow and update model for the Rhinology & Skull Base literature wiki.

## What this is

A **living literature review** of rhinology, chronic rhinosinusitis (CRS) and skull base surgery, with a deliberate emphasis on **emerging technology** — devices, automation, AI, and outcomes. It is built as plain Markdown so it can live in your Obsidian vault and publish as a static site via **Quartz**.

## Structure

- `index.md` — home / map of content
- `Topics/` — eight curated topic pages, each a running list of publications (newest first)
- `Updates/` — dated digests; one per weekly run, so you can see *what's new* at a glance
- `Resources/` — the exact search queries (`Search Strategy`), key journals, and the machine-readable `.search-queries.json`
- `00-About/` — this page

Every publication links to its **PubMed** record and **DOI**. Topic pages cross-link via `[[wikilinks]]`, so the Quartz graph view shows how themes connect.

## Update cadence — weekly (automated)

A scheduled task runs **every Monday**. Each run:

1. Executes the eight topic queries in [[Search Strategy]] against PubMed, filtered to the **trailing 7 days** (entry date).
2. De-duplicates against PMIDs already in the wiki.
3. Fetches metadata for genuinely new papers and writes a one-line plain-language takeaway.
4. Appends them to the relevant `Topics/` pages (newest first) and updates the counts.
5. Creates a new `Updates/YYYY-MM-DD — Weekly digest.md` summarizing the week.

If a week has no new papers in a topic, that topic is simply skipped in the digest.

## Manual supplementation

PubMed under-indexes pure-engineering and industry work. The non-PubMed sources (FDA clearances, arXiv/IEEE robotics & vision papers, society guidance) are tracked under the relevant topic pages and listed in [[Search Strategy]]. Add anything you find by hand — the format is just a Markdown bullet.

## Publishing with Quartz

See `README.md` in this folder for the one-time Quartz setup. In short: point Quartz's `content` at this folder (or symlink it), run `npx quartz build --serve` to preview, and deploy to GitHub Pages or Netlify.

---
*Primary index: PubMed (NCBI E-utilities). This wiki is an information resource, not medical advice.*
