# Skill Usage

## 角色 skill

### 1. 总 skill

- `skills/multi-ai-collab/`

作用：

- 定义总的多 AI 协作规则
- 定义 handoff 和 baseline 规则

### 2. 主控 skill

- `skills/ai-project-manager/`

触发口令：

- `你是主控`
- `你作为主控`
- `你是项目经理`

### 3. 协作者 skill

- `skills/ai-collaborator/`

触发口令：

- `你是协作者`
- `你来执行`
- `你按任务包做`

## 推荐用法

### 主控 AI

> 你是主控，请先分析当前基线，再拆任务，再审查协作者结果。

### 协作者 AI

> 你是协作者，请只按任务包执行，不要扩大范围，结果写成结果文档。

## 注意

skill 负责：

- 角色切换
- 输出习惯
- 协作机制

skill 不替代：

- 项目实际约束
- 任务包
- 审查和正式基线
