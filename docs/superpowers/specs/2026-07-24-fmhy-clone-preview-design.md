# FMHY-style Sources Site (Temporary Preview)

**Date:** 2026-07-24  
**Status:** Approved  
**Hosting:** Temporary Cloudflare tunnel only (permanent deploy later)

## Goal

Run a rebranded clone of the official FMHY VitePress site (`fmhy/edit`) that looks and navigates like [fmhy.net](https://fmhy.net), with three curated Sources pages added, exposed via a temporary public URL.

## Approach

Clone `https://github.com/fmhy/edit.git` into a local working directory (not committed into `Soluchann/Sources`). Rebrand instance metadata to **Sources**. Add curated pages. Serve with VitePress and tunnel with cloudflared.

## Rebranding

Update:

- `docs/.vitepress/constants.ts` — `meta.name`, hostname/description/tags so it is clearly not official fmhy.net
- `docs/index.md` — title, description, hero name/tagline → Sources

## New pages

| Route | Content |
|-------|---------|
| `/ui-tools` | Canvas UI, HeroUI, ASCII Effect (Componentry) |
| `/ai-tools` | Penecho, Atomic Agent |
| `/study-material` | PyTorch Internals, Alacritic thread, nested LLM Cache Management |

Wire into sidebar/nav. Keep stock FMHY pages unchanged.

## Out of scope

- Permanent GitHub Pages / Cloudflare / Vercel deploy
- Committing the full `fmhy/edit` tree into this repo
- Changing existing Sources README structure beyond what’s already merged/PRed
