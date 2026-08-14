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
typography:
  body:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif'
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.5
  body-small:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif'
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.5
  caption:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif'
    fontSize: "0.75rem"
    fontWeight: 400
    lineHeight: 1.5
  title:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif'
    fontSize: "1.75rem"
    fontWeight: 400
    lineHeight: 1.2
  card-title:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif'
    fontSize: "1.1rem"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: '"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif'
    fontSize: "1rem"
    fontWeight: 600
    lineHeight: 1.5
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
    padding: "{spacing.sm}"
  app-sidebar:
    backgroundColor: "{colors.surface-secondary}"
    textColor: "{colors.body-text}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.sm}"
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
    padding: "{spacing.sm}"
  form-control:
    backgroundColor: "{colors.body}"
    textColor: "{colors.body-text}"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: "{spacing.sm}"
  status-danger:
    backgroundColor: "{colors.danger}"
    textColor: "{colors.white}"
    typography: "{typography.caption}"
    rounded: "{rounded.sm}"
    padding: "{spacing.xs}"
  authentication-card:
    backgroundColor: "{colors.body}"
    textColor: "{colors.body-text}"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
---

# AdminLTE 4.3.1 设计开发规范

## Overview

本文是 AdminLTE `4.3.1` 当前源码快照的可执行设计约束，适用于开发者和 AI Agent。AdminLTE 是建立在 Bootstrap `5.3.8` 之上的响应式后台管理界面；视觉语言以 Bootstrap 语义色、Source Sans 3、紧凑信息密度、明确分区和可组合工具类为核心。

规范的优先级是：保留真实 `.app-*` 应用壳与交互契约；优先复用 AdminLTE/Bootstrap 类与数据属性；仅在现有 token、类和组件不足时添加局部样式。本文不定义 ASP.NET Core、ABP、Razor、路由、权限、后端数据或第三方插件约定。

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

## Typography

默认字体取自 AdminLTE 的 Bootstrap 覆盖：`"Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif`。正文以 `{typography.body}` 为基线；`.fs-7` 对应 `0.875rem`，`.fs-8` 对应 `0.75rem`。页面应保持一个可识别的主标题，卡片标题默认 `1.1rem`、常规字重。

- 标题元素按文档层级选择，不因视觉尺寸跳级；`.card-title` 只是样式类，不等同于固定标题级别。
- 元数据、时间和辅助说明使用 `.text-body-secondary` 与较小字号，不用降低透明度隐藏重要信息。
- 按钮和表单标签采用清晰短句；图标不能替代必要文本或可访问名称。
- 表格数字保持可扫描，状态文字不能只靠颜色表达。

## Layout

### 应用壳

所有标准页面使用以下真实区域。`.app-wrapper` 直接位于 `<body>` 内，是 CSS Grid 容器；子元素由类名映射到网格区域，因此源码顺序不决定视觉位置。

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

布局行为由 `<body>` 上的修饰类控制，并可按需组合：`layout-fixed` 让侧栏拥有独立滚动区域；`fixed-header` 将 `.app-header` 固定在视口顶部并同时固定侧栏；`fixed-footer` 将 `.app-footer` 固定在视口底部。固定头部或页脚会减少主内容可用高度，采用前必须在长页面、键盘导航、200% 缩放和移动视口下验证内容不会被遮挡；不要在 `.app-main` 内再用自定义 `position: fixed` 复制这些行为。

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

`.compact-mode` 可加在 `.app-wrapper` 或其祖先上以减少壳体内边距，适用于数据密集页面。RTL 页面必须同时使用 RTL 构建（例如 `adminlte.rtl.min.css`）、`<html dir="rtl">` 和 `body.layout-rtl`；方向图标、图表与第三方控件仍需逐项验证。

## Elevation & Depth

`.card` 默认使用双层轻阴影：`0 0 1px rgba(var(--bs-body-color-rgb), .125), 0 1px 3px rgba(var(--bs-body-color-rgb), .2)`。侧栏示例可加 `.shadow`，头像或图标只在确需分层时用 `.shadow-sm`。层级主要由表面、边框和间距表达，不要为每个块叠加强阴影。

- 普通内容：`.card` 默认阴影。
- 扁平信息：Bootstrap 边框与 `.bg-body`，不再加阴影。
- 浮层：使用 Bootstrap Dropdown、Toast、Modal 自身层级，不手写任意 `z-index`。
- 最大化卡片由 `.maximized-card` 控制；不要复制固定定位逻辑。

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

沿用 Bootstrap `.progress > .progress-bar`，额外尺寸为 `.progress-sm`（10px）、`.progress-xs`（7px）、`.progress-xxs`（3px）；`.progress.vertical` 为垂直形态，`.progress-group` 组合标签与进度。动态条必须给 `.progress-bar` 设置 `role="progressbar"` 与 `aria-valuenow`、`aria-valuemin`、`aria-valuemax`，可见文字应解释百分比代表什么。

### Badge

