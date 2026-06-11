# Quick Start

## 最小落地方式

### 1. 复制目录

把 `multi_ai_collab_template/` 复制到目标工程根目录。

### 2. 建立协作目录

```text
ai_handoff/
├── task_packs/
├── results/
└── reviews/
```

### 3. 角色切换

- 对主控 AI 说：`你是主控`
- 对协作者 AI 说：`你是协作者`

### 4. 固定流转

1. 主控 AI 发任务包
2. 协作者 AI 交结果文档
3. 主控 AI 写审查文档
4. 主控 AI 决定是否更新正式基线

## 最稳的组合

> 角色 skill + task pack + result + review
