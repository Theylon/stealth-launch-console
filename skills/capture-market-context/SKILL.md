---
name: capture-market-context
description: Create a reusable B2B SaaS market context brief from founder notes, website copy, product docs, sales notes, pricing pages, win-loss notes, or prior strategy work. Use when Codex needs to normalize marketing inputs before ICP selection, positioning, value proposition work, messaging architecture, homepage copy, landing pages, email sequences, or messaging audits.
---

# Capture Market Context

## Overview

Turn scattered company information into one concise source of truth that downstream marketing skills can reuse. Optimize for B2B SaaS founders, PMMs, and early marketing hires working in English unless the user explicitly asks otherwise.

Read [references/context-model.md](references/context-model.md) when the input is messy, incomplete, or spread across several sources.

## Workflow

1. Gather the available inputs and label each one as fact, claim, or inference.
2. Normalize the core fields in this order: company, product, ICP hypotheses, buyer/job, alternatives, proof, pricing, GTM motion, goals, tone, constraints.
3. Resolve contradictions instead of averaging them away. Call out where founder language, customer language, and website language disagree.
4. Compress the result into a reusable market context brief that another skill can consume without re-reading the source material.
5. End with the minimum set of missing questions that would materially improve downstream work.

## Output Contract

Always produce these sections:

1. `Market Context Brief`
   - Company and product
   - Target customer and buyer
   - Core job or problem
   - Current alternatives
   - Value claims and proof
   - Pricing and GTM motion
   - Tone and brand constraints
2. `Known Unknowns`
   - Only include gaps that affect positioning or copy quality
3. `Rationale`
   - Explain the most important normalization choices
4. `Suggested Next Skill`
   - Usually `$choose-ideal-customer`; use a different next step only if the context is already sharp

## Quality Bar

- Prefer short, operational language over strategy jargon.
- Distinguish observed facts from your inference.
- Do not invent proof, customer pain, or pricing detail.
- Keep the brief compact enough that a downstream skill can reuse it directly.

## Skill Chain

This skill is the entry point for the library:

`$capture-market-context` -> `$choose-ideal-customer` -> `$position-product` -> `$build-messaging-architecture` -> copy skills -> `$audit-messaging`
