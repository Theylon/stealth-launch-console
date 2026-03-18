---
name: build-3d-landing-page
description: Build a single-file interactive website landing page with Three.js and Tailwind CSS, using a full-screen WebGL background, cinematic lighting, frosted-glass materials, floating geometry, and scroll-reactive parallax. Use when Codex needs to generate a premium frontend landing page or microsite as one complete `index.html` file with all CSS and JavaScript embedded.
---

# Build 3D Landing Page

## Overview

Create immersive landing pages as a single runnable `index.html` file. This skill is for frontend implementation, not copywriting: it should output working HTML with embedded CSS and JavaScript, using Three.js from a CDN and Tailwind CSS.

Read [references/implementation-guide.md](references/implementation-guide.md) before building.

Use external UI references when they help the page feel grounded in real product patterns:

- Use [Refero](https://refero.design/) for page-level research such as section sequencing, content density, interaction ideas, and visual pacing.
- Use [component.gallery](https://component.gallery/) for component-level research such as nav bars, pricing blocks, FAQ accordions, tabs, forms, cards, and other reusable UI patterns.
- If the user provides a Figma file, screenshot, or exact reference, treat that as the source of truth and use these sites only to fill obvious gaps.
- Abstract patterns from multiple examples. Do not closely imitate a single page.

## Workflow

1. Extract the website context, target mood, and requested aesthetic from the prompt.
2. Benchmark relevant page types in Refero before choosing layout direction, especially when the prompt is underspecified.
3. Check component.gallery for any high-risk or reusable UI modules that need to feel credible, such as navigation, FAQ, pricing, tabs, cards, or forms.
4. Choose one strong visual direction and execute it consistently across layout, typography, lighting, color, and motion.
5. Build the page as one file with:
   - Tailwind loaded from CDN
   - Three.js loaded from CDN
   - Embedded CSS and JavaScript
6. Create a fixed, full-screen WebGL scene behind the UI and make the foreground content scroll over it.
7. Use scroll progress to drive parallax, object offsets, camera response, or lighting response in a restrained but clearly visible way.
8. Return only the completed `index.html` content unless the user explicitly asks for explanation.

## Output Contract

- Output exactly one complete `index.html` file.
- Do not split into multiple files.
- Do not wrap the answer in extra explanation before or after the HTML.
- Ensure the file can run directly in a browser with no build step.

## Scene Requirements

Always include:

- A fixed full-screen WebGL canvas as the background
- Cinematic 3-point lighting:
  - key light
  - fill light
  - rim light
- `MeshPhysicalMaterial` on hero objects
- A premium frosted-glass or translucent material treatment
- Multiple geometric objects that float and rotate slowly
- Scroll-linked parallax reactions tied to page sections

## UI Requirements

- Make the foreground layout feel intentionally designed, not generic.
- Use strong typography and a clear aesthetic direction.
- Ensure legibility over the 3D scene with overlays, gradients, blur, or contrast management.
- Include enough section structure for the scroll interaction to matter.
- Keep the page responsive on desktop and mobile.

## Engineering Guardrails

- Cap device pixel ratio when needed for performance.
- Handle resize events correctly.
- Keep animation smooth and avoid overpopulating the scene.
- Use semantic HTML for the content layer.
- Respect reduced motion when practical by softening, not removing, the experience.

## What To Avoid

- Do not output placeholder comments like "add content here".
- Do not use flat, generic hero layouts with weak visual hierarchy.
- Do not make the 3D scene decorative but disconnected from scroll.
- Do not require npm, bundlers, or local assets unless the user explicitly asks for them.
- Do not browse inspiration sites after the layout is already fully specified unless you need a narrow component benchmark.
