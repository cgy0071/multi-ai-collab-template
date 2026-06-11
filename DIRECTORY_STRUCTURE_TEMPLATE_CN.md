# Directory Structure Template

## 推荐目录结构

```text
project_root/
├── doc/                         # 正式文档，仅放审核通过后的结论
├── ai_handoff/                  # AI 协作区
│   ├── task_packs/              # 主控 AI 发出的任务包
│   ├── results/                 # 执行 AI 返回结果
│   ├── reviews/                 # 主控 AI 审查结果
│   └── README_CN.md             # 协作说明
├── scripts/                     # 可复用脚本
├── tmp/                         # 临时产物 / 缓存 / 中间生成物
├── src/                         # 业务源码
└── multi_ai_collab_template/    # 本模板目录
```

---

## 分层原则

### `doc/`

只放：

- 当前正式基线
- 当前架构说明
- 当前正式结论
- 对外可引用内容

不要放：

- 执行 AI 原始结果
- 中间失败实验
- 临时记录

### `ai_handoff/task_packs/`

只放：

- 主控 AI 发出的任务包

### `ai_handoff/results/`

只放：

- 执行 AI 的结果文档

### `ai_handoff/reviews/`

只放：

- 主控 AI 的审查文档

### `tmp/`

只放：

- 生成物
- 缓存
- 临时日志
- 自动导出文件

---

## 命名规范

### 任务包

- `Phase01_Task_Packs_CN.md`
- `Training_Phase22_Task_Packs_CN.md`

### 结果

- `Executor_P22_TaskA_Result_CN.md`
- `Reasonix_P22_TaskB_Result_CN.md`

### 审查

- `Executor_P22_Review_CN.md`

### 收口总结

- `Optimization_Closure_Summary_CN.md`

命名必须满足：

1. 能排序
2. 能看出 phase
3. 能看出是任务 / 结果 / 审查
