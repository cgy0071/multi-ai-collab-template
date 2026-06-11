# Contributing

## Goal

Keep this repository small, reusable, and role-clear.

This is not a random prompt dump. Every addition should make the collaboration model:

- more reliable
- easier to install
- easier to review
- easier to reuse across projects

## Contribution rules

### 1. Keep role boundaries sharp

Do not blur:

- lead AI responsibilities
- collaborator AI responsibilities
- formal baseline responsibilities

### 2. Prefer templates over prose

If a rule can be turned into:

- a task pack template
- a result template
- a review template

prefer that over adding long explanatory text.

### 3. Avoid project-specific assumptions

Do not hardcode:

- one programming language
- one build system
- one toolchain
- one company workflow

Keep the template generic unless a project-specific variant is intentionally added.

### 4. Do not mix official and intermediate artifacts

The repository should distinguish:

- reusable templates
- examples
- skills

from:

- project-specific logs
- generated outputs
- temporary test artifacts

### 5. Preserve low-friction triggers

The skill descriptions are intentionally written so that simple phrases like:

- `你是主控`
- `你是协作者`

can trigger the intended role. Do not accidentally remove those affordances.

## Recommended contribution flow

1. Propose the gap
2. Decide whether it belongs in:
   - skill
   - template
   - example
   - documentation
3. Keep the change scoped
4. Validate skill syntax if a skill changed
5. Update both English and Chinese entry docs when needed
