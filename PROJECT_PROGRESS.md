# 项目进展记录

本文件用于记录每次修改或维护项目时做了什么，方便后续回看。

## 2026-06-07

### 初始网站搭建

- 创建原始三页静态网站：
  - `index.html`
  - `content.html`
  - `about.html`
  - `styles.css`
- 主题确定为“北境微光旅行手帐”。
- 完成固定顶部导航、首页主视觉、路线卡片、关于页面、团队信息和联系方式。
- 去掉“用 HTML 与 CSS 制作的静态网站”等作业说明式文案，让页面更像正式网站。
- 验证内容：
  - 三个页面都能通过顶部导航互相跳转。
  - 三个页面都引用同一个 `styles.css`。
  - 浏览器桌面和移动端渲染检查通过。

### 单文件版本

- 新增 `single.html`。
- 将首页、路线内容页、关于我们页合并到同一个文件。
- 将 CSS 内联到 `<style>` 中，便于复制到 W3School 等在线运行器。
- 使用纯 HTML + CSS 锚点切换：
  - `#home`
  - `#content`
  - `#about`
- 验证内容：
  - 默认显示首页。
  - 点击“路线内容”只显示路线页。
  - 点击“关于我们”只显示关于页。
  - `single.html` 不依赖 `styles.css`。

### 扩展跳转功能

- 在 `single.html` 中新增更多可跳转页面：
  - `#cold-routes`
  - `#photo-spots`
  - `#gear-library`
  - `#season-guide`
  - `#route-iceland`
  - `#route-lagoon`
  - `#route-lofoten`
  - `#route-lapland`
  - `#sources`
- 将首页统计数字改为可点击入口：
  - 18 条冷门路线
  - 42 个拍摄点位
  - 7 份装备清单
  - 4 季节出行建议
- 为路线内容页 4 张主路线卡片增加“查看路线细节”跳转。
- 增加素材参考页，并在页脚加入“素材参考”入口。
- 验证内容：
  - 12 个页面锚点都能正确切换。
  - 每次只显示目标页面。
  - 所有内部 `#链接` 都有对应 `id`。
  - 外部素材来源链接返回 200。

### GitHub 发布准备

- 新增项目维护文件：
  - `README.md`
  - `WORK_RULES.md`
  - `PROJECT_PROGRESS.md`
  - `DATA_SOURCES.md`
  - `.gitignore`
- 新增 GitHub Pages 发布目录：
  - `docs/index.html`
- `docs/index.html` 由 `single.html` 同步生成，用作 GitHub Pages 首页。
- 本次目标：
  - 初始化 git 仓库。
  - 创建公开 GitHub 仓库 `wzgig/polartrail-travel-journal`。
  - 推送项目文件夹。
  - 启用 GitHub Pages。

### 本次推送记录

- 状态：已完成第一次提交并推送。
- 首次提交：`6fb606b feat: add polar travel journal static site`
- 远程仓库：https://github.com/wzgig/polartrail-travel-journal
- GitHub Pages：https://wzgig.github.io/polartrail-travel-journal/
- Pages 发布源：`main` 分支 `/docs` 目录。
- 说明：`single.html` 已同步到 `docs/index.html`，线上页面使用 `docs/index.html`。
