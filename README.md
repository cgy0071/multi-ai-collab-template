# Multi-AI Collaboration Template

This repository keeps a medium-light collaboration template:

- small enough to publish and copy easily
- complete enough to preserve lead / collaborator role separation
- explicit enough to keep handoff, review, and baseline control intact

## Included

### Skills

- `skills/multi-ai-collab/`
  - umbrella workflow skill
- `skills/ai-project-manager/`
  - lead / main-controller role
- `skills/ai-collaborator/`
  - scoped executor role

### Minimal templates

- `QUICKSTART_CN.md`
- `SKILL_USAGE_CN.md`
- `DIRECTORY_STRUCTURE_TEMPLATE_CN.md`
- `TASK_PACK_TEMPLATE_CN.md`
- `RESULT_TEMPLATE_CN.md`
- `REVIEW_TEMPLATE_CN.md`

## Core model

- one lead AI owns planning, delegation, review, and formal baseline updates
- collaborator AIs receive scoped task packs and return evidence-backed results
- handoff artifacts live in `ai_handoff/task_packs/`, `ai_handoff/results/`, and `ai_handoff/reviews/`
- unreviewed collaborator output must not become an official project conclusion

## Fast start

### Role switching

- say `你是主控` to trigger the project-manager role
- say `你是协作者` to trigger the collaborator role

### Handoff layout

```text
ai_handoff/
  task_packs/
  results/
  reviews/
```

## Use this when

- a project needs auditable task delegation
- multiple AI rounds need review before promotion
- execution results and formal conclusions must stay separated

## Not the goal

This repository is not:

- a prompt dump
- a project-specific archive
- a replacement for project-specific technical constraints
