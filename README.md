# Multi-AI Collaboration Template

一个可直接复制到其他工程中的多 AI 协作规范包。

目标很简单：

- 让一个主控 AI 负责分析、规划、拆任务、审查、更新正式结论
- 让一个或多个协作者 AI 负责执行、调试、验证、回传证据
- 让协作过程尽量靠文档落地，而不是靠聊天上下文记忆

这个仓库当前尽量收敛到两类核心材料：

- `README.md`：安装、目录、协作方式、模板示例
- `skills/`：角色行为规范

## 适用场景

适合下面这类项目：

- 需要多轮 AI 接力
- 需要把“执行结果”和“正式结论”分开
- 需要审查后才能更新基线
- 需要以后回看每轮任务、结果和审核记录

不适合下面这类情况：

- 只是一轮简单问答
- 不需要任务拆分
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

### 方式 1：直接复制到你的工程

把整个 `multi_ai_collab_template/` 目录复制到目标工程根目录，建议保留这个名字。

然后在工程根目录新建：

```text
ai_handoff/
  task_packs/
  results/
  reviews/
```

如果你的工程已经有正式文档目录，建议职责分开：

- `doc/` 或 `docs/`：正式基线、正式架构、正式结论
- `ai_handoff/task_packs/`：主控发出的任务包
- `ai_handoff/results/`：协作者返回的结果
- `ai_handoff/reviews/`：主控写的审核结论

### 方式 2：作为独立仓库引用

如果你想把它单独维护成公共模板仓库，可以直接：

1. `git clone` 这个模板仓库
2. 按项目需要复制到目标工程
3. 或者把 `skills/` 和 `README.md` 作为规范包引用

## 最小使用方法

### 给主控 AI 的一句话

`你是主控`

### 给协作者 AI 的一句话

`你是协作者`

### 推荐启动方式

先对主控 AI 说：

> 你是主控。先分析当前工程，再给出任务树，然后生成发给协作者的任务包，最后审查协作者结果。

再对协作者 AI 说：

> 你是协作者。只按任务包执行，返回证据化结果，不扩展范围，不修改正式结论。

## 协作模型

### 主控 AI 负责

- 理解全局问题
- 建立当前基线
- 拆解任务
- 发任务包
- 审查协作者结果
- 决定是否更新正式结论

### 协作者 AI 负责

- 在限定范围内执行
- 调试与验证
- 收集日志、报告、指标、diff
- 返回结果文档

### 基本规则

- 用户优先和主控 AI 对话
- 协作者不直接改写项目方向
- 未经审查的协作者结果不能进入正式基线
- 每一轮尽量只回答一个主问题
- 每一轮都要写清测试口径、工具版本、数据集或样本范围

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

- 正式结论放 `doc/` 或 `docs/`
- 临时协作文档放 `ai_handoff/`
- 不要把协作者原始输出直接当正式结论

## 最小任务流

1. 主控先输出 `Analysis / Plan / Risks / Next Action`
2. 主控生成任务包
3. 协作者按任务包执行
4. 协作者回传结果文档
5. 主控审查并给出 `通过 / 部分通过 / 不通过`
6. 只有审查通过的结论才允许写入正式文档

## 可直接复用的模板

下面这些模板是最小版，直接复制即可。

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

总控协作 skill。定义整体协作模型、角色边界、基线更新规则。

### `skills/ai-project-manager/`

主控 skill。用于：

- 分析项目
- 建立任务树
- 生成任务包
- 审查结果
- 决定是否更新正式结论

### `skills/ai-collaborator/`

协作者 skill。用于：

- 接收任务包
- 执行限定任务
- 输出证据化结果
- 在阻塞时回报，而不是擅自改方向

## 发布建议

如果要发布到 GitHub，建议仓库保持轻量：

- `README.md`
- `LICENSE`
- `.gitignore`
- `skills/`

这样别人一眼就能看懂，也更容易复制到自己的工程里。

## 一句话总结

这个模板的核心不是“多放文档”，而是把多 AI 协作压缩成一套可追溯、可审查、可迁移的最小工作流。
