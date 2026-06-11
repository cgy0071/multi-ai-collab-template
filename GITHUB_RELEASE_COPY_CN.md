# GitHub 首发文案

## 仓库简介文案

### 版本 A

`multi-ai-collab-template` is a reusable template for running one lead AI plus one or more collaborator AIs on real engineering projects. It includes role-based skills, handoff templates, review templates, and a formal baseline workflow so multi-AI collaboration stays scoped, reviewable, and reproducible.

### 版本 B

This repository packages a practical multi-AI workflow:

- a lead AI that plans, decomposes, reviews, and controls the formal baseline
- collaborator AIs that execute scoped tasks and return evidence-backed results
- document templates and skills that make the workflow reusable across projects

---

## 首版 Release 标题建议

### 英文

- `v0.1.0 - Initial public template release`

### 中文

- `v0.1.0 - 首个可公开复用版本`

---

## 首版 Release Notes 建议

### 英文版

```md
## Overview

Initial public release of a reusable multi-AI collaboration template.

This repository is designed for projects where multiple AIs need to work as a real engineering team instead of a loose collection of chat sessions.

## Included in this release

- `ai-project-manager` skill for lead AI behavior
- `ai-collaborator` skill for scoped executor behavior
- task pack, result, review, and baseline update templates
- recommended repository structure for AI handoff workflows
- quickstart, install, and publishing guidance
- a minimal example layout

## What this template is for

- engineering projects with multi-step validation
- optimization loops that need attribution and rollback discipline
- workflows where only reviewed results should become formal baseline

## What this template is not

- a generic prompt dump
- a project-specific internal archive
- a replacement for project-specific technical constraints
```

### 中文版

```md
## 概述

这是首个可公开复用的多 AI 协作模板版本。

它面向的不是“多个 AI 聊天窗口”，而是“多个 AI 像工程团队一样分工协作”的场景。

## 本版包含

- `ai-project-manager` 主控 skill
- `ai-collaborator` 协作者 skill
- 任务包、结果、审查、基线更新模板
- 推荐的协作目录结构
- 快速落地、安装、发布说明
- 一个最小示例结构

## 适用场景

- 需要多轮验证的工程项目
- 需要严格归因和回退控制的优化流程
- 需要“审查后才能进入正式基线”的团队协作

## 不是什么

- 不是 prompt 杂货铺
- 不是某个具体项目的内部档案
- 不能替代具体项目自己的技术约束
```

---

## 首发公告短文案

适合发到 issue、群消息、内部公告：

### 中文

> 我把这段时间沉淀出来的多 AI 协作方法整理成了一个可复用模板仓库。它不是单纯的 prompt 集合，而是把“主控 AI / 协作者 AI / 任务交接 / 审查 / 正式基线维护”这些机制打包成了 skill + 文档模板，方便在其他工程里直接复用。

### 英文

> I packaged our multi-AI collaboration workflow into a reusable template repository. Instead of being just a prompt collection, it bundles lead/collaborator skills, handoff docs, review templates, and formal baseline rules so the setup can be reused across engineering projects.