使用 `.badge.text-bg-*`，圆形状态可加 `.rounded-pill`。Badge 适用于短状态、数量与分类，不用作没有键盘行为的按钮；若可点击，应使用真实 `<a>` 或 `<button>` 并保留 badge 视觉类。

### Timeline

`.timeline` 内以 `.time-label` 分日期；每条由无类 wrapper 包含 `.timeline-icon` 与 `.timeline-item`，后者可含 `.time`、`.timeline-header`、`.timeline-body`、`.timeline-footer`。扁平变体用 `.timeline-inverse`。时间、操作者与动作必须有可读文本。

### Direct Chat

容器为 `.card.direct-chat`，消息和联系人分别用 `.direct-chat-messages`、`.direct-chat-contacts`。切换按钮位于容器内并用 `data-lte-toggle="chat-pane"`；打开状态 `.direct-chat-contacts-open` 由插件管理。可监听 `expanded.lte.direct-chat` 与 `collapsed.lte.direct-chat` 同步业务状态，但不要手动复制插件切换逻辑。

### Toast

使用 Bootstrap `.toast`；AdminLTE 增加 `.toast-{color}` 以同步标题、浅色正文与边框。可访问播报按紧急程度分级：阻断操作、需要立即处理的错误使用 `role="alert"`、`aria-live="assertive"`、`aria-atomic="true"`；普通成功提示和低优先级状态更新使用 `role="status"`、`aria-live="polite"`、`aria-atomic="true"`，避免打断屏幕阅读器当前朗读。关闭按钮使用 `data-bs-dismiss="toast"` 与 `aria-label`。关键失败不能只短暂显示 Toast，还应在页面保留可恢复信息。

### Alert

使用 `.alert.alert-{color}`；可关闭时加 `.alert-dismissible`，关闭按钮使用 `.btn-close`、`data-bs-dismiss="alert"` 和 `aria-label="Close"`。动态插入的 Alert 可由 AdminLTE live region 自动播报。错误、警告和成功消息要有明确文本。

### Modal

触发器使用 `data-bs-toggle="modal"` 与 `data-bs-target="#id"`；结构使用 `.modal > .modal-dialog > .modal-content`，再分 `.modal-header`、`.modal-body`、`.modal-footer`。长内容使用 `.modal-dialog-scrollable`，窄屏可使用 `.modal-fullscreen-lg-down`。Bootstrap 负责对话框内焦点约束与 Escape；AdminLTE 会在关闭后恢复触发焦点，业务需保证标题、说明和关闭路径可访问。

### 认证与锁屏表面

登录/注册使用 `body.login-page.bg-body-secondary` 与 `main.login-box`，内容为 `.card > .login-card-body`，说明用 `.login-box-msg`。可以采用 `.card.card-outline.card-primary` 作为 v2 表面。锁屏使用 `body.lockscreen.bg-body-secondary` 与 `main.lockscreen-wrapper`，核心结构含 `.lockscreen-name`、`.lockscreen-item`、`.lockscreen-image`、`.lockscreen-credentials`。输入必须有显式或 `.visually-hidden` 标签；身份、错误、会话恢复和切换用户逻辑属于业务实现，不由模板假定。

## Do's and Don'ts

### Do

- 保留 `.app-wrapper`、`.app-header`、`.app-sidebar`、`.app-main` 和可选 `.app-footer` 的真实壳结构。
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

AdminLTE 4 以 WCAG 2.1 AA 为目标，但它只提供起点。当前源码记录的基础能力包括：语义化应用壳；单页一个主标题的 demo 约定；带 `aria-label`/`aria-current` 的面包屑；图标控制可访问名称；label 与输入关联；表头 `scope`；单个 polite `#live-region` 与 `announce()`；跳转到主内容/导航的 skip links；Treeview 的 `aria-expanded` 同步；Modal 触发焦点恢复；菜单/下拉的方向键行为；减少动画与高对比偏好样式；表单错误的 `.invalid-feedback`、`aria-describedby` 与 assertive 播报。

### 业务页面仍需验证的责任

每个交付页面仍必须检查：语义标题层级、唯一主标题、landmark、链接名称、图片替代文本、表单 label 与错误关联、表格 scope、焦点顺序和焦点可见性、Modal 关闭后的焦点、动态消息播报、颜色对比、200% 缩放、320px 视口、键盘全流程、NVDA 等屏幕阅读器，以及减少动画设置。模板本身不能证明业务应用符合 WCAG。

### 上游已知缺口

- Treeview 与 PushMenu 没有专用的 roving tabindex 或 ARIA tree 键盘模式，静态无 JS 标记不会自带 `aria-expanded`。AdminLTE 的全局 Accessibility 模块已为 `.nav`（包括侧栏导航）提供方向键及 Home/End 导航；不要重复实现或覆盖这层通用行为。
- Kanban 和可排序仪表盘卡片的拖放 demo 没有键盘替代。
- 全局不强制 44×44px 触摸目标；卡片工具按钮可能更小，可按需使用 `.touch-target`。
- 任意组合 Bootstrap 颜色工具类并不保证对比度，需要逐项测量。
- 当前无自动化 axe/pa11y CI 门禁；上游声明为人工、时间点验证。
- RTL 无障碍审查仍在路线图中。

