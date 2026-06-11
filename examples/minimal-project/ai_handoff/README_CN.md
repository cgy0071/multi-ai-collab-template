# ai_handoff Example

这个目录展示协作文档应该如何分层。

## 子目录

- `task_packs/`
  - 主控 AI 发出的任务包
- `results/`
  - 协作者 AI 交回的结果
- `reviews/`
  - 主控 AI 的审查文档

## 规则

不要把：

- 正式结论
- 生成物
- 缓存

堆进这里。

这里是协作区，不是正式文档区。
