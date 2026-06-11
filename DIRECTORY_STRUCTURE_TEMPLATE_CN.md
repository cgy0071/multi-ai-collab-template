# Directory Structure Template

## 推荐目录

```text
project_root/
├── doc/
├── ai_handoff/
│   ├── task_packs/
│   ├── results/
│   └── reviews/
├── src/
└── multi_ai_collab_template/
```

## 分层规则

### `doc/`

只放：

- 正式基线
- 正式架构说明
- 审核通过后的结论

### `ai_handoff/task_packs/`

只放主控 AI 发出的任务包。

### `ai_handoff/results/`

只放协作者 AI 的执行结果。

### `ai_handoff/reviews/`

只放主控 AI 的审查结论。
