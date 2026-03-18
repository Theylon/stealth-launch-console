# Marketing Skills Index

This workspace is a local marketing skill library. Other agents working in this repo should treat `./skills/` as the source of truth for reusable marketing skills.

## How To Use This Repo

- Skill folders live in `./skills/<skill-name>/`.
- Each skill is defined by `./skills/<skill-name>/SKILL.md`.
- Open the relevant `SKILL.md` before using or extending a skill.
- Many skills also include a short reference file in `./skills/<skill-name>/references/`.
- The high-level catalog lives in `./marketing-skill-library.md`.
- The canonical service model lives in `./service-blueprint.md`.
- The subagent orchestration and save rules live in `./execution-protocol.md`.
- The founder-facing service packaging lives in `./cmo-as-a-service.md`.
- Dogfood and live client workspaces live in `./clients/`.
- Test fixtures for B2B SaaS flows live in `./fixtures/`.

## Core Strategy Chain

Use this chain when the task is end-to-end positioning, messaging, and copy:

1. `$capture-market-context`
2. `$choose-ideal-customer`
3. `$position-product`
4. `$define-value-proposition`
5. `$build-messaging-architecture`
6. One or more copy skills
7. `$audit-messaging`

## Service Operation

- When working on the service itself, follow `./service-blueprint.md` first.
- When running client work, follow `./execution-protocol.md`.
- Treat `./clients/solo-founder-cmo-service/` as the first dogfood workspace and proof system.
- Save approved work into the client workspace instead of leaving it only in chat.

## Skill Catalog

### Strategy, Positioning, and Research

- `$capture-market-context`: Normalize raw company context into a reusable market brief.
- `$choose-ideal-customer`: Pick the sharpest ICP, segment wedge, and beachhead.
- `$position-product`: Define alternatives, differentiated value, and category framing.
- `$define-value-proposition`: Turn jobs, pains, and gains into a value proposition.
- `$create-positioning`: Build a full market positioning canvas with competitor and category analysis.
- `$create-product-insights`: Synthesize PMF, voice-of-customer, feature, and roadmap insights.
- `$create-icp-sizing`: Define ICP criteria, tiers, scoring, and TAM/SAM/SOM logic.
- `$create-category-positioning`: Design a category creation or category reframing strategy.
- `$generate-persona`: Create one detailed buyer persona in structured JSON form.
- `$create-buyers-journey`: Map the buyer journey, touchpoints, objections, and stage content.
- `$create-gtm-strategy`: Build a launch or market-entry GTM plan.
- `$create-pricing-strategy`: Design pricing models, tiering, discounts, and expansion paths.
- `$create-referral-program`: Design referral or affiliate incentives, mechanics, and rollout.

### Messaging and Brand

- `$build-messaging-architecture`: Convert strategy into a proof-backed message house.
- `$create-messaging`: Build a full modular website messaging system.
- `$create-brand-voice`: Define voice traits, tone rules, vocabulary, and channel adaptations.
- `$generate-tagline`: Generate and evaluate tagline and slogan options.
- `$create-value-proposition`: Build feature-to-outcome value ladders for segments and roles.
- `$create-feature-messaging`: Position one feature across launch and channel surfaces.
- `$create-ecosystem-messaging`: Create integration, partner, and ecosystem messaging.

### Copy and Content Production

- `$write-homepage-copy`: Draft homepage messaging and section copy.
- `$write-landing-page-copy`: Draft focused landing-page copy for one offer or use case.
- `$write-email-sequence`: Draft stage-aware nurture, launch, or follow-up sequences.
- `$create-landing-page`: Build a long-form, persuasion-heavy conversion landing page.
- `$create-product-description`: Write product descriptions across ecommerce and marketing formats.
- `$create-marketing-copy`: Generate multi-format copy for web, email, ads, social, and sales.
- `$create-faqs`: Generate FAQ systems with objection handling and SEO structure.
- `$create-press-release`: Write press releases plus distribution and support materials.

### Content Planning and Campaign Development

- `$create-content-angles`: Generate differentiated editorial angles and brief-ready perspectives.
- `$create-content-plan`: Build a content strategy with pillars, distribution, and a 20-day calendar.
- `$create-campaign-ideas`: Generate campaign concepts, compare them, and expand the winner.

### Review and Frontend Execution

- `$audit-messaging`: Review messaging for clarity, differentiation, proof, and stage fit.
- `$analyze-homepage`: Audit a homepage with CRO, LIFT, IA, trust, and CTA analysis.
- `$build-3d-landing-page`: Generate a single-file `index.html` landing page with Tailwind, Three.js, cinematic lighting, frosted materials, floating geometry, and scroll-reactive 3D motion.

## Notes For Agents

- Prefer the narrowest skill that matches the task instead of using the broadest possible one.
- Use the core strategy chain when upstream inputs are still fuzzy.
- Use the prompt-driven skills when the user asks for a specific deliverable directly.
- If the task is frontend implementation rather than marketing strategy or copy, prefer `$build-3d-landing-page` for immersive single-file experiences.
