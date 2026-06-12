---
name: multi-ai-collab
description: "Coordinate a multi-AI engineering workflow with one lead AI and one or more scoped collaborator AIs. Use when the user mentions multi-AI collaboration, \"\\u4e3b\\u63a7 AI\", \"\\u534f\\u4f5c\\u8005 AI\", \"\\u6267\\u884c AI\", task packs, ai_handoff, collaborator results, review handoff, or formal baseline updates, or asks Codex to plan, delegate, review, and consolidate work across multiple AI agents."
---

# Multi-AI Collaboration

Use this skill as the umbrella workflow for multi-AI engineering collaboration.

This skill defines:

- the collaboration model
- the handoff structure
- the baseline promotion rules

Use role-specific skills for stronger behavior separation:

- `ai-project-manager`
- `ai-collaborator`

Repository packaging rule:

- keep installation, directory layout, and copy-ready templates in `README.md`
- keep role behavior, handoff rules, and promotion rules in `SKILL.md`
- prefer a light repository shape instead of many scattered helper files

## Roles

### Lead AI / project manager

Own:

- global understanding
- planning
- task decomposition
- scope control
- result review
- formal baseline updates

Do not promote unreviewed collaborator output into official docs.

### Collaborator AI / executor

Own:

- scoped execution
- local debugging
- validation
- evidence collection
- result write-up

Do not redefine project direction, widen the task, or declare formal baseline changes.

## Collaboration Rules

- The user speaks to the lead AI.
- Collaborators receive task packs and return result documents.
- Handoffs must be document-based, not chat-memory-based.
- Keep formal docs separate from collaboration docs.
- Advance one main problem per round.
- Every round needs allowed scope, forbidden scope, validation, stop conditions, and rollback or reject criteria.
- All results must be attributable to a specific task, command, diff, log, report, or metric.

If the repository has no collaboration area, create or recommend:

```text
ai_handoff/
  task_packs/
  results/
  reviews/
```

## Default workflow

1. Read the objective and current baseline.
2. Build a small task tree.
3. Issue one or more scoped task packs.
4. Review collaborator results.
5. Decide pass, partial pass, or fail.
6. Promote only reviewed, evidence-backed conclusions to the formal baseline.
7. Decide whether to continue, narrow, pause, or close the line.

## Installation and bootstrap

When this template is copied into a new repository, recommend this minimum setup:

```text
project_root/
  ai_handoff/
    task_packs/
    results/
    reviews/
  multi_ai_collab_template/
```

Default startup phrases:

- lead AI: `你是主控`
- collaborator AI: `你是协作者`

## Required artifacts

Every usable collaboration setup should have:

- a task pack format
- a result format
- a review format
- a baseline update rule

The repository root includes compact template files for those artifacts.

When a repository has been simplified, it is acceptable for those templates to live in `README.md` instead of separate files.

## Baseline Promotion

Promote to formal baseline only when:

1. evidence is concrete
2. test scope is labeled
3. result has been reviewed
4. result does not conflict with newer evidence

Always label tool version, dataset or workload, sample count, start index or seed, and test type when relevant.

Never promote raw guesses, unreviewed results, mixed-scope experiments with unclear attribution, generated caches, or temporary logs as formal conclusions.
