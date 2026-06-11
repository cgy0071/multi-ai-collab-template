# Multi-AI Collaboration Template

## 用途

这是一套可直接复制到其他工程中的多 AI 协作规范包，用于建立：

- 主控 AI / 执行 AI 的角色边界
- 任务拆解与交接机制
- 结果审查与正式结论沉淀机制
- 目录结构与文档命名规范

这套模板特别适合以下类型项目：

- 代码量大、验证链长的工程
- 有 Python / HLS / HDL / RTL / 仿真 / 综合等多口径验证链的工程
- 需要多轮实验、回归、复盘的工程
- 用户希望把多个 AI 变成“团队”而不是“多个聊天窗口”的工程

---

## 核心原则

1. 用户只和主控 AI 对话
2. 执行 AI 只负责执行，不直接宣布正式结论
3. 所有交接以文档为准，不依赖聊天记忆
4. 正式文档和协作文档严格分层
5. 一轮只推进一个主问题
6. 每轮必须有停止条件和回退条件
7. 任何结果都必须可归因
8. 主控 AI 负责收口，不只是负责发任务

---

## 目录内容

- `QUICKSTART_CN.md`
  - 快速落地说明
- `DIRECTORY_STRUCTURE_TEMPLATE_CN.md`
  - 推荐目录结构模板
- `PM_SYSTEM_PROMPT_TEMPLATE_CN.md`
  - 主控 AI 提示词模板
- `TASK_PACK_TEMPLATE_CN.md`
  - 发给执行 AI 的任务包模板
- `RESULT_TEMPLATE_CN.md`
  - 执行 AI 返回结果模板
- `REVIEW_TEMPLATE_CN.md`
  - 主控 AI 审查模板
- `BASELINE_UPDATE_TEMPLATE_CN.md`
  - 正式基线更新模板
- `COLLABORATION_RULES_CN.md`
  - 协作规则总表

---

## 推荐使用方式

### 轻量方式

适合中小型项目：

- 直接复制本目录到新工程根目录
- 保留：
  - `PM_SYSTEM_PROMPT_TEMPLATE_CN.md`
  - `TASK_PACK_TEMPLATE_CN.md`
  - `RESULT_TEMPLATE_CN.md`
  - `REVIEW_TEMPLATE_CN.md`

### 标准方式

适合中大型工程：

1. 复制整个目录
2. 在新工程根目录建立：
   - `ai_handoff/task_packs/`
   - `ai_handoff/results/`
   - `ai_handoff/reviews/`
3. 让主控 AI 按模板发任务
4. 让执行 AI 按模板交付
5. 让主控 AI 审查后再写正式基线

### 重度方式

适合高风险工程：

- 增加独立“审计 AI”
- 增加统一验证入口脚本
- 增加阶段性 closure summary
- 增加基线冻结规则

---

## 最小落地流程

1. 复制本目录到目标工程
2. 复制 `DIRECTORY_STRUCTURE_TEMPLATE_CN.md` 里的目录结构
3. 用 `PM_SYSTEM_PROMPT_TEMPLATE_CN.md` 初始化主控 AI
4. 用 `TASK_PACK_TEMPLATE_CN.md` 发出第一轮任务
5. 用 `RESULT_TEMPLATE_CN.md` 接收执行结果
6. 用 `REVIEW_TEMPLATE_CN.md` 审查
7. 用 `BASELINE_UPDATE_TEMPLATE_CN.md` 更新正式结论

---

## 适用边界

这套模板不适合：

- 单文件小脚本
- 一次性问答
- 不需要回归和复盘的小改动

这套模板适合：

- 有阶段性基线
- 有验证链
- 有多轮演进
- 有“不能跑偏”的需求

---

## 一句话说明

> 这套模板的目标，不是让多个 AI 同时说话，而是让多个 AI 像一个可审计、可回溯、可收口的工程团队一样工作。
