---
version: "4.3.1"
name: "AdminLTE 4.3.1"
description: "基于 Bootstrap 5.3.8 的响应式后台管理界面设计与交互规范"
colors:
  primary: "#0d6efd"
  secondary: "#6c757d"
  success: "#198754"
  info: "#0dcaf0"
  warning: "#ffc107"
  danger: "#dc3545"
  light: "#f8f9fa"
  dark: "#212529"
  body-light: "#ffffff"
  body-dark: "#212529"
  text-light: "#212529"
  text-dark: "#dee2e6"
  surface-secondary-light: "#e9ecef"
  surface-secondary-dark: "#343a40"
  border-light: "#dee2e6"
  border-dark: "#495057"
  white: "#ffffff"
  body: "var(--bs-body-bg)"
  body-text: "var(--bs-body-color)"
  surface-secondary: "var(--bs-secondary-bg)"
  surface-tertiary: "var(--bs-tertiary-bg)"
  border: "var(--bs-border-color)"
  muted-text: "var(--bs-secondary-color)"
  emphasis: "var(--bs-emphasis-color)"
  link: "var(--bs-link-color)"
  link-hover: "var(--bs-link-hover-color)"
  sidebar-text: "var(--lte-sidebar-color)"
  sidebar-hover: "var(--lte-sidebar-hover-bg)"
  sidebar-active: "var(--lte-sidebar-menu-active-bg)"
  valid: "var(--bs-form-valid-color)"
  invalid: "var(--bs-form-invalid-color)"
typography:
  body:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"'
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.5
  body-small:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"'
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.5
  caption:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"'
    fontSize: "0.75rem"
    fontWeight: 400
    lineHeight: 1.5
  title:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"'
    fontSize: "1.75rem"
    fontWeight: 500
    lineHeight: 1.2
  card-title:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"'
    fontSize: "1.1rem"
    fontWeight: 400
    lineHeight: 1.2
  label:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"'
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.5
  badge:
    fontFamily: "inherit"
    fontSize: "0.75em"
    fontWeight: 700
    lineHeight: 1
rounded:
  none: "0px"
  sm: "0.25rem"
  md: "0.375rem"
  lg: "0.5rem"
  full: "50rem"
spacing:
  none: "0px"
  xs: "0.25rem"
  sm: "0.5rem"
  md: "1rem"
  lg: "1.5rem"
  xl: "3rem"
dimensions:
  sidebar: "var(--lte-sidebar-width)"
  sidebar-mini: "4.6rem"
  sidebar-mini-compact: "3.1rem"
  header: "3.5rem"
  header-compact: "2.75rem"
  control-padding: "0.375rem 0.75rem"
  control-sm-padding: "0.25rem 0.5rem"
  control-lg-padding: "0.5rem 1rem"
  card-header-padding: "0.5rem 1rem"
  auth-body-padding: "20px"
  border: "var(--bs-border-width)"
motion:
  control: "0.15s ease-in-out"
  shell: "0.3s ease-in-out"
  chat-pane: "0.5s ease-in-out"
  reduced: "0.01ms"
elevation:
  card: "0 0 1px rgba(var(--bs-body-color-rgb), .125), 0 1px 3px rgba(var(--bs-body-color-rgb), .2)"
  small: "var(--bs-box-shadow-sm)"
  regular: "var(--bs-box-shadow)"
  large: "var(--bs-box-shadow-lg)"
components:
  app-shell:
    backgroundColor: "{colors.surface-tertiary}"
    textColor: "{colors.body-text}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.none}"
  app-header:
    backgroundColor: "{colors.body}"
    textColor: "{colors.body-text}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "0.5rem 0"
  app-sidebar:
    backgroundColor: "{colors.surface-secondary}"
    textColor: "{colors.sidebar-text}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.none}"
  content-card:
    backgroundColor: "{colors.body}"
    textColor: "{colors.body-text}"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.white}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    padding: "{dimensions.control-padding}"
  form-control:
    backgroundColor: "{colors.body}"
    textColor: "{colors.body-text}"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: "{dimensions.control-padding}"
  status-danger:
    backgroundColor: "{colors.danger}"
    textColor: "{colors.white}"
    typography: "{typography.badge}"
    rounded: "{rounded.md}"
    padding: "0.35em 0.65em"
  authentication-card:
    backgroundColor: "{colors.body}"
    textColor: "{colors.muted-text}"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: "{dimensions.auth-body-padding}"
---

# AdminLTE 4.3.1 设计开发规范

## Overview

本文是 AdminLTE `4.3.1` 当前源码快照的可执行设计约束，适用于开发者和 AI Agent。AdminLTE 是建立在 Bootstrap `5.3.8` 之上的响应式后台管理界面；视觉语言以 Bootstrap 语义色、Source Sans 3、紧凑信息密度、明确分区和可组合工具类为核心。

保留应用已经选择的 AdminLTE 布局和交互契约；优先复用 AdminLTE/Bootstrap 类与数据属性，再添加局部样式。本文规定视觉组合，不定义服务器框架、权限模型或后端 API。现有应用的路由、授权、验证和数据契约优先于演示值。

### 证据与范围

基线是上游标签 `v4.3.1`、提交 `d635f9396035586a092ee25e6045d03567fa48ca`。`package.json` 声明 Bootstrap `^5.3.8`，`package-lock.json` 实际锁定 `5.3.8`。本次完善同一版本的规范，不升级依赖。冲突时依次采用：消费项目的明确定制、版本匹配的实现及锁文件、可执行示例、上游说明文字。[S1] [S2]

全文用以下标记区分责任：

- **源码事实**：当前快照实际存在的 AdminLTE 类、插件、资源引用或可执行页面。
- **依赖继承**：Bootstrap 5.3.8 或另行加载的固定版本依赖所提供的行为。
- **建议补充**：生产页面应实现、但演示没有端到端完成的规则。
- **待验证**：不能仅通过源码阅读确认的浏览器、服务、无障碍或许可结果。

`src\html\pages` 是 Astro 演示与文档路由清单。`tables/data.html` 等构建路径是组件组合的证据，不是应用必须使用的 URL。普通侧导航、顶部导航、独立认证/异常页面使用不同壳层。源码没有内置路由标签缓存、权限路由、通用 CRUD 后端或统一混合导航控制器。[S8] [S9]

### 令牌作用域与定制

Front matter 描述默认角色，不是 CSS 生成器。`content-card.padding` 作用于 `.card-body`；`authentication-card.padding` 作用于 `.login-card-body`/`.register-card-body`；`status-danger` 描述默认危险状态徽章。不要把这些值重复施加到已有样式的外层卡片。侧栏颜色变量只在 `.app-sidebar` 内解析；顶栏 padding 是默认 navbar 尺寸，不是固定高度约束。

AdminLTE 导入了 Bootstrap SCSS，并启用阴影和负 margin。编译后的 `adminlte.css` 已包含 Bootstrap CSS，只加载一次；Bootstrap JavaScript 单独加载，之后再加载 AdminLTE JavaScript。定制 `$primary`、`$font-family-sans-serif`、`$lte-sidebar-width` 等 SCSS 变量时，在导入 AdminLTE 前声明。运行时表面优先使用有作用域的 Bootstrap/AdminLTE CSS 属性。仅修改 `--bs-primary` 不会更新所有已编译的 `.btn-primary` 状态；应使用按钮的 `--bs-btn-*` 属性或重编译调色板。[S2]

## Colors

颜色必须表达语义而不是装饰偏好。主要操作用 `{colors.primary}`，完成用 `{colors.success}`，提示用 `{colors.info}`，需注意用 `{colors.warning}`，错误或破坏性操作用 `{colors.danger}`，次要信息用 `{colors.secondary}`。优先使用 `.text-bg-primary`、`.text-bg-success`、`.text-bg-warning` 等 Bootstrap 组合类，让前景色随背景自动获得合理对比。

