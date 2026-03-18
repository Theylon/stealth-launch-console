# Marketing Repo Overview

This repository is a local marketing skill library plus a static MVP product surface.

## Repo Structure

- [service-blueprint.md](/Users/eylon/Claude/marketing/service-blueprint.md): canonical operating model
- [execution-protocol.md](/Users/eylon/Claude/marketing/execution-protocol.md): orchestration and save rules
- [cmo-as-a-service.md](/Users/eylon/Claude/marketing/cmo-as-a-service.md): founder-facing packaging
- [skills](/Users/eylon/Claude/marketing/skills): reusable strategy, messaging, copy, and launch skills
- [clients/solo-founder-cmo-service](/Users/eylon/Claude/marketing/clients/solo-founder-cmo-service): dogfood proof workspace
- [index.html](/Users/eylon/Claude/marketing/index.html): GitHub Pages-ready MVP app

## Current MVP

The repository now has two user-facing surfaces:

- [index.html](/Users/eylon/Claude/marketing/index.html): concise landing page
- [app/index.html](/Users/eylon/Claude/marketing/app/index.html): the actual workflow app

The app runs through:

1. `$capture-market-context`
2. `$choose-ideal-customer`
3. `$position-product`
4. `$define-value-proposition`
5. `$create-press-release`

It produces a markdown `coming out of stealth` PR document with intermediate strategy outputs visible in the UI.

The app now supports runtime OpenAI stage execution:

- testers enter their own API key in the browser
- each stage can be run individually through the OpenAI Responses API
- `Run All Stages` generates all five deliverables in sequence

Because this is hosted on GitHub Pages, secrets are not stored server-side. The key is saved only in the local browser for testing.

## Hosting

The repository includes [deploy-pages.yml](/Users/eylon/Claude/marketing/.github/workflows/deploy-pages.yml) for GitHub Pages deployment through GitHub Actions.
