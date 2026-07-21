# Portfolio Richa — Deploy Knowledge

## Project
- **Cloudflare Pages Project:** `portfolio-richa`
- **Project ID:** `79b3de74-8674-4fbc-94a2-3ff1f316c9ce`
- **Custom Domain:** `portofolio.richa.id`
- **Pages URL:** `portfolio-richa.pages.dev`
- **Local Path:** `/home/richa/.openclaw/workspace/portfolio-richa/`

## Directory Structure
```
portfolio-richa/
├── index.html          # V1 (root)
├── testimonials.md
├── v2/index.html
├── v3/index.html
├── v4/index.html
├── v5/index.html
├── v6/index.html
├── v7/index.html
└── DEPLOY.md           # this file
```

## Deploy Command
```bash
cd /home/richa/.openclaw/workspace/portfolio-richa
npx wrangler pages deploy <version> --project-name portfolio-richa --branch main
```

Example:
```bash
npx wrangler pages deploy v7 --project-name portfolio-richa --branch main
```

## Notes
- No `wrangler.jsonc` / `wrangler.toml` — direct upload, no build step
- Each version is a subfolder: `v1` (root), `v2`, `v3`, ...
- Cloudflare DNS proxies `portofolio.richa.id` → Pages project
- After deploy, new version available at `https://portofolio.richa.id/<vN>/` within minutes

## Adding New Version
1. Create `vN/index.html` locally
2. Run deploy command with `vN`
3. Done — no config changes needed