组件表面必须使用主题响应式 token：`{colors.body}`、`{colors.body-text}`、`{colors.surface-secondary}`、`{colors.surface-tertiary}`、`{colors.border}`。这些 token 分别代理 `--bs-body-bg`、`--bs-body-color`、`--bs-secondary-bg`、`--bs-tertiary-bg`、`--bs-border-color`，会在 `data-bs-theme` 解析为 light 或 dark 时随 Bootstrap 变量更新。带 `-light`/`-dark` 后缀的静态值只用于说明当前默认值或明确固定主题区域，不得作为通用组件表面。

页面底色使用 `.bg-body-tertiary` 或 Bootstrap 的 `--bs-body-bg`；内容表面使用 `.bg-body`、`.card`。边框依赖 `--bs-border-color`，不要把浅色模式的 `#dee2e6` 硬编码到深色表面。侧栏可以用 `data-bs-theme="dark"` 固定为深色区域，同时页面其余区域继续跟随全局主题。

### 主题模式

- `light`：在 `<html data-bs-theme="light">` 应用浅色变量。
- `dark`：在 `<html data-bs-theme="dark">` 应用深色变量。
- `auto`：跟随 `prefers-color-scheme`，系统偏好改变时同步更新。
- 用户选择存储在 `localStorage` 的 `lte-theme`；选择按钮使用 `data-bs-theme-value="light|dark|auto"`。
- 解析优先级为用户已存选择、服务端标记的 `data-bs-theme`、操作系统偏好。
- 必须在 `<head>` 中、首次绘制前运行与 ColorMode 同优先级的短内联脚本，读取 `lte-theme`、解析主题、设置 `<html data-bs-theme>` 与 `color-scheme`，避免首屏主题闪烁。若应用自管主题，则在 `<html>` 使用 `data-lte-color-mode="off"`，内联脚本也必须尊重该开关。

### 表面与状态继承

三级背景在浅色下为 `#f8f9fa`，深色下为 `#2b3035`。强调文字为黑/白；次级文字分别为 `rgba(33,37,41,.75)`/`rgba(222,226,230,.75)`。弱化状态区域配套使用 `--bs-{color}-bg-subtle`、`--bs-{color}-text-emphasis` 与 `--bs-{color}-border-subtle`。验证状态使用 `--bs-form-valid-*`、`--bs-form-invalid-*`，其深色值与普通 success/danger 色不同。这些是编译进入当前版本的 Bootstrap 默认值。[S2]

侧栏有独立导航调色板：浅色主文字 `#343a40`、子菜单 `#777`、hover/active 背景 `rgba(0,0,0,.1)`；深色主文字/子菜单 `#c2c7d0`、hover/active 文字白色、背景 `rgba(255,255,255,.1)`。选中导航并不自动成为主蓝色块。应使用 `--lte-sidebar-*` 变量，把固定深色主题限定在实际侧栏区域。[S3]

### 首屏初始化与主题更新

**源码事实**：ColorMode 通过 `data-lte-theme-resolved` 区分页面声明值与计算结果，遗漏标记会让跟随系统的结果被误当成固定偏好。上游 head 片段在已保存 `auto` 且页面显式声明 light/dark 时也存在优先级问题。**建议修正**：以下首屏片段识别三种有效选择并标记计算结果，它是修正后的集成配方，不是上游原样示例。按应用现有 CSP nonce/hash 机制允许执行。[S4]

```javascript
(() => {
  const root = document.documentElement;
  if (root.getAttribute("data-lte-color-mode") === "off") return;
  const valid = value => ["light", "dark", "auto"].includes(value);
  let stored = null;
  try { stored = localStorage.getItem("lte-theme"); } catch {}
  const authored = root.getAttribute("data-bs-theme");
  const preferred = valid(stored) ? stored : valid(authored) ? authored : "auto";
  const resolved = preferred === "auto"
    ? (matchMedia("(prefers-color-scheme: dark)").matches ? "dark" : "light")
    : preferred;
  root.setAttribute("data-bs-theme", resolved);
  root.style.colorScheme = resolved;
  if (resolved !== authored) root.setAttribute("data-lte-theme-resolved", "");
})();
```

经典构建中，`new adminlte.ColorMode().setTheme("dark")` 保存选择，并在 `document` 上触发携带 `{theme, resolved}` 的 `changed.lte.color-mode`。初始应用和系统自动切换不会触发该事件；需要在 auto 模式重绘的图表等非 CSS 控件还应观察 `data-bs-theme` 或系统偏好。`off` 禁用自动和 data API 处理；页面由其他主题管理器控制时不要再手动调用 `setTheme()`。[S4]

Bootstrap 浮层继承实际 DOM 容器的主题。移动到 `body` 的弹出层不会继承仅声明在内层面板上的 dark。根主题属性变化不意味着第三方 CSS 已完整适配暗色；下拉、日期、编辑器、图表、验证和禁用状态需要分别检查。[S14]

## Typography

默认字体取自 AdminLTE 的 Bootstrap 覆盖：`"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif`。正文以 `{typography.body}` 为基线；`.fs-7` 对应 `0.875rem`，`.fs-8` 对应 `0.75rem`。页面应保持一个可识别的主标题，卡片标题默认 `1.1rem`、常规字重。

- 标题元素按文档层级选择，不因视觉尺寸跳级；`.card-title` 只是样式类，不等同于固定标题级别。
- 元数据、时间和辅助说明使用 `.text-body-secondary` 与较小字号，不用降低透明度隐藏重要信息。
- 按钮和表单标签采用清晰短句；图标不能替代必要文本或可访问名称。
- 表格数字保持可扫描，状态文字不能只靠颜色表达。

### 字体、间距与控件尺寸

源码完整字体栈在 `sans-serif` 后还包含 `"Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"`。Source Sans 3 需要单独加载，仅声明名称不会提供字体文件或完整中文字形；消费项目应保留经过测试的系统 CJK 回退。正文默认 `1rem`、字重 `400`、行高 `1.5`；`.form-label` 与 `.btn` 不会自动变成 `600`，需要强调时才使用 `.fw-semibold`。[S2] [S5]

Bootstrap 间距级别 `0 / 1 / 2 / 3 / 4 / 5` 对应 `0 / .25 / .5 / 1 / 1.5 / 3rem`，栅格 gutter 为 `1.5rem`。`.fs-1` 到 `.fs-8` 的目标字号分别为 `2.5 / 2 / 1.75 / 1.5 / 1.25 / 1 / .875 / .75rem`。较大标题在阈值以下使用 Bootstrap RFS；演示页标题的 `.fs-3` 并非在所有宽度强制为 1.75rem。[S2]

| 元素 | 默认尺寸与作用域 |
| --- | --- |
| 按钮/输入 | padding `.375rem .75rem`、`1rem/1.5`、字重 `400`、1px 边框；根字号 16px 时名义高度 38px |
| 小号/大号按钮及输入 | `.25rem .5rem` 与 `.875rem` 字号，或 `.5rem 1rem` 与 `1.25rem` 字号；输入名义高度 31px/48px |
| Select | 相同基线，但末端 `2.25rem` padding 给箭头留位；不要直接套用按钮 padding |
| 卡片 | Body `1rem`；header/footer `.5rem 1rem`；标题 `1.1rem`、字重 `400` |
| 标签/帮助 | Label 下 margin `.5rem`；`.form-text` 上 margin `.25rem`、字号 `.875em` |
| 焦点/禁用 | 输入焦点环 `0 0 0 .25rem rgba(13,110,253,.25)`；按钮焦点环随变体；按钮禁用 opacity `.65` |

名义像素高度只是默认值推导，不是多行内容、自定义根字号和翻译标签的强制固定高度。[S2]

`typography.title` 描述演示页的 `h1.fs-3`：字重 `500`、行高 `1.2`、RFS 目标字号 `1.75rem`。`.card-title` 设置字重 `400` 和字号 `1.1rem`，但没有设置行高：令牌描述标题元素上的卡片标题（`1.2`），普通 div 则继承上下文行高。普通 Badge 使用 `.75em`、字重 `700`、行高 `1`；`.navbar-badge` 是独立覆盖，使用 `.6rem`、字重 `400`、padding `2px 4px`。[S2] [S3]

