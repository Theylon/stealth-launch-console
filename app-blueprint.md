# Stealth Launch Console Blueprint

## Product Thesis

This repo already contains the ingredients for a usable product:

- a canonical service model in [service-blueprint.md](/Users/eylon/Claude/marketing/service-blueprint.md)
- an agent execution contract in [execution-protocol.md](/Users/eylon/Claude/marketing/execution-protocol.md)
- a large skill library in [skills](/Users/eylon/Claude/marketing/skills)
- one dogfood client workspace with approved artifacts in [clients/solo-founder-cmo-service](/Users/eylon/Claude/marketing/clients/solo-founder-cmo-service)

The MVP should not invent a different methodology. It should compress the existing one into a static product surface an external company can use immediately.

## MVP Goal

Give a company one workflow that:

1. runs through five high-leverage skills
2. keeps the intermediate strategic outputs visible
3. ends with a markdown `coming out of stealth` PR document
4. deploys on GitHub Pages with no build system

## Chosen Skill Chain

The first MVP uses:

1. `$capture-market-context`
2. `$choose-ideal-customer`
3. `$position-product`
4. `$define-value-proposition`
5. `$create-press-release`

This is the tightest path from raw company input to a usable launch artifact.

## Why This Chain Works

- `$capture-market-context` gives the app a clean source of truth.
- `$choose-ideal-customer` prevents vague launch messaging.
- `$position-product` defines the alternative and differentiated frame.
- `$define-value-proposition` turns the position into one believable promise.
- `$create-press-release` packages everything into an external-facing document.

## UX Shape

The product now has two separate surfaces:

- a concise landing page at [index.html](/Users/eylon/Claude/marketing/index.html)
- the actual workflow at [app/index.html](/Users/eylon/Claude/marketing/app/index.html)

The app itself is a compact two-panel console:

- top stepper for workflow progress
- left panel for guided questions
- right panel for the live artifact preview

The preview should not feel like a generic summary panel. It should feel like the document the user is building.

## Output Shape

The exported markdown file includes:

- market context brief
- ICP decision
- positioning core
- recommended value proposition
- press release framework output

The press release package includes:

- news angle assessment
- headline options
- lead and body copy
- quote bank
- key messages
- SEO keywords
- multimedia assets
- distribution strategy
- supporting materials
- announcement variations

## Technical Boundary

The current MVP is intentionally static:

- one root [index.html](/Users/eylon/Claude/marketing/index.html)
- no backend
- no build step
- local browser persistence via `localStorage`
- markdown export via client-side download

This keeps the first version easy to host and easy to hand to an external company.

## GitHub Pages Model

Deployment should use GitHub Actions Pages publishing:

- push the repo to GitHub
- keep `index.html` at the repo root
- deploy the repository contents as the Pages artifact

The workflow lives in [deploy-pages.yml](/Users/eylon/Claude/marketing/.github/workflows/deploy-pages.yml).

## What A Real Product Version Adds Later

- actual skill execution instead of deterministic templating
- saved projects and multi-user collaboration
- approval gates that write approved artifacts into `clients/<client-slug>/`
- richer exports for press, content, and launch teams
- analytics on completion, drop-off, and refinement
