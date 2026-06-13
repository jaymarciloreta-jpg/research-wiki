# Rhinology & Skull Base Literature Wiki

A living, weekly-updated literature review of **rhinology, chronic rhinosinusitis, and skull base surgery**, emphasizing **emerging technology** — devices, automation, AI, and outcomes. Authored as Obsidian-flavored Markdown and designed to publish as a static site with [Quartz](https://quartz.jzhao.xyz/).

## Contents

| Path | What it holds |
|------|---------------|
| `index.md` | Home / map of content |
| `Topics/` | 8 curated topic pages (newest publication first) |
| `Updates/` | Dated digests — one per weekly run |
| `Resources/` | Search queries, key journals, `.search-queries.json` |
| `00-About/` | How the wiki works |

Currently seeded with **58 publications** from a 12-month backfill (Jun 2025 → Jun 2026).

## Weekly automation

A scheduled task runs every Monday: it re-runs the eight PubMed queries (trailing 7 days), de-duplicates against existing PMIDs, appends new papers to the topic pages, and writes a new digest in `Updates/`. See `00-About/How this wiki works.md`.

## Publishing with Quartz (one-time setup)

Quartz v4 requires Node 20+.

```bash
# 1. Clone Quartz somewhere outside this vault
git clone https://github.com/jackyzha0/quartz.git
cd quartz && npm install

# 2. Point Quartz at this folder as its content source.
#    Easiest: symlink the vault into quartz/content
rm -rf content
ln -s "/Users/jaymarc/Dropbox/Pharyvac Vault/Projects/Pharyvac Surgical Technologies/research/Chronic Sinusitis and Skull base literature review" content

# 3. Preview locally
npx quartz build --serve         # http://localhost:8080

# 4. Deploy (GitHub Pages / Netlify / Cloudflare Pages)
npx quartz build                 # outputs static site to ./public
```

### Recommended `quartz.config.ts` tweaks

- `pageTitle`: `"Rhinology & Skull Base Literature Wiki"`
- Enable the **graph view** and **full-text search** plugins (defaults in Quartz) — the `[[wikilinks]]` between topic pages and tags (`#ai`, `#robotics`, `#biologics`, …) will populate both.
- Set `ignorePatterns` to include `build_wiki.py` and `.search-queries.json` if you don't want them rendered.
- `enableSPA: true` and `enablePopovers: true` give the wiki-style hover previews.

> Note: `index.md` uses Obsidian wikilinks (`[[Note Title]]`). Quartz resolves these by note title, which matches the filenames here. If you prefer Hugo/Jekyll instead, convert wikilinks to relative Markdown links first.

## Regenerating from scratch

`build_wiki.py` (in the outputs folder of the session that created this) holds the curated dataset and renders every page deterministically. Re-running it overwrites the topic pages — edit the `E = [...]` list to curate.

---
*Primary literature index: PubMed (NCBI E-utilities). Supplementary: FDA device database, arXiv/IEEE, Google Scholar, society guidance. This wiki is an information resource, not medical advice.*
