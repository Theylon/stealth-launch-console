---
name: generate-persona
description: Create one comprehensive buyer persona with psychological, behavioral, and journey context from company notes, product descriptions, audience hypotheses, sales notes, research summaries, or market context briefs. Use when Codex needs a detailed persona for messaging, segmentation, content planning, GTM, or journey design.
---

# Generate Persona

## Overview

Generate exactly one rich persona that is specific enough to drive messaging, channel planning, and sales alignment. Infer B2B or B2C from context, but default to B2B SaaS framing when the signals are mixed and the user is clearly working on software or services.

Read [references/framework.md](references/framework.md) for the full persona schema and JSON shape.

## Workflow

1. Normalize the company, product, audience, and differentiators.
2. Infer the dominant market type from the context.
3. Select one primary buyer persona instead of averaging several audiences together.
4. Fill the full persona structure with realistic, action-oriented detail.
5. Make metrics and quotes plausible for the role and market.

## Output Contract

- Output a single JSON object, not an array.
- Follow the exact top-level keys from the reference file.
- Start directly with the JSON payload.
- Do not prepend commentary or explanation.

## Quality Bar

- No generic placeholders.
- Use credible role context, responsibilities, motivations, and pains.
- Make content, event, and journey sections actionable for marketing work.
- Voice-of-customer quotes should sound like things a real buyer would say.
