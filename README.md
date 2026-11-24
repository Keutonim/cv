# Keutonim's CV

Personal CV site of **Anton Pichugin** — AI Systems Engineer | Agentic AI | AI Security.
Built on top of [CV Hub](https://github.com/KeeGooRoomiE/cv_hub) (MIT), heavily customized:
single-section layout, dark/light theme toggle, EN-only.

## Data

- CV: `src/content/cv/en.yaml` (single source of truth; also served at `/cv/en.yaml` for machines)
- Projects: `src/content/showcase/projects_en.yaml`
- Site settings: `src/content/site/site.yml`
- Themes: `src/styles/themes/dark.css`, `light.css` (tokens override `src/styles/global.css`)

## Commands

```bash
npm install          # Node >= 24
npm run dev          # dev server
npm run build        # merge CV -> DOCX/TXT -> PDF (polished + ATS) -> Astro -> OG image
npm run preview      # serve dist/
```

PDF export needs Playwright chromium locally: `npx playwright install chromium`
(CI uses the runner's preinstalled Chrome).

## Deploy

GitHub Pages via `.github/workflows/deploy.yml` on every push to `main`.
`site`/`base` resolve from `GITHUB_REPOSITORY`; custom domain via `SITE_URL`/`BASE_PATH`
repo variables + `public/CNAME`.

## License

Code based on CV Hub © 2026 Alexander Gusarov — MIT, see [LICENSE](LICENSE).
CV content © Anton Pichugin.
