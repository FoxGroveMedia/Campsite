# Campsite Monorepo

Welcome to Campsite, the static site generator that feels like a weekend in the woods. Pack light, pitch fast, and ship sites with a cozy developer experience.

## Trail Map
- packages/create-campsite — scaffolder invoked via `npm create campsite@latest`
- packages/basecamp — the build/dev/serve engine
- campsite01 — example site in this repo; scaffolder output defaults to `campsite-site`

## Why Camp With Us?
- Quick setup: new sites in a few prompts
- Flexible templating: Markdown, Nunjucks, Liquid, optional Vue/Alpine sprinkles
- Friendly defaults: warm colors, simple layouts, and Tailwind-ready styles
- Batteries included: dev server, file watcher, and static output to `dist/`

## Fast Start (New Site)
```
npm create campsite@latest my-campsite
cd my-campsite
npm install
npm run dev
```
- Choose your template engines when prompted (Markdown/Nunjucks/Liquid/Vue/Alpine)
- Swap `_gitignore` to `.gitignore` is handled automatically by the scaffolder

## Working in This Repo
```
npm install
cd campsite01
npm install
npm run dev
```
- Runs the sample site using the local basecamp build
- Scripts: `npm run build` (clean build), `npm run serve` (serve existing `dist/`)

## Basecamp Commands
- `campsite dev` — watch `src/` and `public/`, rebuild, and serve `dist/`
- `campsite build` — clean build to `dist/`
- `campsite serve` — serve an existing `dist/`

## Project Layout
- packages/create-campsite — CLI that copies the starter template and installs deps
- packages/basecamp — exposes `campsite dev|build|serve`
- campsite-site — sample consumer with `src/pages`, `src/layouts`, `public`

## Core Concepts
- Config: `campsite.config.js` controls `siteName`, `srcDir`, `outDir`, engines, integrations
- Pages: Markdown with frontmatter or `.njk` templates; other files copy through
- Layouts: Nunjucks defaults with a base layout and content block
- Dev loop: file watcher rebuilds on change; output served from `dist/`

## Contributing
Pull up a camp chair and open a PR. Keep it cozy, documented, and easy to extend. Tests and linting are coming soon.

## License
MIT
