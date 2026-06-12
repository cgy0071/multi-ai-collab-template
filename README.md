# Multi-AI Collaboration Template

用于工程项目中的多 AI 分工协作规范包。

该模板的目标是建立一套轻量、可追溯、可审查、可迁移的协作机制：

- 由一个主控 AI 负责分析、规划、拆解任务、审查结果、维护正式基线
- 由一个或多个协作者 AI 负责执行、调试、验证、收集证据、返回结果
- 通过文档化 handoff 保持协作稳定，而不是依赖聊天上下文记忆

当前仓库尽量收敛为两类核心材料：

- `README.md`：安装方法、目录结构、使用方式、最小模板
- `skills/`：角色行为规范

## 适用场景

适用于以下类型的项目：

- 需要多轮 AI 接力执行
- 需要把“执行结果”和“正式结论”明确分离
- 需要审查通过后才能更新正式基线
- 需要长期保留任务、结果、审查记录

不适用于以下场景：

- 单轮简单问答
- 不需要任务拆解
- 不需要审查和可追溯记录

## 仓库内容

```text
multi_ai_collab_template/
├── README.md
├── LICENSE
├── .gitignore
└── skills/
    ├── multi-ai-collab/
    │   └── SKILL.md
    ├── ai-project-manager/
    │   └── SKILL.md
    └── ai-collaborator/
        └── SKILL.md
```

## 安装方式

### 方式 1：复制到目标工程

将整个 `multi_ai_collab_template/` 目录复制到目标工程根目录，建议保留该目录名。

随后在工程根目录创建：

```text
ai_handoff/
  task_packs/
  results/
  reviews/
```

如果目标工程已经存在正式文档目录，推荐职责分层如下：

- `doc/` 或 `docs/`：正式基线、正式架构、正式结论
- `ai_handoff/task_packs/`：主控发出的任务包
- `ai_handoff/results/`：协作者返回的结果
- `ai_handoff/reviews/`：主控写出的审查结论

### 方式 2：作为独立仓库引用

如果需要将该模板单独维护为公共模板仓库，可采用以下方式：

1. `git clone` 模板仓库
2. 按项目需要复制到目标工程
3. 或只引用其中的 `skills/` 与 `README.md`

## 最小使用方法

### 角色触发语

- 主控 AI：`你是主控`
- 协作者 AI：`你是协作者`

### 推荐启动方式

主控 AI 的典型启动指令：

> 你是主控。先分析当前工程，再给出任务树，然后生成发给协作者的任务包，最后审查协作者结果。

协作者 AI 的典型启动指令：

> 你是协作者。只按任务包执行，返回证据化结果，不扩展范围，不修改正式结论。

## 协作模型

### 主控 AI 负责

- 理解全局问题
- 建立当前基线
- 拆解任务
- 发出任务包
- 审查协作者结果
- 决定是否更新正式结论

### 协作者 AI 负责

- 在限定范围内执行
- 调试与验证
- 收集日志、报告、指标、diff
- 返回结果文档

### 基本规则

- 默认由用户与主控 AI 交互
- 协作者不直接改写项目方向
- 未经审查的协作者结果不得进入正式基线
- 每一轮尽量只回答一个主问题
- 每一轮都应写清测试口径、工具版本、数据集或样本范围

## 推荐目录边界

```text
project_root/
├── doc/ or docs/
├── ai_handoff/
│   ├── task_packs/
│   ├── results/
│   └── reviews/
└── multi_ai_collab_template/
```

推荐约束：

- 正式结论放在 `doc/` 或 `docs/`
- 临时协作文档放在 `ai_handoff/`
- 协作者原始输出不直接视为正式结论

## 最小任务流

1. 主控输出 `Analysis / Plan / Risks / Next Action`
2. 主控生成任务包
3. 协作者按任务包执行
4. 协作者回传结果文档
5. 主控审查并给出 `通过 / 部分通过 / 不通过`
6. 只有审查通过的结论才允许写入正式文档

## 可直接复用的模板

### 1. Task Pack Template

```md
# 任务包标题

## 背景
- 当前正式基线：
- 已知问题：
- 本轮不做：

## 目标
本轮只回答一个问题：

> [主问题]

## Allowed Scope
- [允许修改的文件或目录]
- [允许执行的验证]

## Forbidden Scope
- [禁止修改的文件或目录]
- [禁止扩展的方向]

## Expected Output
- [需要提交的结果文档]
- [需要提供的证据]

## Validation
- [命令 / 报告 / 对比脚本]

## Done Criteria
- [完成标准]

## Stop Conditions
- [何时停止并回报]

## One-line Instruction
> [发给协作者 AI 的一句话]
```

### 2. Result Template

```md
# 执行结果

## Task Name

## Input Files
- 

## Actual Execution
1.
2.

## Key Evidence
- diff
- log
- report
- metric

## Result
- 

## Uncertainties
- 

## Suggested Next Step
- 
```

### 3. Review Template

```md
# 审查结论

## Verdict
- 通过 / 部分通过 / 不通过

## One-line Summary

## Checklist
| 检查项 | 结论 |
|---|---|
| 是否回答了主问题 | |
| 是否在范围内 | |
| 证据是否充分 | |
| 是否可以更新正式基线 | |

## Accepted Points
- 

## Concerns
- 

## Next Action
- 
```

## Skills 说明

### `skills/multi-ai-collab/`

总控协作 skill，用于定义整体协作模型、角色边界、基线更新规则。

### `skills/ai-project-manager/`

主控 skill，用于：

- 分析项目
- 建立任务树
- 生成任务包
- 审查结果
- 决定是否更新正式结论

### `skills/ai-collaborator/`

协作者 skill，用于：

- 接收任务包
- 执行限定任务
- 输出证据化结果
- 在阻塞时回报，而不是擅自改方向

## 发布建议

发布到 GitHub 时，建议仓库保持轻量：

- `README.md`
- `LICENSE`
- `.gitignore`
- `skills/`

这种结构更便于快速浏览、复制和移植。

## 一句话总结

该模板的核心不是堆叠更多文档，而是将多 AI 协作收敛为一套可追溯、可审查、可迁移的最小工作流。