## Layout

### 应用壳

标准侧导航页面使用以下真实区域。`.app-wrapper` 直接位于 `<body>` 内，是 CSS Grid 容器；子元素由类名映射到网格区域，因此源码顺序不决定视觉位置。

```html
<body class="layout-fixed sidebar-expand-lg bg-body-tertiary">
  <div class="app-wrapper">
    <nav class="app-header navbar navbar-expand bg-body"><!-- 顶部栏内容 --></nav>
    <aside class="app-sidebar bg-body-secondary shadow" data-bs-theme="dark"><!-- 品牌与导航 --></aside>
    <main class="app-main">
      <div class="app-content-header"><!-- 标题与面包屑 --></div>
      <div class="app-content"><div class="container-fluid"><!-- 页面内容 --></div></div>
    </main>
    <footer class="app-footer"><!-- 可选页脚内容 --></footer>
  </div>
</body>
```

`.app-footer` 可选。`.app-content-header` 放页面标题与面包屑，`.app-content` 放业务内容；两者内部通常使用 `.container-fluid`，需要封顶宽度时使用 `.container`。不要混用 AdminLTE 3 的 `.main-*` 命名。

布局行为由 `<body>` 上的修饰类控制，并可按需组合：`layout-fixed` 让侧栏拥有独立滚动区域；`fixed-header` 使用 `position: sticky; top: 0`，同时让桌面侧栏 sticky；`fixed-footer` 使用 `position: sticky; bottom: 0`。名称并不意味着 `position: fixed`，移动侧栏才使用 fixed。Sticky 行为依赖滚动祖先，必须结合现有滚动容器验证长页面、键盘导航、200% 缩放与移动视口。[S3]

### 顶部栏

`.app-header.navbar.navbar-expand.bg-body` 内使用 `.container-fluid`。侧栏按钮置于 navbar 语境并使用 `data-lte-toggle="sidebar"`；右侧工具组使用 `.navbar-nav.ms-auto`。纯图标控制必须有 `aria-label`，通知数可用 `.navbar-badge.badge.text-bg-*`。

### 侧栏与树形菜单

`.app-sidebar` 必须包含 `.sidebar-brand` 和可滚动的 `.sidebar-wrapper`。菜单根节点使用 `.nav.sidebar-menu.flex-column` 与 `data-lte-toggle="treeview"`；子菜单使用 `.nav.nav-treeview`。当前链接加 `.active`；需要初始展开的父 `.nav-item` 加 `.menu-open`。父级箭头使用 `.nav-arrow`。

侧栏宽度由 AdminLTE SCSS 变量 `$lte-sidebar-width` 控制，当前源码默认值为 `250px`。组件 token 不固定该宽度；需要定制时，在导入 AdminLTE 前覆盖 SCSS 变量，运行时只读取 `.app-sidebar` 的计算宽度。

```html
<nav aria-label="主导航">
  <ul class="nav sidebar-menu flex-column" data-lte-toggle="treeview">
    <li class="nav-item menu-open">
      <a href="#" class="nav-link active">
        <i class="nav-icon bi bi-folder"></i>
        <p>报表 <i class="nav-arrow bi bi-chevron-right"></i></p>
      </a>
      <ul class="nav nav-treeview">
        <li class="nav-item"><a class="nav-link" href="/reports">销售报表</a></li>
      </ul>
    </li>
  </ul>
</nav>
```

侧栏是站点导航而不是应用菜单控件，默认保留 `<nav>`、列表和链接语义；不要只在根列表添加 `role="menu"`。只有同时实现 `menuitem` 角色及完整复合菜单键盘模型时，才采用 ARIA menu 模式。

### 内容标题与面包屑

标题区使用 `.app-content-header > .container-fluid`。保留单个页面主标题；面包屑放在 `<nav aria-label="breadcrumb">` 中，当前项用 `aria-current="page"`。窄屏允许标题与面包屑换行，不用绝对定位对齐。

### 密度与方向

`.compact-mode` 放在 wrapper 上可影响后代，但要让迷你宽度组合选择器生效，应把它与 `sidebar-mini`、`sidebar-collapse` 一起放在 `body`。RTL 页面必须同时使用 RTL 构建、`<html dir="rtl">` 和 `body.layout-rtl`；方向图标、图表与第三方控件仍需逐项验证。[S3]

### 布局变体与导航工具

| 源码变体 | 组合与行为 |
| --- | --- |
| 默认/固定/非固定侧栏 | Grid 列 `auto 1fr`、行 `min-content 1fr min-content`、最小 `100vh`；`layout-fixed` 改变滚动方式，不改变语义区域 |
| 迷你/折叠/禁止悬停 | 默认通过 `--lte-sidebar-width` 取 `250px`；mini `4.6rem`；compact mini `3.1rem`；`sidebar-without-hover` 禁止悬停展开 |
| 紧凑/顶栏/页脚 | 品牌/顶栏基线 `3.5rem`，compact 顶栏最大 `2.75rem`；页脚最小 `3rem`、padding `1rem` 或 compact `.5rem` |
| 顶部导航 | `layout/top-nav.astro` 省略侧栏与 `sidebar-expand-*`；使用 `.navbar-expand-lg` 和 Bootstrap Collapse 处理移动导航，不添加假侧栏填补网格 |
| 自定义内容区域 | `.app-content-top-area`、`.app-content-bottom-area` 位于 `.app-main` 内；底部区域使用 `margin-top:auto`，不是全局固定页脚 |
| Logo 切换与菜单密度 | `.logo-xs`/`.logo-xl` 配合 `.brand-link.logo-switch`；`.nav-indent` 控制子菜单缩进，`.nav-compact` 形成无圆角连续链接 |

内容标题 padding 为 `1rem .5rem`；`.app-main` 底部预留 `.75rem`。`--lte-sidebar-width` 支持运行时修改，但迷你宽度及关联尺寸单独编译；修改一个变量并不等于完成响应式换肤。[S2] [S3] [S8]

侧栏筛选输入使用 `data-lte-toggle="sidebar-search"`，可选 `data-lte-target="#menu-id"`，并提供 `[data-lte-search-empty]` 元素。不区分大小写匹配标签，展开匹配节点祖先，保留命中分组的整个子树，清空/Escape 恢复搜索前展开状态。输入上的 `filtered.lte.sidebar-search` 携带 `{query, matches}`：`matches` 包括父节点等可见条目，`-1` 表示重置。演示把搜索放在 `.sidebar-wrapper` 外；mini 收起状态隐藏输入，悬停展开后恢复。它是菜单筛选，不是后端或权限搜索。[S6]

顶栏全屏控件使用 `data-lte-toggle="fullscreen"`，子图标使用 `data-lte-icon="maximize|minimize"`。`maximized.lte.fullscreen`/`minimized.lte.fullscreen` 跟随真实 `fullscreenchange`，包括 Escape 退出；请求被拒绝时不发送虚假的最大化事件。消息/用户/通知下拉使用 Bootstrap Dropdown 和 `.dropdown-menu-end`；计数及动作在应用接入前仍是演示内容。[S5] [S6]

## Elevation & Depth

`.card` 默认使用双层轻阴影：`0 0 1px rgba(var(--bs-body-color-rgb), .125), 0 1px 3px rgba(var(--bs-body-color-rgb), .2)`。侧栏示例可加 `.shadow`，头像或图标只在确需分层时用 `.shadow-sm`。层级主要由表面、边框和间距表达，不要为每个块叠加强阴影。

- 普通内容：`.card` 默认阴影。
- 扁平信息：Bootstrap 边框与 `.bg-body`，不再加阴影。
- 浮层：使用 Bootstrap Dropdown、Toast、Modal 自身层级，不手写任意 `z-index`。
- 最大化卡片由 `.maximized-card` 控制；不要复制固定定位逻辑。

### 层级与动效

