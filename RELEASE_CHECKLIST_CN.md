# 发布检查清单

## 发布到 GitHub 前

### 仓库级文件

- [ ] `README.md` 存在
- [ ] `README_CN.md` 存在
- [ ] `LICENSE` 存在
- [ ] `CONTRIBUTING.md` 存在
- [ ] `.gitignore` 存在

### 技能文件

- [ ] `skills/ai-project-manager/SKILL.md` 存在
- [ ] `skills/ai-collaborator/SKILL.md` 存在
- [ ] skill 描述中保留角色触发词
- [ ] skill 内容不依赖某个特定工程

### 模板文件

- [ ] 任务包模板存在
- [ ] 结果模板存在
- [ ] 审查模板存在
- [ ] 基线更新模板存在

### 内容边界

- [ ] 没有带入某个具体项目的缓存、日志、生成物
- [ ] 没有带入敏感路径、私有信息、内部标识
- [ ] 没有把中间实验结果当成正式模板

### 可用性

- [ ] `QUICKSTART_CN.md` 可以指导 5 分钟落地
- [ ] `SKILL_USAGE_CN.md` 可以指导角色切换
- [ ] `README.md` 能让陌生人看懂用途

## 建议首版 release 文案

建议首版 release 强调：

1. 这是一个“多 AI 协作规范 + skill”模板仓库
2. 它解决的是：
   - 角色边界
   - 任务交接
   - 审查收口
   - 正式基线维护
3. 它不是：
   - 通用 prompt 杂货铺
   - 某个单一工程的私有脚手架
