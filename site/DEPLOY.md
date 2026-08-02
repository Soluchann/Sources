# Deploy Sources (FMHY-style) to Vercel

This `site/` folder is a rebranded VitePress instance based on [fmhy/edit](https://github.com/fmhy/edit). It is **not** the official fmhy.net site.

## One-time setup

1. Push this repo to GitHub (`Soluchann/Sources`).
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Use these settings (root of repo):
   - **Framework Preset:** Other
   - **Install Command:** `cd site && pnpm install --frozen-lockfile`
   - **Build Command:** `cd site && pnpm docs:build`
   - **Output Directory:** `site/docs/.vitepress/dist`
   - **Node.js Version:** 22.x
4. Add environment variables:
   - `FMHY_BUILD_API` = `false`
   - `FMHY_BUILD_NSFW` = `false`
5. Click **Deploy**.

`vercel.json` at the repo root already encodes the install/build/output settings.

## After deploy

- Update `docs/.vitepress/shared.ts` → `meta.hostname` to your real Vercel URL (e.g. `https://sources-xxx.vercel.app` or a custom domain).
- Every push to the connected branch redeploys automatically.

## Local preview

```bash
cd site
pnpm install
FMHY_BUILD_API=false FMHY_BUILD_NSFW=false pnpm docs:dev
```