当前基线普通顶栏 `1034`、侧栏遮罩 `1037`、侧栏 `1038`、sticky 顶栏/页脚 `1030`。Bootstrap Offcanvas 遮罩/面板 `1040/1045`，Modal 遮罩/对话框 `1050/1055`，Popover `1070`、Tooltip `1080`、Toast `1090`。AdminLTE 最大化卡片 `1050`；可选 Select2 兼容层下拉 `1060`。数值只在兼容的 stacking context 中可比较，仍需考虑裁切、transform 和 portal 挂载位置。[S2] [S3] [S14]

控件通常 `.15s`，壳层/Treeview/CardWidget 为 `.3s`/`300ms`，Direct Chat 面板 transform 为 `.5s`。减弱动效 CSS 将动画缩短到 `.01ms`；插件定时回调仍可能等待配置时长，不能假设视觉动画缩短就改变事件时间。优先单一、有意义的过渡，并尊重用户动效设置。[S2] [S6] [S7]

## Shapes

基础圆角跟随 Bootstrap：小型元素 `{rounded.sm}`、普通卡片/按钮/输入 `{rounded.md}`、Modal 等较大表面 `{rounded.lg}`。圆形头像用 `.rounded-circle`，胶囊标签用 `.rounded-pill`。Callout 的识别形状是 `.25rem` 起始侧边框；Progress 的 AdminLTE 默认圆角为 `1px`。

同一层级保持一致圆角。不要把所有卡片改成夸张大圆角，也不要用装饰性不规则轮廓破坏后台信息密度。

## Components

### 卡片

标准结构为 `.card > .card-header + .card-body + .card-footer`；尾部可省略。标题用 `.card-title`，工具区用 `.card-tools`，图标按钮用 `.btn.btn-tool` 并提供 `aria-label`。主题卡片用 `.card-primary` 等 `.card-{color}`；`.card-outline` 将主题色变为 3px 顶边框。

卡片折叠、移除、最大化分别使用 `data-lte-toggle="card-collapse"`、`data-lte-toggle="card-remove"`、`data-lte-toggle="card-maximize"`。初始折叠使用 `.collapsed-card`；运行时状态 `.maximized-card`、`.was-collapsed`、`.expanding-card` 交由 CardWidget 管理。

### 按钮

使用 Bootstrap `.btn` 与 `.btn-primary`、`.btn-secondary`、`.btn-success`、`.btn-danger`、`.btn-outline-*`。主操作每个区域通常只保留一个 `.btn-primary`；危险操作使用 `.btn-danger` 且在不可逆时增加确认。卡片工具只用 `.btn-tool`。必须呈现默认、hover、focus、active 和 disabled 状态，不能移除可见焦点。

### 表单与验证

输入使用 `.form-control`、选择使用 `.form-select`、布尔项使用 `.form-check`；每个控件必须关联 `<label>`。验证失败时给控件 `.is-invalid`，就近放置 `.invalid-feedback`，并让错误节点进入 `aria-describedby`；错误提示要说明修正方式。动态错误使用 `role="alert"` 或 AdminLTE 的 announce 能力，提交失败后把焦点移至错误摘要或首个错误字段。

### 表格

基础使用 `.table`，按需要组合 `.table-striped`、`.table-hover`、`.align-middle`、`.table-sm`。表头单元格必须有正确的 `scope`。窄屏下用 `.table-responsive` 包裹，避免卡片溢出；但业务还需评估关键列折叠、换行或卡片化，不能把横向滚动视为唯一响应式方案。

### Small Box

`.small-box.text-bg-*` 用于高优先级指标；`.inner` 放数字与标签，`.small-box-icon` 是水印图标并设 `aria-hidden="true"`，`.small-box-footer` 是完整链接。不要只用大图标表达指标含义。

### Info Box

`.info-box` 是紧凑指标行；`.info-box-icon.text-bg-*`、`.info-box-content`、`.info-box-text`、`.info-box-number` 为核心结构，可加入 `.progress`、`.progress-description` 和 `.info-box-more`。长标签会截断，业务必须优先通过可见换行、调整布局或可访问名称保留完整信息；`title` 只能提供补充提示，不能单独替代可见文本，也不能作为键盘、触摸或辅助技术用户获取关键信息的唯一方式。

### Callout

`.callout.callout-info|success|warning|danger|primary|secondary` 用于嵌入正文的说明；`.callout-link` 用于内部重点链接。语义应同时由标题或图标/文本表达，不依赖边框颜色。

### Progress

沿用 Bootstrap `.progress > .progress-bar`，额外尺寸为 `.progress-sm`（10px）、`.progress-xs`（7px）、`.progress-xxs`（3px）、`.progress.vertical` 与 `.progress-group`。按 Bootstrap 5.3，在外层 `.progress` 设置 `role="progressbar"`、名称、`aria-valuenow/min/max`，内层 `.progress-bar` 只负责视觉宽度。不要在两层重复设置 progressbar 角色；不确定进度时省略 `aria-valuenow`。[S10]

### Badge

使用 `.badge.text-bg-*`，圆形状态可加 `.rounded-pill`。Badge 适用于短状态、数量与分类，不用作没有键盘行为的按钮；若可点击，应使用真实 `<a>` 或 `<button>` 并保留 badge 视觉类。

### Timeline

`.timeline` 内以 `.time-label` 分日期；每条由无类 wrapper 包含 `.timeline-icon` 与 `.timeline-item`，后者可含 `.time`、`.timeline-header`、`.timeline-body`、`.timeline-footer`。扁平变体用 `.timeline-inverse`。时间、操作者与动作必须有可读文本。

### Direct Chat

容器为 `.card.direct-chat`，消息和联系人分别用 `.direct-chat-messages`、`.direct-chat-contacts`。切换按钮位于容器内并用 `data-lte-toggle="chat-pane"`；打开状态 `.direct-chat-contacts-open` 由插件管理。可监听 `expanded.lte.direct-chat` 与 `collapsed.lte.direct-chat` 同步业务状态，但不要手动复制插件切换逻辑。

### Toast

使用 Bootstrap `.toast`；AdminLTE 增加 `.toast-{color}` 以同步标题、浅色正文与边框。可访问播报按紧急程度分级：阻断操作、需要立即处理的错误使用 `role="alert"`、`aria-live="assertive"`、`aria-atomic="true"`；普通成功提示和低优先级状态更新使用 `role="status"`、`aria-live="polite"`、`aria-atomic="true"`，避免打断屏幕阅读器当前朗读。关闭按钮使用 `data-bs-dismiss="toast"` 与 `aria-label`。关键失败不能只短暂显示 Toast，还应在页面保留可恢复信息。

显示 Toast 需要调用 `bootstrap.Toast.getOrCreateInstance(toastElement).show()`。`UI/general.astro` 的 `data-bs-toggle="toast"` 由页面自身点击监听处理，不是 Bootstrap 自动 toggle API。Tooltip、Popover 也需显式初始化，例如 `bootstrap.Tooltip.getOrCreateInstance(element)`，宿主移除时需销毁实例。[S10]

### Alert

使用 `.alert.alert-{color}`；可关闭时加 `.alert-dismissible`，关闭按钮使用 `.btn-close`、`data-bs-dismiss="alert"` 和 `aria-label="Close"`。动态插入的 Alert 可由 AdminLTE live region 自动播报。错误、警告和成功消息要有明确文本。

### Modal

触发器使用 `data-bs-toggle="modal"` 与 `data-bs-target="#id"`；结构使用 `.modal > .modal-dialog > .modal-content`，再分 `.modal-header`、`.modal-body`、`.modal-footer`。长内容使用 `.modal-dialog-scrollable`，窄屏可使用 `.modal-fullscreen-lg-down`。Bootstrap 负责对话框内焦点约束与 Escape；AdminLTE 会在关闭后恢复触发焦点，业务需保证标题、说明和关闭路径可访问。

### 认证与锁屏表面

