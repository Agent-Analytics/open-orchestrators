# Open Orchestrators

Open Orchestrators is a small Astro site for [`open-orchestrators.org`](https://open-orchestrators.org/). It curates a narrow editorial directory of open-source and orchestration-first AI agent products, frameworks, and company operating systems.

## What lives here

- `src/pages/index.astro`: the homepage and editorial directory composition.
- `src/data/orchestrators.ts`: the source of truth for directory entries, rank order, notes, tags, and links.
- `src/layouts/` and `src/components/`: layout and reusable UI pieces for future pages.
- `src/styles/global.css`: the local editorial design system.
- `public/`: favicons, social-sharing images, robots, and sitemap assets.
- `.firecrawl/`: local research artifacts used while evaluating products. This folder is ignored and does not need to be committed.

## Local preview

Install dependencies once, then run the Astro dev server:

```bash
cd open-orchestrators.org
npm install
npm run dev
```

Then open the local Astro URL it prints, usually `http://localhost:4321/`.

## Updating the directory

Most content changes should happen in `src/data/orchestrators.ts`.

- Add or edit entries in the exported `orchestrators` array.
- Keep summaries factual, short, and based on public sources.
- Prefer official website, docs, and GitHub links.
- If the number of entries changes, the homepage count and JSON-LD update from the shared data source automatically.
- If social preview imagery changes, keep the metadata in `src/layouts/BaseLayout.astro` aligned with the assets in `public/assets/`.

## Contributing

Contribution guidelines live in [`CONTRIBUTING.md`](./CONTRIBUTING.md).
