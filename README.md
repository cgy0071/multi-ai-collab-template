# Multi-AI Collaboration Template

A reusable collaboration kit for running one lead AI plus one or more collaborator AIs on real engineering projects.

This repository packages:

- role-based skills
- handoff document templates
- review templates
- baseline update templates
- recommended directory structure

It is designed for projects where "just chatting with multiple AIs" is not enough, and you need:

- scoped execution
- traceable handoff
- review before promotion
- formal baseline control

## What is included

### 1. Role skills

- `skills/ai-project-manager`
  - for the lead AI
  - triggers on phrases like:
    - `你是主控`
    - `你作为主控`
    - `you are the lead`
    - `you are the coordinator`

- `skills/ai-collaborator`
  - for collaborator / executor AIs
  - triggers on phrases like:
    - `你是协作者`
    - `你来执行`
    - `you are the collaborator`
    - `you are the executor`

### 2. Reusable templates

- `TASK_PACK_TEMPLATE_CN.md`
- `RESULT_TEMPLATE_CN.md`
- `REVIEW_TEMPLATE_CN.md`
- `BASELINE_UPDATE_TEMPLATE_CN.md`

### 3. Process and structure docs

- `QUICKSTART_CN.md`
- `DIRECTORY_STRUCTURE_TEMPLATE_CN.md`
- `COLLABORATION_RULES_CN.md`
- `PM_SYSTEM_PROMPT_TEMPLATE_CN.md`
- `SKILL_USAGE_CN.md`
- `INSTALL_CN.md`
- `GITHUB_REPO_BOOTSTRAP_CN.md`
- `GITHUB_RELEASE_COPY_CN.md`
- `FIRST_COMMIT_TEMPLATE_CN.md`
- `PUBLISH_STEPS_CN.md`

## Recommended workflow

1. User talks only to the lead AI
2. Lead AI creates a task pack
3. Collaborator AI executes and returns a result document
4. Lead AI reviews the result
5. Only reviewed conclusions are promoted into the formal baseline

## Recommended repository layout

```text
project_root/
├── doc/
├── ai_handoff/
│   ├── task_packs/
│   ├── results/
│   └── reviews/
├── src/
├── scripts/
└── multi_ai_collab_template/
```

## Installation

### Option A: copy into a project

Copy this whole directory into your target project and use the templates directly.

### Option B: install the skills into Codex

Copy:

- `skills/ai-project-manager`
- `skills/ai-collaborator`

into:

- `$CODEX_HOME/skills/`
  or
- `~/.codex/skills/`

Then trigger them with:

- `你是主控`
- `你是协作者`

## When this is useful

Use this for:

- large engineering projects
- multi-step optimization loops
- hardware / software co-design
- experiments that need strict attribution
- projects with formal baselines

Do not use this for:

- tiny one-off edits
- single-file tasks
- simple Q&A

## Publishing note

This template is intentionally lightweight and text-first. It does not assume any specific project type, language, or build system.

You can publish it as:

- a standalone template repository
- a subdirectory in an internal engineering playbook
- a shared skill bundle for your AI workflow

## License

MIT. See [LICENSE](LICENSE).

## Chinese docs

Start here:

- [README_CN.md](README_CN.md)
- [QUICKSTART_CN.md](QUICKSTART_CN.md)
- [SKILL_USAGE_CN.md](SKILL_USAGE_CN.md)
- [INSTALL_CN.md](INSTALL_CN.md)
- [GITHUB_REPO_BOOTSTRAP_CN.md](GITHUB_REPO_BOOTSTRAP_CN.md)