登录/注册分别使用 `body.login-page.bg-body-secondary` 或 `body.register-page.bg-body-secondary`，以及 `main.login-box` 或 `main.register-box`；内容为 `.card > .login-card-body` 或 `.register-card-body`，说明为 `.login-box-msg` 或 `.register-box-msg`。可以采用 `.card.card-outline.card-primary` 作为 v2 表面。锁屏使用 `body.lockscreen.bg-body-secondary` 与 `main.lockscreen-wrapper`，核心结构含 `.lockscreen-name`、`.lockscreen-item`、`.lockscreen-image`、`.lockscreen-credentials`。输入必须有显式或 `.visually-hidden` 标签；身份、错误、会话恢复和切换用户逻辑属于业务实现。

登录/注册框默认 `400px`；在 `max-width:576px` 下变为 `90%`。Body padding 为 `20px`，不是普通卡片的 `1rem`。v2 页面使用浮动标签；`examples/forgot-password.astro` 提供找回密码页面组合，不代表已有真实邮件发送流程。[S9]

认证内容文字使用 `--bs-secondary-color`，不是普通卡片文字令牌。其 input-group 焦点规则移除 box-shadow，但保留边框反馈；应在该上下文评估可见焦点，不能假设普通输入的焦点环仍存在。覆盖位于 `src/scss/pages/_login_and_register.scss`。[S2]

### 选择控件、标签页、分页与抽屉

**依赖继承**，见 `forms/elements.astro`、`UI/general.astro`：Checkbox/Radio 使用 `.form-check-input`，布尔开关 `.form-switch`，原生范围输入 `.form-range`，附加内容 `.input-group`，浮动标签 `.form-floating` 且 label 位于 input 之后。在真实控件上体现 checked、indeterminate、readonly、disabled、invalid 和 focus，不只改变外层样式。Readonly 与 disabled 是不同状态。[S10]

标签页使用 `.nav-tabs`/`.nav-pills`、`data-bs-toggle="tab|pill"` 和对应 `.tab-pane`，配套 tablist/tab/tabpanel 关系；它们是局部内容切换，不提供路由缓存或访问历史标签栏。分页使用 `.pagination > .page-item > .page-link`、`aria-current="page"` 和真正不可用的上一页/下一页控件。Bootstrap 提供外观，不提供数据集分页。[S10]

FAQ 使用 `.accordion` 与 Bootstrap Collapse。抽屉使用 `.offcanvas-start|end|top|bottom`、`data-bs-toggle="offcanvas"`、关联标题、关闭按钮与 Bootstrap 生命周期。侧栏 PushMenu 是独立组件，不继承 Offcanvas 的焦点约束或 Escape 行为。[S6] [S10]

### 固定版本的高级表单与数据表

`forms/advanced.astro` 加载 **Tom Select 2.6.1** 及其 Bootstrap 5 样式、**Flatpickr 4.6.13**。单选用 `clear_button`；标签用 `remove_button`，仅允许自由录入时设置 `create:true`。远程审核人示例使用 `valueField:"id"`、`labelField:"name"`、`loadThrottle:300`、`virtual_scroll` 和 AbortController 取消过时请求。`{results,next}` 只是演示 loader 格式，不是消费项目必须使用的 API。接入真实数据时保留稳定 ID、选中值、键盘、标签、加载、无结果和重试状态。[S11]

Flatpickr 示例格式为 `Y-m-d`、`Y-m-d H:i`、`mode:"range"`，以及配合 `time_24hr:true` 的纯时间 `H:i`；页面没有定义业务时区或日期序列化合同。`forms/editors.astro` 加载 **Quill 2.0.3** 的 Snow/Bubble 主题；保留已配置工具栏，为编辑区提供可访问名称。保存富文本应遵守应用现有的验证/清洗策略。[S11]

`tables/data.astro` 加载 **Tabulator 6.4.0** 与 `tabulator_bootstrap5.min.css`。本地数据示例使用 `layout:"fitColumns"`、分页大小 `10`、选项 `[10,25,50,100]`、可拖动列、input/list 表头筛选、name/email 的 OR 搜索、状态徽章、CSV/JSON 导出和打印。这些行为在页面实现，不是 DataTables/jQuery 或服务端分页。重置时明确处理全局筛选及表头筛选；保留应用既有分页/排序/导出合同，不能把演示数据当成 API。任意用户字符串不得未经转义插入 formatter HTML。[S12]

### Ribbon 与社交组件

`4.3.1` Ribbon 填满裁切卡片角：定位父元素内使用 `.ribbon-wrapper` 与内层 `.ribbon`；正方形尺寸 `70 / 110 / 145px`，带宽 `91 / 143 / 188.5px`，字号 `.8 / 1 / 1.25rem`。`.ribbon-lg`/`.ribbon-xl` 放在 wrapper。为短文字和工具保留空间，不得遮住标题或操作目标。[S13]

社交组合包括 `.user-block`（头像 `2.5rem`、small `1.75rem`）、`.post`、`.description-block`、`.widget-user`、`.widget-user-2`。第一种个人头部高 `8.4375rem`、悬出头像 `5.625rem`；第二种使用 `4.0625rem` 内联头像。Small Box 数字默认 `2.2rem` 并按列宽局部缩小；Info Box 最小高度 `80px`、图标区域 `70px`。这些是组件特定尺寸，不是放大所有卡片的依据。[S13]

## Page Patterns

以下**源码事实**描述真实页面组合。标记为 demo 的部分需要接入应用逻辑，控件才代表操作成功。路径相对于 `src\html\pages`。[S9]

| 页面族 | 结构、行为与集成边界 |
| --- | --- |
| `index.astro`、`index2.astro`、`index3.astro` | 指标网格、图表卡片、表格/活动；ApexCharts 3.37.1，第一仪表盘还用 jsVectorMap 1.5.3、SortableJS 1.15.0；序列、地图及日期为演示值 |
| `users.astro`、`tables/simple.astro` | 卡头可换行搜索/角色/操作、`.card-body.p-0`、响应式表格、徽章、行操作、分页和新增用户 Modal；目录筛选/保存是视觉控件，与可运行的 Tabulator 示例不同 |
| `forms/layout.astro`、`forms/validation.astro` | 纵向/横向/网格/浮动标签、input group、HTML validity 与 Bootstrap feedback；保留字段名、服务器错误与提交合同 |
| `forms/wizard.astro` | 上一步/下一步/提交、步骤显隐、active/completed、分步校验及确认摘要；最终提交只弹 alert。建议补充：文本安全摘要渲染、焦点转移、整表校验和防重复提交 |
| `pages/profile.astro`、`pages/settings.astro` | 头像/资料/活动与编辑表单；设置使用 `col-md-3` list-group pills 与 `col-md-9` 内容，包含账户、通知、安全、计费和危险区域；双因素、计费、删除是 UI 示例 |
| `pages/projects.astro` | 汇总指标、项目筛选/表格、头像、进度、状态徽章与行命令；详情路由及编辑沿用现有业务合同 |
| `pages/gallery.astro` | 响应式图片区、带 `aria-pressed` 的分类控件、可见计数、空态与图片 Modal；筛选在本地实现 |
| `pages/file-manager.astro` | 文件夹导航、存储汇总、文件网格/列表模式；模式切换在本地实现，上传/删除/下载需要真实服务 |
| `pages/search-results.astro` | 搜索框、内容标签、带标题的结果摘要、分页；数据与搜索结果为演示内容 |
| `pages/chat.astro` | 独立 `.chat-app`，联系人 `320px`、会话 `1fr`，高 `calc(100vh - 14rem)`、最小 `32rem`；本地发送安全追加文字。`max-width:768px` 隐藏联系人但没有替代选择器，真实聊天建议补齐入口 |
| `pages/calendar.astro`、`pages/kanban.astro` | 分别用 FullCalendar 6.1.20、SortableJS 1.15.7；日历事件和跨列卡片移动为本地行为；Kanban 使用 `repeat(auto-fit,minmax(280px,1fr))`、`1rem` gap。业务应补键盘移动、持久化及回滚 |
| `mailbox/inbox.astro`、`mailbox/read.astro`、`mailbox/compose.astro` | 文件夹列表+邮件表格、阅读详情、收件人/主题/编辑区/附件组合；没有邮箱服务、上传管道或真实发送流程 |
| `pages/invoice.astro`、`pages/pricing.astro` | 可打印发票及合计、套餐比较/价格卡片；保留数字/货币合同，修正而非照搬发票示例的重复 h1 |
| `pages/faq.astro`、`pages/404.astro`、`pages/500.astro`、`pages/maintenance.astro` | FAQ 折叠面板；含恢复链接的独立异常/维护页面，不强制套用侧导航壳 |
| `examples/*.astro` | 登录/注册及 v2、找回密码、锁屏；认证/会话规则由应用负责 |
| `layout/*.astro`、`generate/theme.astro`、`UI/*.astro`、`widgets/*.astro` | 布局变体、主题生成演示、组件展示；生成的颜色/类是定制示例，不是额外的 light/dark 偏好值 |

