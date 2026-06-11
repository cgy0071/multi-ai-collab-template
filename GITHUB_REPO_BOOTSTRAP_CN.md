# GitHub 仓库首发清单

## 目标

把当前 `multi_ai_collab_template/` 目录整理成：

- 可以直接 `git init`
- 可以直接首发到 GitHub
- 可以直接给别人看懂用途
- 可以直接被复制或安装使用

---

## 建议仓库名

优先候选：

1. `multi-ai-collab-template`
2. `ai-collaboration-template`
3. `lead-collaborator-ai-template`

如果你更想强调 skill：

4. `ai-collab-skills-template`

我最推荐：

> `multi-ai-collab-template`

原因：

- 够短
- 含义清楚
- 不绑定具体平台
- 后续扩展到不同 AI 工具也不违和

---

## 建议仓库描述

可直接用于 GitHub repository description：

> Reusable multi-AI collaboration template with lead/collaborator skills, handoff docs, review templates, and formal baseline workflow.

更短版本：

> Reusable template for lead/collaborator AI workflows, handoff docs, reviews, and baseline control.

---

## 建议 Topics

建议添加这些 GitHub topics：

- `ai`
- `llm`
- `agent`
- `multi-agent`
- `prompt-engineering`
- `ai-workflow`
- `engineering-process`
- `templates`
- `skills`
- `collaboration`

如果你想偏 Codex 生态，也可以加：

- `codex`

---

## 首发前必须确认

### 内容边界

- [ ] 不包含具体工程缓存
- [ ] 不包含具体工程日志
- [ ] 不包含私有路径说明以外的敏感信息
- [ ] 不包含某个特定项目的实验结果

### 仓库文件

- [ ] `README.md`
- [ ] `README_CN.md`
- [ ] `LICENSE`
- [ ] `CONTRIBUTING.md`
- [ ] `.gitignore`
- [ ] `skills/`
- [ ] 模板文档

### 技能

- [ ] `ai-project-manager` skill 可读
- [ ] `ai-collaborator` skill 可读
- [ ] skill 触发口令保留

---

## 建议目录保留清单

建议首发时保留：

```text
multi_ai_collab_template/
├── README.md
├── README_CN.md
├── LICENSE
├── CONTRIBUTING.md
├── .gitignore
├── INSTALL_CN.md
├── QUICKSTART_CN.md
├── SKILL_USAGE_CN.md
├── DIRECTORY_STRUCTURE_TEMPLATE_CN.md
├── COLLABORATION_RULES_CN.md
├── PM_SYSTEM_PROMPT_TEMPLATE_CN.md
├── TASK_PACK_TEMPLATE_CN.md
├── RESULT_TEMPLATE_CN.md
├── REVIEW_TEMPLATE_CN.md
├── BASELINE_UPDATE_TEMPLATE_CN.md
├── RELEASE_CHECKLIST_CN.md
├── GITHUB_REPO_BOOTSTRAP_CN.md
├── GITHUB_RELEASE_COPY_CN.md
├── FIRST_COMMIT_TEMPLATE_CN.md
├── examples/
└── skills/
```

---

## 建议不要在首发时加入的内容

- 与当前芯片工程强绑定的文件
- 某个项目下的 task/result/review 实例
- 具体实验数据
- 具体仿真日志
- 大量历史版本记录

原因：

> 首发版本应该先证明“这是一套通用模板”，而不是“这是某个项目的历史档案”。

---

## 最小首发流程

1. 复制 `multi_ai_collab_template/` 到独立目录
2. 在独立目录执行：
   - `git init`
3. 检查文件边界
4. 写首个 commit
5. 建 GitHub 仓库
6. push
7. 填仓库描述和 topics
8. 发首版 release

---

## 成功标准

首发成功应满足：

1. 陌生人打开仓库 1 分钟内能理解用途
2. 陌生人 5 分钟内知道怎么落地
3. 使用者能区分：
   - 主控 AI
   - 协作者 AI
4. 使用者知道：
   - skill 负责角色切换
   - 文档负责交接和收口
