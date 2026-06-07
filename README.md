# 北境微光旅行手帐

一个纯 HTML + CSS 的北境旅行主题静态网站。项目包含原始三页版本和一个适合直接发布/复制的单文件版本。

## 在线入口

GitHub Pages 发布入口：

https://wzgig.github.io/polartrail-travel-journal/

## 本地查看

推荐打开单文件版本：

```text
single.html
```

也可以查看原始三页版本：

```text
index.html
content.html
about.html
styles.css
```

## 文件说明

- `single.html`：完整单文件网页，包含全部 HTML 和 CSS，通过锚点在同一个文件中切换页面。
- `docs/index.html`：GitHub Pages 发布版本，由 `single.html` 同步而来。
- `index.html`、`content.html`、`about.html`：原始三页版本。
- `styles.css`：原始三页版本共用样式。
- `WORK_RULES.md`：项目维护规则。
- `PROJECT_PROGRESS.md`：项目进展记录。
- `DATA_SOURCES.md`：旅行素材与参考来源。

## 维护提醒

如果修改 `single.html`，并希望线上 GitHub Pages 同步更新，需要同时更新 `docs/index.html`。

```powershell
Copy-Item -LiteralPath single.html -Destination docs\index.html -Force
```

每次修改后请更新 `PROJECT_PROGRESS.md`，如果新增或改动资料来源，也要更新 `DATA_SOURCES.md`。
