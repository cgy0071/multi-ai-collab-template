# GitHub 发布步骤

## 方式一：从当前目录复制后单独建仓

### 1. 复制目录

把：

- `multi_ai_collab_template/`

复制到一个新的独立目录，例如：

- `D:/repo/multi-ai-collab-template`

### 2. 初始化 Git

在新目录中执行：

```bash
git init
git add .
git commit -m "feat: initial public release of multi-AI collaboration template"
```

### 3. 创建 GitHub 仓库

建议仓库名：

- `multi-ai-collab-template`

### 4. 绑定远程并推送

```bash
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```

### 5. 补仓库设置

在 GitHub 页面补：

- repository description
- topics
- release

---

## 方式二：从当前大仓库中导出

如果你不想手工复制，也可以：

1. 单独把 `multi_ai_collab_template/` 导出到新目录
2. 只保留这个目录内的内容
3. 在导出目录建新仓库

核心原则：

> 不要把当前大工程的历史、缓存、实验记录一起带过去。

---

## 发布后建议立刻做的两件事

### 1. 建一个首版 Release

建议：

- tag: `v0.1.0`
- title: `Initial public template release`

### 2. 建一个后续路线 issue

建议 issue 标题：

- `Roadmap: next improvements for the collaboration template`

可以放的内容：

- skill 安装说明英文版
- 更多示例项目
- 自动生成 task pack 的脚本
- 自动同步 review/baseline 的脚本
