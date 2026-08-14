# AGENTS.md

## Cursor Cloud specific instructions

### What this repository is

Personal **Sources** index: FMHY-style markdown wiki plus a VitePress site under `site/` (rebranded copy of `fmhy/edit`, not official fmhy.net).

- Root index: `README.md` and `fmhy.md` (keep them in sync)
- Site pages: `site/docs/` (curated pages include `ui-tools.md`, `ai-tools.md`, `study-material.md`, `shopping-gear.md`)
- Deploy: Vercel via root `vercel.json`

### Dual-update rule

When adding curated links, update **both**:

1. Root `README.md` + `fmhy.md`
2. The matching `site/docs/*.md` page

### Toolchain

- Node `22.x`
- `pnpm@10.12.2` (site lockfile requires pnpm 10)

### Install / run / build (from `site/`)

```bash
cd site
pnpm install --frozen-lockfile
FMHY_BUILD_API=false FMHY_BUILD_NSFW=false pnpm docs:dev   # http://localhost:5173/
FMHY_BUILD_API=false FMHY_BUILD_NSFW=false pnpm docs:build
```

Optional Nitro API (`pnpm api:dev`) is only needed when working on `site/api/`.

### Vercel

- Production (stable): https://sources-phi.vercel.app
- PR/branch pushes create temporary **preview** URLs — use production for day-to-day browsing
- Install/build must use `npx pnpm@10.12.2` (see root `vercel.json` / `site/DEPLOY.md`)
- Env: `FMHY_BUILD_API=false`, `FMHY_BUILD_NSFW=false`

### Notes

- Set `FMHY_BUILD_API=false` / `FMHY_BUILD_NSFW=false` for fast local runs
- `docs:dev` / `docs:build` may clone temporary git history into `site/.git-temp/` (git-ignored)
- OpenGraph image generation is the slow part of production builds
- Do not mass-reformat upstream-inherited Prettier warnings unless the task is formatting