## Interaction Contracts

| 契约 | 所在元素 | 运行结果/责任 |
|---|---|---|
| `data-lte-toggle="sidebar"` | 顶部栏按钮或链接 | PushMenu 切换侧栏；触发 `open.lte.push-menu` / `collapse.lte.push-menu`。 |
| `data-lte-toggle="treeview"` | `.sidebar-menu` 根列表 | Treeview 管理 `.menu-open`、`.nav-treeview` 和 `aria-expanded`；触发 expanded/collapsed 事件。 |
| `data-bs-theme-value` | 主题选择按钮 | 值仅为 `light`、`dark`、`auto`；ColorMode 同步 `.active` 与 `aria-pressed`。 |
| `lte-theme` | `localStorage` | 保存用户主题选择；读取失败必须安全回退。 |
| `sidebar-expand-lg` | `<body>` | `lg`（992px）以上 inline，以下 off-canvas。 |
| `compact-mode` | `.app-wrapper` 或祖先 | 减少壳体 padding，适配高密度界面。 |
| `layout-rtl` | `<body>` | 与 `dir="rtl"` 和 RTL CSS 一起镜像应用壳。 |
| `data-lte-toggle="chat-pane"` | `.direct-chat` 内按钮 | 切换 `.direct-chat-contacts-open`。 |
| `data-bs-toggle="modal"` | Modal 触发器 | 由 Bootstrap 管理打开、焦点约束、Escape 与关闭。 |

运行时状态类由插件拥有；业务可监听事件同步自己的状态，但不要绕过插件直接模拟状态。布局插件在 resize 期间添加 `.hold-transition`，DOMContentLoaded 后延迟添加 `.app-loaded`，自定义入场动画只能在 `.app-loaded` 后启动，并尊重 `prefers-reduced-motion`。

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
1. 保留 .app-wrapper/.app-header/.app-sidebar/.app-main/可选 .app-footer。
2. 侧栏与树菜单分别使用 data-lte-toggle="sidebar" 和 data-lte-toggle="treeview"。
3. 优先复用 AdminLTE/Bootstrap 的真实类、data 属性和状态，不复制插件逻辑。
4. 同时支持 light/dark/auto；首屏主题不得闪烁。
5. 默认 sidebar-expand-lg 在 992px 以下为 off-canvas。
6. 不假设 ASP.NET Core、ABP、Razor、第三方插件、路由、权限或后端契约。

交付时列出：使用的真实结构/状态、各断点行为、无障碍处理、验证证据、尚未验证的业务边界。
```

Agent 在编码前应先识别当前壳、页面类型、必要组件、业务状态和所有未知点；未知的后端、权限或插件行为必须提问，不能用演示数据补齐。

## Iteration Guide

每轮设计或实现迭代执行以下检查清单：

- [ ] 确认目标、范围、数据契约和未知项，没有引入未授权技术栈假设。
- [ ] 核对 `.app-*` 壳、`.container-fluid`、标题与面包屑结构。
- [ ] 核对菜单 active/expanded、表单默认/验证/禁用、加载/空/失败/成功状态。
- [ ] 核对组件是否优先使用真实 AdminLTE/Bootstrap 类与 data 属性。
- [ ] 在 320px、576px、768px、992px、1200px、1400px 附近验证布局。
- [ ] 验证 `sidebar-expand-lg` 的 off-canvas/inline 转换、遮罩与键盘入口。
- [ ] 验证 light、dark、auto、`lte-theme` 持久化和首次绘制无闪烁。
- [ ] 验证键盘顺序、焦点可见、Escape、Modal 焦点恢复和动态播报。
- [ ] 验证 label、错误关联、表头 scope、图标名称、颜色之外的状态表达。
- [ ] 验证 200% 缩放、320px、减少动画与必要的 RTL 场景。
- [ ] 对比最终差异与任务目标；记录浏览器、自动化、真实业务数据和生产环境中未验证的部分。

## Known Gaps

- 本文基于本地 AdminLTE `4.3.1` 源码快照与 Bootstrap peer dependency `5.3.8`；后续升级需重新核对类、事件、主题脚本和可访问性声明。
- token 描述的是当前默认设计基线；实际运行色值由 Bootstrap CSS 自定义属性及 `data-bs-theme` 决定，组件级硬编码不能取代主题变量。
- 本文未定义图标库选型之外的资产、图表样式、数据可视化语义、编辑器、日历、数据表等第三方集成。
- 本文未定义任何服务器框架、模板引擎、身份认证实现、权限、路由、国际化资源或业务数据契约。
- 上游无障碍仍有 Treeview/PushMenu 专用键盘、拖放替代、全局触摸目标、完整颜色组合对比、自动化 CI 和 RTL 审计缺口；业务项目必须自行补测或补强。
- `.table-responsive` 能防止溢出，但复杂数据表的列优先级、移动操作入口和替代视图仍由业务设计决定。
