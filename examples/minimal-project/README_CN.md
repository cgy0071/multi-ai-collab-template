# Minimal Project Example

这是一个最小示例目录，展示这套模板在真实工程里的最小落地方式。

## 推荐结构

```text
minimal-project/
├── doc/
├── ai_handoff/
│   ├── task_packs/
│   ├── results/
│   └── reviews/
└── src/
```

## 用法

1. 主控 AI 使用 `ai-project-manager`
2. 协作者 AI 使用 `ai-collaborator`
3. 主控 AI 在 `task_packs/` 里发任务
4. 协作者 AI 在 `results/` 里回结果
5. 主控 AI 在 `reviews/` 里写审查
6. 审查通过后再更新 `doc/`

## 注意

这个目录是结构示意，不包含具体工程源码。
