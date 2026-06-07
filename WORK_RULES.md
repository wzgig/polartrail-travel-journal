# 项目维护规则

最后更新：2026-06-07

## 每次修改必须记录

每次修改本项目后，都需要在 `PROJECT_PROGRESS.md` 追加一条记录，至少包含：

- 修改日期
- 修改了哪些文件
- 完成了什么工作
- 做过哪些验证
- 是否已经提交并推送到 GitHub

## 来源资料必须可追溯

如果网页内容使用了新的旅游资料、官网信息、数据、图片来源或参考网址，必须同步更新 `DATA_SOURCES.md`，记录：

- 来源名称
- 来源网址
- 使用在页面中的哪一部分
- 访问日期
- 简短说明

## GitHub Pages 同步规则

`single.html` 是主要编辑文件。GitHub Pages 使用 `docs/index.html` 作为发布入口。

每次修改 `single.html` 后，推送前必须执行：

```powershell
Copy-Item -LiteralPath single.html -Destination docs\index.html -Force
```

## 推送前检查

推送到 GitHub 前至少检查：

- 所有内部 `#锚点` 都有对应 `id`
- `single.html` 不依赖外部 `styles.css`
- `docs/index.html` 与 `single.html` 内容一致
- 页面可以在浏览器中打开
- `PROJECT_PROGRESS.md` 已记录本次工作
- 如有新资料来源，`DATA_SOURCES.md` 已更新

## Git 提交流程

推荐流程：

```powershell
git status --short
git add .
git commit -m "feat: describe the change"
git push
```

提交信息尽量使用简短、清楚的英文 Conventional Commit 风格，例如：

```text
feat: add route detail navigation
docs: update project progress log
fix: adjust mobile layout
```