独立聊天页样式不等于 `.direct-chat` 组件样式：页面使用 `.chat-message.me` 与 `.chat-bubble`（1rem 圆角、70% 最大宽度），组件使用 `.direct-chat-text`。页面局部样式未包含在 `adminlte.css` 中，只移植选中页面的作用域规则。价格页和独立聊天可有页面级形状例外，普通工作卡片保持基础圆角。[S9]

## State and Content Rules

以下是由演示实际缺口引出的**应用建议规则**，不声称 AdminLTE 会自动实现。

| 触发/状态 | 可见结果与恢复路径 |
| --- | --- |
| 初次加载/刷新 | 稳定区域尺寸、有名称的 spinner/placeholder、`aria-busy`；适当保留可用筛选与已加载数据 |
| 没有记录/没有匹配 | 使用不同空态文案，提供适当的新建或清空筛选入口，不虚构记录 |
| 验证失败 | 保留输入、错误关联字段、体现 `aria-invalid`、聚焦摘要或首个错误；Wizard 最终提交重新验证隐藏步骤 |
| 请求失败 | 停止加载、保留输入、可操作错误及重试，按真实响应合同区分未登录/无权限/冲突 |
| 正在提交/成功 | 防重复调用、禁用执行中的命令、完成后恢复，仅在真实操作确认后播报成功 |
| 选中/批量操作 | 说明选择范围（当前页或全部匹配）、半选状态与数量，处理部分成功并保留失败项供重试 |
| 破坏性操作 | 确认中写明目标与后果，取消入口可访问，成功后再更新 UI，或明确提供回滚路径 |
| 排序/文件传输 | 有支持时提供进度、取消/重试/错误；本地拖动或选择文件不等于已持久化/上传 |

姓名、Wizard 摘要、formatter 标签、聊天和文件名应使用文本安全的 DOM 更新。Wizard 示例把输入值插入 `innerHTML`；其外观可复用，数据处理方式不是生产要求。日期示例只定义演示格式，业务时区、显示语言、货币、精度和序列化仍由应用决定。格式化显示不改变保存值，区分零和未知，彩色状态徽章需带明确文字。[S11] [S12]

**建议补充**：准确设置 `lang`，同时测试中英文，允许工具栏与标签换行，保留重要可见文字，长 URL/文件名使用换行或有名称的详情入口。仅 ellipsis/title 不能覆盖移动端和键盘体验。可比较数字右对齐、保留单位/币种，不混淆显示格式与 API 数据；现有权限和授权行为始终有效。

## Do's and Don'ts

### Do

- 保留已选择的侧导航、顶导航或独立认证/异常壳；没有侧栏的页面不强行添加侧栏。
- 优先选择 Bootstrap 语义色、间距、网格、表单和交互组件；AdminLTE 类负责壳与增强组件。
- 用 `.container-fluid` 提供内容内边距，用 `.row`/`.col-*` 组织响应式网格。
- 为所有图标按钮提供名称，为当前菜单、展开状态、验证结果和异步反馈提供可感知状态。
- 同时检查 light、dark、auto、窄屏、键盘、200% 缩放和 `prefers-reduced-motion`。

### Don't

- 不要混用 AdminLTE 3 的 `.main-*` 类与 AdminLTE 4 的 `.app-*` 类。
- 不要硬编码侧栏宽度；源码默认 `$lte-sidebar-width: 250px`，定制应通过导入前的 SCSS 变量覆盖或读取计算样式。
- 不要手动维护 `sidebar-open`、`sidebar-collapse`、`menu-open` 等运行状态来替代插件 API。
- 不要仅靠颜色、图标、占位符或 Toast 传达关键业务信息。
- 不要虚构 Razor、ABP、ASP.NET Core、权限、路由、数据表插件或后端契约。
- 不要复制整套 AdminLTE/Bootstrap API；只实现当前页面所需结构和状态。

## Responsive Behavior

以 Bootstrap 5.3 断点为基线：`sm 576px`、`md 768px`、`lg 992px`、`xl 1200px`、`xxl 1400px`。内容从移动端单列开始，在断点上逐步增加列数，不要以固定像素宽度拼接后台页面。

默认 `sidebar-expand-lg`：在 `992px` 及以上侧栏以内联网格区域显示；在 `992px` 以下变为 off-canvas，默认关闭，`data-lte-toggle="sidebar"` 打开后显示遮罩。移动运行状态由 PushMenu 设置 `body.sidebar-open` 或 `body.sidebar-collapse`。桌面迷你模式使用 `sidebar-mini`，禁止悬停展开可加 `sidebar-without-hover`。

- `xs`（<576px）：单列卡片；标题/面包屑换行；Modal 可全屏；操作组允许纵向排列。
- `sm`（≥576px）：启用小屏工具类，仍优先保障触摸与文本可读。
- `md`（≥768px）：可显示顶部栏的次要文字项，双列内容按信息优先级启用。
- `lg`（≥992px）：默认侧栏进入 inline；主内容与侧栏并排。
- `xl`（≥1200px）与 `xxl`（≥1400px）：可增加网格列，但保持每张卡片的最小可读宽度。

在 320px 视口和 200% 缩放下验证无内容丢失。表格可以使用 `.table-responsive`，但关键操作不得藏在无法发现的横向区域。RTL 时结合 `dir="rtl"`、RTL CSS 与 `layout-rtl` 验证侧栏、间距、方向图标和浮层。

## Accessibility

### AdminLTE 已实现的基础能力

AdminLTE 4 以 WCAG 2.1 AA 为目标，但它只提供起点。`accessibility.ts` 实现单个 polite `#live-region` 与 `announce()`、skip links、通用导航按键、Modal 触发焦点历史及表单错误关联/播报。Treeview 同步 `aria-expanded`；SCSS 提供焦点、减少动画与高对比偏好样式。这些是实现能力，不证明每个 demo 或生成页面都正确使用。发票示例有两个 h1；标题、面包屑、label、表头与图标名称仍是页面级责任。[S6] [S7] [S9]

### 业务页面仍需验证的责任

每个交付页面仍必须检查：语义标题层级、唯一主标题、landmark、链接名称、图片替代文本、表单 label 与错误关联、表格 scope、焦点顺序和焦点可见性、Modal 关闭后的焦点、动态消息播报、颜色对比、200% 缩放、320px 视口、键盘全流程、NVDA 等屏幕阅读器，以及减少动画设置。模板本身不能证明业务应用符合 WCAG。

### 上游已知缺口

- Treeview 与 PushMenu 没有专用的 roving tabindex 或 ARIA tree 键盘模式，静态无 JS 标记不会自带 `aria-expanded`。AdminLTE 的全局 Accessibility 模块已为 `.nav`（包括侧栏导航）提供方向键及 Home/End 导航；不要重复实现或覆盖这层通用行为。
- Kanban 和可排序仪表盘卡片的拖放 demo 没有键盘替代。
- 全局不强制 44×44px 触摸目标；卡片工具按钮可能更小，可按需使用 `.touch-target`。
- 任意组合 Bootstrap 颜色工具类并不保证对比度，需要逐项测量。
- `.github/workflows/a11y.yml` 在 master push 与 PR 上运行 Playwright/axe，使用 Node 22 和构建后的产物。`tests/a11y.mjs` 检查 16 条 demo 路径，仅阻断 serious/critical 问题。缺少 Playwright 时会跳过且不以失败退出；仅退出码为零不能证明测试通过。[S7]
- 上游无障碍声明是历史自述，在自动化方面与实际 CI 不一致。本轮文档更新没有执行该 CI、交互状态审计、对比度测量、NVDA 或 RTL 无障碍检查，结果仍待验证。

