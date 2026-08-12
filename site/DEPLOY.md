# Deploy Sources (FMHY-style) to Vercel

This `site/` folder is a rebranded VitePress instance based on [fmhy/edit](https://github.com/fmhy/edit). It is **not** the official fmhy.net site.

## One-time setup

1. Push this repo to GitHub (`Soluchann/Sources`).
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Use these settings (root of repo):
   - **Framework Preset:** Other
   - **Install Command:** `cd site && npx --yes pnpm@10.12.2 install --frozen-lockfile`
   - **Build Command:** `cd site && npx --yes pnpm@10.12.2 docs:build`
   - **Output Directory:** `site/docs/.vitepress/dist`
   - **Node.js Version:** 22.x
4. Add environment variables:
   - `FMHY_BUILD_API` = `false`
   - `FMHY_BUILD_NSFW` = `false`
5. In Vercel Project Settings → General / Build, clear any old Install Command override so `vercel.json` is used.
6. Click **Deploy**.

`vercel.json` at the repo root already encodes the install/build/output settings.

### Why this install command?

The site lockfile is **pnpm 10**. Vercel’s default pnpm is often older, so it ignores the lockfile and fails. Using `npx pnpm@10.12.2` runs the matching pnpm without Corepack or global installs.

## After deploy

- Production URL for this project: **https://sources-phi.vercel.app**
  - That domain stays the same on every push to `main`.
  - PR / branch commits get temporary **preview** URLs (unique each time) — use production for day-to-day browsing.
- `docs/.vitepress/shared.ts` → `meta.hostname` should match production (`https://sources-phi.vercel.app`).
- Every push to `main` redeploys production automatically.

## Local preview

```bash
cd site
pnpm install
FMHY_BUILD_API=false FMHY_BUILD_NSFW=false pnpm docs:dev
```
