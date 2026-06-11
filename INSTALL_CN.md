# 安装说明

## 方式一：作为项目内模板使用

适合：

- 你想把整套规范跟着工程一起走
- 你希望 `doc/`、`ai_handoff/`、技能模板都一起存在

步骤：

1. 把 `multi_ai_collab_template/` 复制到目标工程根目录
2. 按 [DIRECTORY_STRUCTURE_TEMPLATE_CN.md](DIRECTORY_STRUCTURE_TEMPLATE_CN.md) 建立协作目录
3. 用 [PM_SYSTEM_PROMPT_TEMPLATE_CN.md](PM_SYSTEM_PROMPT_TEMPLATE_CN.md) 初始化主控 AI
4. 用 [TASK_PACK_TEMPLATE_CN.md](TASK_PACK_TEMPLATE_CN.md) 给协作者 AI 发任务

## 方式二：作为 Codex skill 安装

适合：

- 你希望在多个工程里复用同一套角色切换能力
- 你不想每次都复制整包

把下面两个目录复制到：

- `$CODEX_HOME/skills/`
  或
- `~/.codex/skills/`

需要复制的目录：

- `skills/ai-project-manager`
- `skills/ai-collaborator`

安装后可以这样触发：

- 主控：`你是主控`
- 协作者：`你是协作者`

## 方式三：作为 GitHub 模板仓库

适合：

- 你希望公开发布
- 你希望团队统一从同一个模板仓库初始化

建议保留：

- `README.md`
- `README_CN.md`
- `LICENSE`
- `CONTRIBUTING.md`
- `skills/`
- 各类模板文档

可以按需补充：

- `examples/`
- `releases/`
- `docs/`