## Interaction Contracts

| 契约 | 所在元素 | 运行结果/责任 |
|---|---|---|
| `data-lte-toggle="sidebar"` | 顶部栏按钮或链接 | PushMenu 切换侧栏；可取消的 `open/collapse.lte.push-menu` 在前，`opened/collapsed.lte.push-menu` 在后。 |
| `data-lte-toggle="treeview"` | `.sidebar-menu` 根列表 | Treeview 管理 `.menu-open`、`.nav-treeview` 和 `aria-expanded`；触发 expanded/collapsed 事件。 |
| `data-bs-theme-value` | 主题选择按钮 | 值仅为 `light`、`dark`、`auto`；ColorMode 同步 `.active` 与 `aria-pressed`。 |
| `lte-theme` | `localStorage` | 保存用户主题选择；读取失败必须安全回退。 |
| `sidebar-expand-lg` | `<body>` | `lg`（992px）以上 inline，以下 off-canvas。 |
| `compact-mode` | `body` | 减少壳体 padding；组合 mini 选择器要求 compact 与侧栏状态类在同一 body。 |
| `layout-rtl` | `<body>` | 与 `dir="rtl"` 和 RTL CSS 一起镜像应用壳。 |
| `data-lte-toggle="chat-pane"` | `.direct-chat` 内按钮 | 切换 `.direct-chat-contacts-open`。 |
| `data-bs-toggle="modal"` | Modal 触发器 | 由 Bootstrap 管理打开、焦点约束、Escape 与关闭。 |

运行时状态类由插件拥有；业务可监听事件同步自己的状态，但不要绕过插件直接模拟状态。布局插件在 resize 期间添加 `.hold-transition`，DOMContentLoaded 后延迟添加 `.app-loaded`，自定义入场动画只能在 `.app-loaded` 后启动，并尊重 `prefers-reduced-motion`。

### 插件配置与生命周期

- PushMenu 实例属于 `.app-sidebar`，通过 `adminlte.PushMenu.getOrCreateInstance(sidebar)` 获取。兜底断点为 `991.98`；初始化读取 `body::before` 的实际 CSS 断点。持久化默认 **false**；在侧栏设置 `data-enable-persistence="true"` 才启用，存储键为 `lte.sidebar.state`。桌面偏好与移动遮罩状态不能混用。`opened/collapsed` 在写入状态后触发，不表示 CSS 动画结束。[S6]
- Treeview 默认 `accordion:true`、`animationSpeed:300`。在首次交互前给根 treeview 设置 `data-accordion`/`data-animation-speed`。`expand/collapse.lte.treeview` 是父 nav item 上可取消的前置事件；`expanded/collapsed.lte.treeview` 为后置事件。CardWidget 在 card 上提供可取消的 `collapse/expand/remove.lte.card-widget`，及后置 `collapsed/expanded/removed/maximized/minimized.lte.card-widget`；最大化没有对应的可取消前置事件。[S6]
- 全屏、侧栏搜索和 Direct Chat 契约见前文，不提供路由、消息或业务服务。Bootstrap 拥有其 `data-bs-*` 插件及可配置的焦点/Escape 行为；不要为已有 data API 触发器重复绑定切换逻辑。
- 框架在初次加载后才渲染壳时，DOM 挂载后调用导出的 `adminlte.initialize()`，卸载前调用 `adminlte.teardown()`。生命周期重置 AbortController 绑定的监听并重放初始化。Turbo 自动使用 `turbo:before-render`/`turbo:load`。委托点击已支持后加入节点，不需要每次点击或新增表格行都重新初始化。[S6]
- Bootstrap 实例、OverlayScrollbars、编辑器、图表及业务监听各有销毁要求。AdminLTE teardown 不销毁第三方组件、不取消业务请求，也不重置路由。需验证重新挂载和导航时没有重复监听或残留浮层。

## Assets and Dependency Boundaries

AdminLTE 核心不依赖 jQuery。共享 demo head 独立加载 Source Sans 3、Bootstrap Icons 与 OverlayScrollbars；`_scripts.astro` 依次使用 Popper 2.11.8、Bootstrap 5.3.8 独立 JS、AdminLTE。Bootstrap bundle 已含 Popper，选择一种加载组合即可。`adminlte-docs.css` 是文档站样式，不是业务页面依赖。Demo 的 OverlayScrollbars 只在桌面初始化（`innerWidth > 992`），与 PushMenu 响应式状态相互独立。[S2] [S5]

