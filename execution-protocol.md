# Solo Founder CMO Execution Protocol

This document defines how the service is actually run by agents.

## Core Rule

Every skill run is one isolated delivery unit handled by one dedicated subagent.

The parent orchestrator does not merge several skills into one silent step. It selects the next skill, spawns a subagent, waits for the result, presents it for review, and only advances after approval.

## Folder Contract

All service work lives under:

- `./clients/<client-slug>/`

Every client folder should contain:

- `client-index.md`
- `intake/`
- `phase-01-position-and-narrative/`
- `phase-02-diagnose-and-validate/`
- `phase-03-website-and-conversion/`
- `phase-04-launch-and-demand/`
- `phase-05-monetization-and-growth/`

## Parent Orchestrator Responsibilities

For each step:

1. read the client index and current phase status
2. choose the next skill from the lifecycle
3. spawn one dedicated subagent for that skill
4. pass only the context needed for that skill
5. wait for the skill result
6. present:
   - short summary
   - full doc
   - direct refinement request
   - recommended next skill
7. stop for user review
8. after approval, auto-save the artifact and update the client index

## Subagent Contract

Each skill subagent must:

1. read the skill instructions
2. remain in plan mode for its own task
3. ask all questions needed to resolve that skill properly
4. stay inside the scope of the assigned skill
5. return one final package containing:
   - `Summary`
   - `Full Deliverable`
   - `Refinement Request`
   - `Recommended Next Skill`

The subagent must not auto-run the next skill.

## Review Gate

After each skill run, the user must explicitly accept one of these outcomes:

- approve as-is
- refine and rerun this skill
- pause
- change the next skill

No skill should silently chain into the next one.

## Auto-Save Rule

Once the user approves a skill result, the parent orchestrator saves two files automatically:

- approved deliverable
- public-proof narrative

These become part of the client workspace immediately.

## File Naming

Use:

- `<run-order>-<skill-name>.md`
- `<run-order>-<skill-name>-proof.md`

Examples:

- `00-capture-market-context.md`
- `00-capture-market-context-proof.md`
- `01-choose-ideal-customer.md`

Run order is sequential within the client, not reset per phase.

## Artifact Metadata Contract

Every approved deliverable must record:

- `client`
- `phase`
- `skill`
- `objective`
- `required_inputs_used`
- `summary`
- `refinement_history`
- `recommended_next_skill`
- `status`

## Deliverable Structure

Use this minimum structure:

```md
---
client: ...
phase: ...
skill: ...
objective: ...
required_inputs_used:
  - ...
summary: ...
refinement_history:
  - ...
recommended_next_skill: ...
status: approved
---

# Approved Deliverable

...
```

## Proof Narrative Structure

Use this minimum structure:

```md
---
client: ...
phase: ...
skill: ...
status: approved
---

# Public Proof Narrative

## Before
...

## What Changed
...

## Why It Mattered
...

## Reusable Sales Takeaway
...
```

## B2B and B2C Branch Rule

The service stays one core offer.

Branch only:

- examples
- proof framing
- buyer language
- funnel shape
- recommended downstream skills

Do not split into separate B2B and B2C operating systems.

## Dogfood Client Rule

The first client is:

- `solo-founder-cmo-service`

This client is the test bed for:

- the file contract
- the review gate
- the proof narrative system
- the package ladder

## Completion Rule

A phase is only marked complete when:

- its required core skills are approved or explicitly skipped
- the client index is updated
- the next phase recommendation is recorded
