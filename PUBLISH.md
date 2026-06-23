# 发布到 GitHub

本仓库已经是可发布的 Git 仓库，并完成了首个提交。

## 已完成

- 复制当前 `ai-job-assistant` Skill
- 补齐 `.codex-plugin/plugin.json`
- 编写中文 README
- 添加 MIT LICENSE
- 通过 Codex 插件校验
- 通过 Skill 校验
- 完成本地 Git 初始提交

## 推送到 GitHub

先在 GitHub 创建一个空仓库，例如：

```text
ai-job-assistant-skill
```

创建时不要勾选 README、LICENSE 或 `.gitignore`，因为本地已经有这些文件。

然后在本目录执行：

```bash
git remote add origin git@github.com:<your-github-username>/ai-job-assistant-skill.git
git push -u origin main
```

如果你使用 HTTPS：

```bash
git remote add origin https://github.com/<your-github-username>/ai-job-assistant-skill.git
git push -u origin main
```

## 发布后建议补充

发布成功后，可以把 `.codex-plugin/plugin.json` 里的 `repository` 和 `homepage` 补成实际仓库地址。