| 资源 | 精确 demo/锁定版本与包许可元数据 | 使用边界 |
| --- | --- | --- |
| Bootstrap / Popper | [5.3.8, MIT](https://registry.npmjs.org/bootstrap/5.3.8) / [2.11.8, MIT](https://registry.npmjs.org/@popperjs/core/2.11.8) | Bootstrap CSS 已编译进 AdminLTE；JS 独立加载 |
| Bootstrap Icons / Source Sans 3 | [1.13.1, MIT](https://registry.npmjs.org/bootstrap-icons/1.13.1) / [fontsource 5.0.12, OFL-1.1](https://registry.npmjs.org/@fontsource/source-sans-3/5.0.12) | 使用 `bi bi-*`；装饰图标对辅助技术隐藏，操作控件有名称；保留字体许可 |
| OverlayScrollbars | [2.11.0, MIT](https://registry.npmjs.org/overlayscrollbars/2.11.0) | 可选滚动条需要独立初始化和销毁 |
| Tom Select / Flatpickr | [2.6.1, Apache-2.0](https://registry.npmjs.org/tom-select/2.6.1) / [4.6.13, MIT](https://registry.npmjs.org/flatpickr/4.6.13) | 高级表单页面集成，不内置于所有表单 |
| Quill | [2.0.3, BSD-3-Clause](https://registry.npmjs.org/quill/2.0.3) | 独立编辑器主题、工具栏、内容验证和保存 |
| Tabulator | [6.4.0, MIT](https://registry.npmjs.org/tabulator-tables/6.4.0) | 独立表格 CSS/JS 和明确的数据契约 |
| ApexCharts / jsVectorMap | [3.37.1, MIT](https://registry.npmjs.org/apexcharts/3.37.1) / [1.5.3, MIT](https://registry.npmjs.org/jsvectormap/1.5.3) | 演示仪表盘/图表/地图；不能推断后续版本的许可或行为 |
| SortableJS / FullCalendar | [1.15.0, MIT](https://registry.npmjs.org/sortablejs/1.15.0), [1.15.7, MIT](https://registry.npmjs.org/sortablejs/1.15.7) / [6.1.20, MIT](https://registry.npmjs.org/fullcalendar/6.1.20) | 仪表盘与 Kanban 使用不同 Sortable 版本；日历是标准 demo，不含 premium 扩展 |

许可列已核对精确版本 npm 元数据，不等同于全部分发资产和传递依赖的法律审查。不要复制上游集成说明“全部 MIT”的概括。源码 README 致谢 Pixeden、Graphicsfuel、Pickaface、Unsplash、Uifaces、Unavatar，但不能据此认定每张内置图片都适用 AdminLTE 的 MIT 许可。再分发前保留归属并逐项核实图片权利。[S1] [S14]

`adminlte-select2.css` 是适配 Select2 4.0.x/4.1.x 标记的**可选纯 CSS**，不内置 Select2 或 jQuery 运行时。顺序为 AdminLTE CSS、Select2 CSS、适配样式。核对暗色、验证、禁用/多选及 Modal 下拉位置；`z-index:1060` 本身不能解决焦点陷阱，应按实际集成需要设置合适的 `dropdownParent`。仅在 `integrations.mdx` 中推荐的 noUiSlider、Dropzone 等不代表页面已经加载。[S14]

保留现有资源/CDN 政策、CSP、integrity、认证、授权、路由、字段名、后端验证、请求/响应格式、多语言和数据所有权。使用消费项目批准的固定版本或自托管资源。不能把演示上传、本地图表数组、远程 loader 占位实现或只弹 alert 的提交说成生产数据流程已完成。

## Agent Prompt Guide

复制以下框架，并替换方括号内容：

```text
你正在为 AdminLTE 4.3.1（Bootstrap 5.3.8）实现[页面/组件]。
先读取 DESIGN.md，并检查当前页面已有结构；只使用本任务提供的业务事实。

目标：[用户目标与成功标准]
范围：[允许修改的文件/组件]
数据与状态：[字段、空态、加载、成功、失败、禁用、权限可见性]
响应式：[各断点的优先级与可折叠内容]
无障碍：[标题、label、键盘、焦点、live region、对比度要求]

约束：
1. 保留选定的侧导航、顶导航或独立页面壳。
2. 存在侧栏/树菜单时分别使用 data-lte-toggle="sidebar" 和 data-lte-toggle="treeview"。
3. 优先复用 AdminLTE/Bootstrap 的真实类、data 属性和状态，不复制插件逻辑。
4. 同时支持 light/dark/auto；首屏主题不得闪烁。
5. 默认 sidebar-expand-lg 在 992px 以下为 off-canvas。
6. 仅使用已确认依赖；保留既有路由、权限、数据和后端契约。
7. 区分源码事实、依赖继承、应用建议和未验证结果。

交付时列出：使用的真实结构/状态、各断点行为、无障碍处理、验证证据、尚未验证的业务边界。
```

Agent 在编码前应先识别当前壳、页面类型、必要组件、业务状态和所有未知点；未知的后端、权限或插件行为必须提问，不能用演示数据补齐。

## Iteration Guide

每轮设计或实现迭代执行以下检查清单：

- [ ] 确认目标、范围、数据契约和未知项，没有引入未授权技术栈假设。
- [ ] 核对选定壳、内容容器、标题与面包屑，不给独立/顶导航页面强加侧栏。
- [ ] 核对菜单 active/expanded、表单默认/验证/禁用状态。
- [ ] 核对加载/空/失败/成功状态。
- [ ] 核对组件是否优先使用真实 AdminLTE/Bootstrap 类与 data 属性。
- [ ] 在 320px、576px、768px、992px、1200px、1400px 附近验证布局。
- [ ] 存在侧栏时验证 `sidebar-expand-lg` 的 off-canvas/inline 转换、遮罩与键盘入口。
- [ ] 验证 light、dark、auto、`lte-theme` 持久化和首次绘制无闪烁。
- [ ] 验证键盘顺序、焦点可见、Escape、Modal 焦点恢复和动态播报。
- [ ] 验证 label、错误关联、表头 scope、图标名称、颜色之外的状态表达。
- [ ] 验证 200% 缩放、320px、减少动画与必要的 RTL 场景。
- [ ] 对比最终差异与任务目标；记录浏览器、自动化、真实业务数据和生产环境中未验证的部分。

## Known Gaps

- 本文保持 AdminLTE `4.3.1`，Bootstrap peer 范围 `^5.3.8` 在锁文件中解析为 `5.3.8`。只有明确要求将来升级时，才重新审计实现和依赖。[S1]
- token 描述的是当前默认设计基线；实际运行色值由 Bootstrap CSS 自定义属性及 `data-bs-theme` 决定，组件级硬编码不能取代主题变量。
- 本文覆盖固定演示依赖及组合，不是完整 API、全部插件配置、图表数据语义、资产再分发权利或生产集成结果的证明。
- 本文未定义任何服务器框架、模板引擎、身份认证实现、权限、路由、国际化资源或业务数据契约。
- 上游已有有限的自动 axe 门禁；Treeview/PushMenu 专用键盘模式、键盘拖放替代、触摸目标、完整对比度组合、动态状态和 RTL 仍需业务验证。
- `.table-responsive` 能防止溢出，但复杂数据表的列优先级、移动操作入口和替代视图仍由业务设计决定。
- 本轮采用静态源码/文档检查及隔离的主题片段逻辑测试，没有运行 AdminLTE 构建、浏览器截图、axe、屏幕阅读器或真实后端验证，不得把结果称作 UI 验收。

## Sources and Verification

以下链接固定到上游 `v4.3.1` 对应提交 `d635f9396035586a092ee25e6045d03567fa48ca`。表中路径相对于上游仓库；以实际实现为准，不把过时说明当作验证结果。本地工作副本为 `AdminLTE-4.3.1\`，不随规范发布。

| 来源 | 重点文件/目录 |
| --- | --- |
| [S1] | `package.json; package-lock.json; README.md; LICENSE` |
| [S2] | `src/scss/_bootstrap-overrides.scss; _variables.scss; adminlte.scss; dist/css/adminlte.css` |
| [S3] | `src/scss/_app-wrapper.scss; _app-main.scss; _app-header.scss; _app-footer.scss; _app-sidebar.scss; _compact-mode.scss` |
| [S4] | `src/ts/color-mode.ts; src/html/components/_head.astro` |
| [S5] | `src/html/components/_head.astro; _scripts.astro; dashboard/_topbar.astro; dashboard/_sidenav.astro` |
| [S6] | `src/ts/adminlte.ts; util/index.ts; push-menu.ts; treeview.ts; card-widget.ts; direct-chat.ts; sidebar-search.ts; fullscreen.ts; layout.ts; accessibility.ts` |
| [S7] | `.github/workflows/a11y.yml; tests/a11y.mjs; src/ts/accessibility.ts; src/scss/_accessibility.scss; ACCESSIBILITY-COMPLIANCE.md` |
| [S8] | `src/html/pages/layout/*.astro` |
| [S9] | `src/html/pages/*.astro; pages/; examples/; mailbox/; charts/` |
| [S10] | `src/html/pages/UI/general.astro; forms/elements.astro; src/scss/_progress-bars.scss; _toasts.scss` |
| [S11] | `src/html/pages/forms/advanced.astro; editors.astro; wizard.astro; validation.astro; layout.astro` |
| [S12] | `src/html/pages/tables/data.astro; simple.astro; src/html/pages/users.astro` |
| [S13] | `src/scss/_ribbon.scss; _small-box.scss; _info-box.scss; _widgets.scss; src/html/pages/UI/ribbons.astro; widgets/social.astro` |
| [S14] | `src/scss/compat/_select2.scss; src/html/components/docs/integrations.mdx; README.md` |

Bootstrap 继承规则还可核对 [5.3.8 源码](https://github.com/twbs/bootstrap/tree/v5.3.8) 中的 `scss/_variables.scss`、`scss/_variables-dark.scss`、`scss/_buttons.scss`、`scss/forms/` 和 `js/src/`。包许可链接固定到精确版本。应用级建议不冒充上游自带功能。

[S1]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/package-lock.json
[S2]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/scss/_variables.scss
[S3]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/scss/_app-sidebar.scss
[S4]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/ts/color-mode.ts
[S5]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/html/components/_scripts.astro
[S6]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/ts/adminlte.ts
[S7]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/tests/a11y.mjs
[S8]: https://github.com/ColorlibHQ/AdminLTE/tree/d635f9396035586a092ee25e6045d03567fa48ca/src/html/pages/layout
[S9]: https://github.com/ColorlibHQ/AdminLTE/tree/d635f9396035586a092ee25e6045d03567fa48ca/src/html/pages
[S10]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/html/pages/UI/general.astro
[S11]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/html/pages/forms/advanced.astro
[S12]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/html/pages/tables/data.astro
[S13]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/scss/_ribbon.scss
[S14]: https://github.com/ColorlibHQ/AdminLTE/blob/d635f9396035586a092ee25e6045d03567fa48ca/src/scss/compat/_select2.scss
