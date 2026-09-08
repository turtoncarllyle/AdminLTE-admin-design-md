---
version: "4.3.1"
name: "AdminLTE 4.3.1"
description: "Responsive admin interface design and interaction specification based on Bootstrap 5.3.8"
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

# AdminLTE 4.3.1 Design and Development Specification

## Overview

This document is an executable design constraint for the AdminLTE 4.3.1 source snapshot, intended for developers and AI agents. AdminLTE is a responsive admin interface built on Bootstrap 5.3.8. Its visual language centers on Bootstrap semantic colors, Source Sans 3, compact information density, clear regions, and composable utility classes.

Preserve the application's chosen AdminLTE layout and interaction contracts. Reuse AdminLTE and Bootstrap classes and data attributes before adding narrowly scoped custom styles. This document defines visual composition, not a server framework, permission model, or backend API. Existing application routes, authorization, validation, and data contracts take precedence over demo values.

### Evidence and scope

The baseline is upstream tag `v4.3.1`, commit `d635f9396035586a092ee25e6045d03567fa48ca`. `package.json` declares Bootstrap `^5.3.8`; `package-lock.json` resolves exactly `5.3.8`. This is an update to the same design specification, not a dependency upgrade. Resolve conflicts using this order: the consuming project's explicit customization, version-matched implementation and lockfile, executable demo, then explanatory upstream prose. [S1] [S2]

The following labels distinguish responsibilities throughout this document:

- **Source fact**: an AdminLTE class, plugin, asset reference, or executable page in this snapshot.
- **Inherited**: Bootstrap 5.3.8 behavior or a separately loaded, version-pinned dependency.
- **Recommended**: a requirement for production pages that the demo does not implement end to end.
- **Unverified**: a browser, service, accessibility, or licensing result that has not been established by reading source.

The source directory `src\html\pages` is an Astro demo/documentation route inventory. Built names such as `tables/data.html` are evidence for composition, not required application URLs. Ordinary side-navigation pages, top-navigation pages, and standalone authentication/error pages use different shells. There is no built-in route-tab cache, permission router, general CRUD backend, or universal mixed-navigation controller. [S8] [S9]

### Token scope and customization

Front matter describes default roles, not a CSS generator. `content-card.padding` applies to `.card-body`; `authentication-card.padding` applies to `.login-card-body`/`.register-card-body`; `status-danger` describes a default danger badge. Do not apply these values as extra padding on an already styled parent card. The sidebar color variables resolve only inside `.app-sidebar`. The header padding is the default navbar metric, not a fixed-height constraint.

AdminLTE imports Bootstrap SCSS and enables shadows and negative margins. Its compiled `adminlte.css` already contains Bootstrap CSS. Load it once; load Bootstrap JavaScript separately, then AdminLTE JavaScript. Override SCSS variables before the AdminLTE import, including `$primary`, `$font-family-sans-serif`, and `$lte-sidebar-width`. For runtime surfaces, prefer the scoped Bootstrap/AdminLTE CSS properties. Changing only `--bs-primary` does not recolor every compiled `.btn-primary` state; use the button's `--bs-btn-*` properties or rebuild the palette. [S2]

## Colors

Color must convey meaning rather than decoration. Use {colors.primary} for primary actions, {colors.success} for completion, {colors.info} for information, {colors.warning} for caution, {colors.danger} for errors or destructive actions, and {colors.secondary} for secondary information. Prefer Bootstrap combination utilities such as .text-bg-primary, .text-bg-success, and .text-bg-warning so foreground contrast follows the selected background.

Component surfaces must use theme-responsive tokens: {colors.body}, {colors.body-text}, {colors.surface-secondary}, {colors.surface-tertiary}, and {colors.border}. They proxy --bs-body-bg, --bs-body-color, --bs-secondary-bg, --bs-tertiary-bg, and --bs-border-color. Their resolved values change with the Bootstrap data-bs-theme mode. Static tokens ending in -light or -dark document current defaults or deliberately fixed theme regions; they are not general-purpose component surfaces.

Use .bg-body-tertiary or --bs-body-bg for the page background and .bg-body or .card for content surfaces. Borders depend on --bs-border-color; do not hardcode the light-theme #dee2e6 border on dark surfaces. A sidebar may carry data-bs-theme="dark" while the rest of the page follows the global theme.

### Theme modes

- light applies light variables through html[data-bs-theme="light"].
- dark applies dark variables through html[data-bs-theme="dark"].
- auto follows prefers-color-scheme and updates when the OS preference changes.
- Store the user choice in localStorage under lte-theme. Theme controls use data-bs-theme-value="light|dark|auto".
- Resolution priority is the stored user choice, the server-rendered data-bs-theme value, then the OS preference.
- Run a short inline script in head before first paint. It must resolve lte-theme with the same priority as ColorMode and set data-bs-theme plus color-scheme to avoid a theme flash. When the application owns theme management, set data-lte-color-mode="off" on html and make the inline script honor it.

### Surface and state inheritance

The tertiary background is `#f8f9fa` in light mode and `#2b3035` in dark mode. Emphasis text is black/white; secondary text is `rgba(33,37,41,.75)`/`rgba(222,226,230,.75)`. Use `--bs-{color}-bg-subtle`, `--bs-{color}-text-emphasis`, and `--bs-{color}-border-subtle` together for muted status regions. Validation uses `--bs-form-valid-*` and `--bs-form-invalid-*`, whose dark values differ from the ordinary success/danger colors. These are Bootstrap defaults compiled into this version. [S2]

Sidebar navigation has its own palette: light base text `#343a40`, submenu text `#777`, and hover/active backgrounds `rgba(0,0,0,.1)`; dark base/submenu text `#c2c7d0`, white hover/active text, and backgrounds `rgba(255,255,255,.1)`. A selected sidebar link is not automatically a primary-blue block. Use the `--lte-sidebar-*` variables and scope fixed dark palettes to the actual sidebar. [S3]

### Pre-paint initialization and theme updates

**Source fact:** ColorMode distinguishes authored markup from computed markup with `data-lte-theme-resolved`. Omitting this marker can cause an OS-derived theme to become a fixed preference. The upstream head snippet also mishandles stored `auto` when an explicit light/dark markup value exists. **Recommended correction:** the following pre-paint snippet accepts all three valid choices and marks computed output. It is a corrected integration recipe, not a verbatim upstream example. Permit it through the application's existing CSP nonce/hash mechanism. [S4]

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

`new adminlte.ColorMode().setTheme("dark")` in the classic build persists a choice and emits `changed.lte.color-mode` on `document` with `{theme, resolved}`. Initial application and automatic OS changes do not emit this event. A chart or other non-CSS widget must additionally observe `data-bs-theme` or the OS preference if it needs repainting in auto mode. The `off` switch disables automatic/data-API handling; do not call `setTheme()` when a different theme manager owns the page. [S4]

Bootstrap floating content follows the theme of its actual DOM container. A popup moved to `body` cannot inherit a dark theme declared only on an inner panel. Third-party CSS does not acquire complete dark mode just because the root attribute changes; inspect dropdowns, calendars, editors, charts, validation, and disabled states separately. [S14]

## Typography

The default family comes from AdminLTE's Bootstrap override: "Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif. Use {typography.body} as the baseline. .fs-7 is 0.875rem and .fs-8 is 0.75rem. Every page needs one recognizable primary title; card titles default to 1.1rem with regular weight.

- Choose heading elements by document hierarchy, not visual size. .card-title is a style class, not a fixed heading level.
- Use .text-body-secondary and a smaller size for metadata, timestamps, and supporting details. Do not hide important information with low opacity.
- Keep button and form-label text concise and explicit. An icon cannot replace required text or an accessible name.
- Keep numbers in tables scannable, and never express a status with color alone.

### Type, spacing, and control metrics

The full source font stack ends with `"Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"` after `sans-serif`. Load Source Sans 3 separately; declaring its name does not supply a font file or complete Chinese glyph coverage. Preserve a tested system CJK fallback in the consuming project. Body defaults are `1rem`, weight `400`, line height `1.5`; `.form-label` and `.btn` do not become weight `600` automatically. Use `.fw-semibold` only where emphasis is intended. [S2] [S5]

Bootstrap spacing steps `0 / 1 / 2 / 3 / 4 / 5` correspond to `0 / .25 / .5 / 1 / 1.5 / 3rem`; the grid gutter is `1.5rem`. `.fs-1` through `.fs-8` have target sizes `2.5 / 2 / 1.75 / 1.5 / 1.25 / 1 / .875 / .75rem`. Larger headings use Bootstrap RFS below its threshold; `.fs-3` on the demo page heading is not a forced 1.75rem at every width. [S2]

| Element | Default metrics and scope |
| --- | --- |
| Button/input | `.375rem .75rem` padding, `1rem/1.5`, weight `400`, 1px border; nominal 38px height at a 16px root |
| Small/large button/input | `.25rem .5rem` at `.875rem`, or `.5rem 1rem` at `1.25rem`; nominal input heights 31px/48px |
| Select | Same baseline, but `2.25rem` end padding reserves the indicator; do not copy button padding to it |
| Card | Body `1rem`; header/footer `.5rem 1rem`; title `1.1rem`, weight `400` |
| Label/help | Label bottom margin `.5rem`; `.form-text` top margin `.25rem`, size `.875em` |
| Focus/disabled | Input ring `0 0 0 .25rem rgba(13,110,253,.25)`; button ring uses its variant; button disabled opacity `.65` |

Nominal pixel heights are derived defaults, not mandatory fixed heights for multiline content, custom root sizes, or translated labels. [S2]

`typography.title` describes the demo's `h1.fs-3`: weight `500`, line height `1.2`, and an RFS target size of `1.75rem`. `.card-title` sets weight `400` and size `1.1rem` but does not set line height: the token describes a heading-based card title (`1.2`), while a plain div inherits its surrounding line height. Ordinary badges use `.75em`, weight `700`, line height `1`; `.navbar-badge` is a separate override with `.6rem`, weight `400`, and `2px 4px` padding. [S2] [S3]

## Layout

### Application shell

Standard side-navigation pages use the following regions. .app-wrapper is a CSS Grid container directly inside body. Child class names map to grid areas, so source order does not determine visual placement.

~~~html
<body class="layout-fixed sidebar-expand-lg bg-body-tertiary">
  <div class="app-wrapper">
    <nav class="app-header navbar navbar-expand bg-body"><!-- Header --></nav>
    <aside class="app-sidebar bg-body-secondary shadow" data-bs-theme="dark"><!-- Brand and navigation --></aside>
    <main class="app-main">
      <div class="app-content-header"><!-- Title and breadcrumb --></div>
      <div class="app-content"><div class="container-fluid"><!-- Page content --></div></div>
    </main>
    <footer class="app-footer"><!-- Optional footer --></footer>
  </div>
</body>
~~~

The .app-footer is optional. Put the page title and breadcrumb in .app-content-header and business content in .app-content. Their inner wrapper is normally .container-fluid; use .container only when the content needs a maximum width. Never mix AdminLTE 3 .main-* names into this shell.

Body modifiers may be combined deliberately. `layout-fixed` gives the sidebar an independent scroll region. `fixed-header` uses `position: sticky; top: 0`, and also makes the desktop sidebar sticky. `fixed-footer` uses `position: sticky; bottom: 0`. Their names do not mean `position: fixed`; the mobile sidebar does use fixed positioning. Sticky behavior depends on the scroll ancestor. Validate long pages, keyboard navigation, 200% zoom, and mobile viewports with the existing scroll containers. [S3]

### Header

Use .app-header.navbar.navbar-expand.bg-body with an inner .container-fluid. Place the sidebar trigger in the navbar context and use data-lte-toggle="sidebar". Put right-side tools in .navbar-nav.ms-auto. Icon-only controls require aria-label. Notification counts may use .navbar-badge.badge.text-bg-*.

### Sidebar and tree navigation

.app-sidebar contains .sidebar-brand and a scrollable .sidebar-wrapper. The menu root uses .nav.sidebar-menu.flex-column with data-lte-toggle="treeview"; nested lists use .nav.nav-treeview. Add .active to the current link and .menu-open to an initially expanded parent .nav-item. Use .nav-arrow for the parent indicator.

Sidebar width is controlled by the AdminLTE SCSS variable $lte-sidebar-width, whose current default is 250px. Do not freeze that value into a component token. Customize it before importing AdminLTE or read the computed .app-sidebar width at runtime.

~~~html
<nav aria-label="Primary navigation">
  <ul class="nav sidebar-menu flex-column" data-lte-toggle="treeview">
    <li class="nav-item menu-open">
      <a href="#" class="nav-link active">
        <i class="nav-icon bi bi-folder"></i>
        <p>Reports <i class="nav-arrow bi bi-chevron-right"></i></p>
      </a>
      <ul class="nav nav-treeview">
        <li class="nav-item"><a class="nav-link" href="/reports">Sales report</a></li>
      </ul>
    </li>
  </ul>
</nav>
~~~

The sidebar is site navigation, not an application menu widget. Preserve nav, list, and link semantics by default; do not add role="menu" only to the root list. Use the ARIA menu pattern only when menuitem roles and the complete composite-menu keyboard model are implemented together.

### Content header and breadcrumb

Use .app-content-header > .container-fluid. Keep one primary page heading. Put breadcrumbs in nav[aria-label="breadcrumb"] and mark the current item with aria-current="page". Allow title and breadcrumbs to wrap on narrow screens instead of aligning them with absolute positioning.

### Density and direction

`.compact-mode` can style descendants from a wrapper, but put it on `body` alongside `sidebar-mini` and `sidebar-collapse` to activate the combined mini-width selector. RTL requires the RTL build, html[dir="rtl"], and body.layout-rtl together. Validate directional icons, charts, and third-party controls separately. [S3]

### Layout variants and navigation tools

| Source variant | Composition and behavior |
| --- | --- |
| Default/fixed/unfixed sidebar | Grid tracks `auto 1fr`, rows `min-content 1fr min-content`, minimum `100vh`; `layout-fixed` changes scrolling, not the page's semantic regions |
| Mini/collapsed/without-hover | Default width `250px` through `--lte-sidebar-width`; mini `4.6rem`; compact mini `3.1rem`; `sidebar-without-hover` suppresses hover expansion |
| Compact/header/footer | Brand/header baseline `3.5rem`, compact header maximum `2.75rem`; footer minimum `3rem`, padding `1rem` or compact `.5rem` |
| Top navigation | `layout/top-nav.astro` omits the sidebar and `sidebar-expand-*`; use `.navbar-expand-lg` and Bootstrap Collapse for the mobile navbar. Do not add a fake sidebar to fill the grid |
| Custom content areas | `.app-content-top-area` and `.app-content-bottom-area` live inside `.app-main`; bottom area uses `margin-top:auto`, not a global fixed footer |
| Logo switch and menu density | `.logo-xs`/`.logo-xl` with `.brand-link.logo-switch`; `.nav-indent` for submenus and `.nav-compact` for square, adjoining links |

The content header pads `1rem .5rem`; `.app-main` reserves `.75rem` below content. `--lte-sidebar-width` permits runtime width changes, but mini widths and related metrics are separately compiled values; changing one variable is not a complete responsive reskin. [S2] [S3] [S8]

Sidebar filtering uses an input with `data-lte-toggle="sidebar-search"`, optional `data-lte-target="#menu-id"`, and a `[data-lte-search-empty]` element. It matches labels case-insensitively, expands matching ancestors, retains a matched group's subtree, and restores pre-search expansion on clear/Escape. `filtered.lte.sidebar-search` emits `{query, matches}` on the input: `matches` counts visible items including parents; `-1` means reset. Search lives outside `.sidebar-wrapper` in the demo and disappears on the collapsed mini rail until hover expansion. It is a menu filter, not a backend or permission search. [S6]

For header fullscreen controls use `data-lte-toggle="fullscreen"` and child `data-lte-icon="maximize|minimize"` elements. `maximized.lte.fullscreen`/`minimized.lte.fullscreen` follow actual `fullscreenchange`, including Escape exits. A denied request does not emit a fake maximization event. Message/user/notification dropdowns use Bootstrap Dropdown and `.dropdown-menu-end`; their counters and actions are demo content until connected by the application. [S5] [S6]

## Elevation & Depth

A .card uses the light two-layer shadow 0 0 1px rgba(var(--bs-body-color-rgb), .125), 0 1px 3px rgba(var(--bs-body-color-rgb), .2). Sidebar examples may use .shadow; avatars or icons use .shadow-sm only when separation is necessary. Express hierarchy primarily with surfaces, borders, and spacing instead of heavy shadows on every block.

- Normal content uses the default .card shadow.
- Flat information uses Bootstrap borders and .bg-body without another shadow.
- Floating UI uses Bootstrap Dropdown, Toast, and Modal stacking. Do not invent arbitrary z-index values.
- CardWidget owns fixed positioning for .maximized-card; do not duplicate it.

### Stacking and motion

At this baseline the ordinary header is `1034`, sidebar overlay `1037`, sidebar `1038`, and sticky header/footer `1030`. Bootstrap's Offcanvas backdrop/panel are `1040/1045`, Modal backdrop/dialog `1050/1055`, Popover `1070`, Tooltip `1080`, and Toast `1090`. A maximized AdminLTE card is `1050`; the optional Select2 compatibility dropdown is `1060`. These numbers only compare within compatible stacking contexts; clipping, transforms, or portal placement still matter. [S2] [S3] [S14]

Controls normally transition over `.15s`, shell/Treeview/CardWidget over `.3s`/`300ms`, and Direct Chat pane transforms over `.5s`. Reduced-motion CSS shortens animations to `.01ms`; plugin timer callbacks may still wait for their configured duration. Do not assume that a visually shortened animation changes event timing. Prefer one purposeful transition and respect the user's motion setting. [S2] [S6] [S7]

## Shapes

Base radii follow Bootstrap: {rounded.sm} for small elements, {rounded.md} for ordinary cards, buttons, and inputs, and {rounded.lg} for large surfaces such as modals. Use .rounded-circle for avatars and .rounded-pill for pill badges. A Callout is identified by a .25rem inline-start border. AdminLTE Progress defaults to a 1px radius.

Keep radii consistent within a hierarchy. Do not turn every card into an oversized rounded panel or introduce decorative irregular shapes that reduce admin information density.

## Components

### Cards

The standard structure is .card > .card-header + .card-body + .card-footer; the footer is optional. Use .card-title for the title, .card-tools for tools, and .btn.btn-tool with aria-label for icon controls. Theme cards use .card-primary and the other .card-{color} variants. .card-outline turns the theme color into a 3px top border.

Collapse, remove, and maximize actions use data-lte-toggle="card-collapse", data-lte-toggle="card-remove", and data-lte-toggle="card-maximize". Use .collapsed-card for an initially collapsed card. Runtime states such as .maximized-card, .was-collapsed, and .expanding-card belong to CardWidget.

### Buttons

Use Bootstrap .btn with .btn-primary, .btn-secondary, .btn-success, .btn-danger, or .btn-outline-*. Keep one primary action per region in most cases. Use .btn-danger for destructive actions and add confirmation when the action cannot be reversed. Card tools use .btn-tool. Preserve visible default, hover, focus, active, and disabled states; never remove the visible focus indicator.

### Forms and validation

Use .form-control for inputs, .form-select for selects, and .form-check for Boolean controls. Associate every control with a label. On validation failure, add .is-invalid to the control, place .invalid-feedback nearby, and include the error node in aria-describedby. Error text must explain how to correct the value. Use role="alert" or AdminLTE announcement support for dynamic errors, and move focus to an error summary or the first invalid field after a failed submission.

### Tables

Start with .table and add .table-striped, .table-hover, .align-middle, or .table-sm as needed. Header cells require correct scope values. Wrap tables in .table-responsive on narrow screens to prevent card overflow. Also evaluate column priority, wrapping, or an alternate compact view; horizontal scrolling is not the only responsive strategy.

### Small Box

Use .small-box.text-bg-* for high-priority metrics. .inner holds the number and label, .small-box-icon is a watermark icon with aria-hidden="true", and .small-box-footer is a complete link. Never let a large icon carry the metric meaning by itself.

### Info Box

.info-box is a compact metric row. Its core structure is .info-box-icon.text-bg-*, .info-box-content, .info-box-text, and .info-box-number, optionally followed by .progress, .progress-description, and .info-box-more. Long labels may truncate. Preserve complete information with visible wrapping, layout changes, or an accessible name. A title attribute may supplement visible content but cannot be the only way keyboard, touch, or assistive-technology users obtain important information.

### Callout

Use .callout.callout-info|success|warning|danger|primary|secondary for inline explanations and .callout-link for important links inside. Pair border color with a heading, icon, or explicit text so meaning does not depend on color.

### Progress

Use Bootstrap `.progress > .progress-bar`. AdminLTE adds `.progress-sm` at 10px, `.progress-xs` at 7px, `.progress-xxs` at 3px, `.progress.vertical`, and `.progress-group`. Following Bootstrap 5.3, put `role="progressbar"`, a name, and `aria-valuenow/min/max` on the outer `.progress`; the inner `.progress-bar` carries visual width. Do not put duplicate progressbar roles on both elements. For indeterminate progress omit `aria-valuenow`. [S10]

### Badge

Use .badge.text-bg-* and optionally .rounded-pill. Badges represent short states, counts, and categories. They are not non-keyboard buttons. A clickable badge must use a real a or button element while retaining badge styling.

### Timeline

Inside .timeline, divide dates with .time-label. Each event uses a plain wrapper containing .timeline-icon and .timeline-item, which may contain .time, .timeline-header, .timeline-body, and .timeline-footer. Use .timeline-inverse for the flat variant. Time, actor, and action require readable text.

### Direct Chat

Use .card.direct-chat with .direct-chat-messages and .direct-chat-contacts. The in-card toggle uses data-lte-toggle="chat-pane"; the plugin owns .direct-chat-contacts-open. Listen for expanded.lte.direct-chat and collapsed.lte.direct-chat when business state must follow the pane, but do not copy the plugin's toggle logic.

### Toast

Use Bootstrap .toast. AdminLTE adds .toast-{color} to synchronize the header, subtle body, and border. Match announcements to urgency: blocking errors that require immediate attention use role="alert", aria-live="assertive", and aria-atomic="true"; ordinary success notices and low-priority status updates use role="status", aria-live="polite", and aria-atomic="true". Close controls use data-bs-dismiss="toast" and aria-label. A critical failure must also leave recoverable information on the page instead of existing only in a temporary Toast.

Call `bootstrap.Toast.getOrCreateInstance(toastElement).show()` to show it. `data-bs-toggle="toast"` in `UI/general.astro` works through that page's click listener; it is not an automatic Bootstrap toggle API. Tooltip and Popover also need explicit initialization, for example `bootstrap.Tooltip.getOrCreateInstance(element)`, and disposal when their host is removed. [S10]

### Alert

Use .alert.alert-{color}. A dismissible alert adds .alert-dismissible and a .btn-close with data-bs-dismiss="alert" plus aria-label="Close". AdminLTE's live region can announce dynamically inserted alerts. Error, warning, and success messages need explicit text.

### Modal

Triggers use data-bs-toggle="modal" and data-bs-target="#id". Structure the dialog as .modal > .modal-dialog > .modal-content, followed by .modal-header, .modal-body, and .modal-footer. Use .modal-dialog-scrollable for long content and .modal-fullscreen-lg-down when a narrow viewport requires it. Bootstrap constrains focus and handles Escape; AdminLTE restores trigger focus after close. The application must provide an accessible title, description, and close path.

### Authentication and lockscreen surfaces

Sign-in and registration use body.login-page.bg-body-secondary or body.register-page.bg-body-secondary with main.login-box or main.register-box. Content uses .card > .login-card-body or .register-card-body with .login-box-msg or .register-box-msg. .card.card-outline.card-primary is available for the v2 surface. Lockscreen uses body.lockscreen.bg-body-secondary and main.lockscreen-wrapper with .lockscreen-name, .lockscreen-item, .lockscreen-image, and .lockscreen-credentials. Inputs require explicit or .visually-hidden labels. Identity, errors, session recovery, and user switching are application responsibilities.

Login/register boxes default to `400px`; at `max-width:576px` they become `90%` wide. Body padding is `20px`, not the ordinary card body's `1rem`. The v2 pages use floating labels; `examples/forgot-password.astro` supplies the recovery-page composition, not a real email delivery flow. [S9]

The authentication body uses `--bs-secondary-color`, not the ordinary card text token. Its input-group focus rule removes the box shadow while preserving border feedback; assess visible focus in that context rather than assuming the ordinary input ring is present. These overrides live in `src/scss/pages/_login_and_register.scss`. [S2]

### Selection, tabs, pagination, and drawers

**Inherited**, demonstrated in `forms/elements.astro` and `UI/general.astro`: use `.form-check-input` for checkboxes/radios, `.form-switch` for a Boolean switch, `.form-range` for native range inputs, `.input-group` for add-ons, and `.form-floating` with a label after its input. Reflect checked, indeterminate, readonly, disabled, invalid, and focused states on the real control, not just the wrapper. Readonly and disabled are different states. [S10]

Tabs use `.nav-tabs`/`.nav-pills`, `data-bs-toggle="tab|pill"`, and corresponding `.tab-pane` elements with tablist/tab/tabpanel relationships. They are local content tabs; no route caching or visited-page tab bar is supplied. Pagination uses `.pagination > .page-item > .page-link`, `aria-current="page"`, and genuinely unavailable previous/next controls. Bootstrap supplies appearance, not a dataset pager. [S10]

Use `.accordion` with Bootstrap Collapse for FAQs. Use `.offcanvas-start|end|top|bottom`, `data-bs-toggle="offcanvas"`, labelled title, dismiss button, and Bootstrap's lifecycle for a drawer. Sidebar PushMenu is a separate component and does not inherit Offcanvas focus trapping or Escape behavior. [S6] [S10]

### Version-pinned advanced forms and data tables

`forms/advanced.astro` loads **Tom Select 2.6.1** with its Bootstrap 5 stylesheet and **Flatpickr 4.6.13**. Single selects use `clear_button`; tags use `remove_button` and `create:true` where free entry is intended. The remote reviewer demo uses `valueField:"id"`, `labelField:"name"`, `loadThrottle:300`, `virtual_scroll`, and an AbortController to discard superseded requests. `{results,next}` is the demo loader shape, not the consuming application's mandatory API. Preserve stable IDs, selected values, keyboard access, labels, loading, no-results, and retry states when integrating real data. [S11]

Flatpickr examples use `Y-m-d`, `Y-m-d H:i`, `mode:"range"`, and time-only `H:i` with `time_24hr:true`. The page does not establish a business timezone or date serialization contract. `forms/editors.astro` loads **Quill 2.0.3** Snow and Bubble themes; retain the configured toolbar and provide an accessible editor name. Persisted rich text requires the application's existing validation/sanitization policy. [S11]

`tables/data.astro` loads **Tabulator 6.4.0** and `tabulator_bootstrap5.min.css`. Its local-data example uses `layout:"fitColumns"`, pagination size `10`, choices `[10,25,50,100]`, movable columns, input/list header filters, a name/email OR search, status badges, CSV/JSON export, and print. These behaviors are implemented on the page; they are not DataTables/jQuery or server-side paging. When resetting, clear global and header filters deliberately. Preserve the existing application's paging/sort/export contracts rather than treating demo data as an API. Arbitrary user strings must not be interpolated into formatter HTML without escaping. [S12]

### Ribbons and social widgets

The `4.3.1` ribbon fills a clipped card corner: `.ribbon-wrapper` on a positioned parent, inner `.ribbon`, square sizes `70 / 110 / 145px`, band widths `91 / 143 / 188.5px`, and font sizes `.8 / 1 / 1.25rem`. Use `.ribbon-lg`/`.ribbon-xl` on the wrapper. Leave space for its short text and tools; a ribbon must not cover the title or action target. [S13]

Social patterns include `.user-block` (avatar `2.5rem`, small `1.75rem`), `.post`, `.description-block`, `.widget-user`, and `.widget-user-2`. The first profile header is `8.4375rem` tall with a `5.625rem` overhanging avatar; the second uses a `4.0625rem` inline avatar. Small Box metrics default to `2.2rem` with column-specific reductions; Info Box minimum height is `80px` with a `70px` icon region. These are component-specific metrics, not a reason to enlarge every card. [S13]

## Page Patterns

**Source facts** below describe actual page compositions. Rows marked demo require application logic before their controls represent successful operations. Paths are relative to `src\html\pages`. [S9]

| Page family | Structure, behavior, and integration boundary |
| --- | --- |
| `index.astro`, `index2.astro`, `index3.astro` | Metric grid, chart cards, tables/activity; ApexCharts 3.37.1, with jsVectorMap 1.5.3 and SortableJS 1.15.0 on the first dashboard; series, maps, and dates are demo values |
| `users.astro`, `tables/simple.astro` | Card header with wrapping search/role/actions, `.card-body.p-0`, responsive table, badges, row actions, pager, add-user Modal; directory filters/save are visual controls, unlike the working Tabulator example |
| `forms/layout.astro`, `forms/validation.astro` | Vertical/horizontal/grid/floating-label composition, input groups, HTML validity and Bootstrap feedback; preserve field names, server errors, and submission contracts |
| `forms/wizard.astro` | Previous/Next/Submit, step visibility, active/completed indicators, per-step validity, confirmation summary; final submit only displays an alert. Recommended: text-safe summary rendering, focus transfer, whole-form validation, and duplicate-submit protection |
| `pages/profile.astro`, `pages/settings.astro` | Avatar/about/activity and edit forms; settings use `col-md-3` list-group pills plus `col-md-9` content for account, notifications, security, billing, and danger. Two-factor, billing, and deletion are UI examples |
| `pages/projects.astro` | Summary counters, project filters/table, avatars, progress, state badges, and row commands; detail routing and edits must use existing application contracts |
| `pages/gallery.astro` | Responsive image grid, category controls with `aria-pressed`, visible count, empty state, and image Modal; filtering is implemented locally |
| `pages/file-manager.astro` | Folder navigation, storage summary, file grid/list modes; mode switch is implemented locally. Upload, delete, and download require actual services |
| `pages/search-results.astro` | Search input, content tabs, labelled result summaries, pagination; data and search results are demo content |
| `pages/chat.astro` | Separate `.chat-app` grid with `320px` contacts, `1fr` conversation, `calc(100vh - 14rem)` height and `32rem` minimum; local send appends text safely. At `max-width:768px` contacts are hidden without a replacement picker; recommend adding one for a real chat |
| `pages/calendar.astro`, `pages/kanban.astro` | FullCalendar 6.1.20 and SortableJS 1.15.7 respectively; calendar events and cross-lane card moves are local. Kanban uses `repeat(auto-fit,minmax(280px,1fr))`, `1rem` gap. Add keyboard moves and persistence/rollback for business use |
| `mailbox/inbox.astro`, `mailbox/read.astro`, `mailbox/compose.astro` | Folder list plus message table, message detail, and recipient/subject/editor/attachment composition; no mailbox service, upload pipeline, or actual send flow |
| `pages/invoice.astro`, `pages/pricing.astro` | Printable invoice and totals; tier comparison/pricing cards. Preserve numeric/currency contracts; correct the invoice demo's duplicate h1 instead of copying it |
| `pages/faq.astro`, `pages/404.astro`, `pages/500.astro`, `pages/maintenance.astro` | FAQ accordion; standalone error/maintenance surfaces with visible recovery links. Do not force the side-navigation shell into standalone errors |
| `examples/*.astro` | Login/register and v2 variants, password recovery, lockscreen; authentication/session rules remain application-owned |
| `layout/*.astro`, `generate/theme.astro`, `UI/*.astro`, `widgets/*.astro` | Layout variants, theme-generation demo, component showcases; generated colors/classes are customization examples, not additional light/dark preference values |

Standalone chat page styles are not the `.direct-chat` widget's styles: the page uses `.chat-message.me` and `.chat-bubble` (1rem radius, 70% maximum width), while the widget uses `.direct-chat-text`. Page-specific styles are not included in `adminlte.css`; port only the chosen page's scoped rules. Pricing and standalone chat may have page-specific shape exceptions; ordinary operational cards keep the baseline radius. [S9]

## State and Content Rules

The following are **recommended application rules**, grounded in gaps in the demos rather than claimed as automatic AdminLTE behavior.

| Trigger/state | Required visible result and recovery |
| --- | --- |
| Initial load or refresh | Stable region dimensions, labelled spinner/placeholder and `aria-busy`; retain usable filters and previously loaded data where appropriate |
| No records / no filter matches | Distinct empty messages; offer the relevant create or clear-filter action without inventing records |
| Validation failure | Keep values, associate text with the field, reflect `aria-invalid`, and focus a summary/first invalid field; revalidate hidden wizard steps before final submission |
| Request failure | Stop loading, retain user input, show an actionable error, allow retry, and distinguish unauthenticated/forbidden/conflict states using real response contracts |
| Pending submit / success | Guard repeated invocation, disable the in-flight command, restore it on completion, and announce success only after confirmation from the real operation |
| Selection and bulk action | Name the selection scope (page or all matching records), expose indeterminate state and selected count, handle partial success, and retain failed selections for retry |
| Destructive action | Name the target and consequence in confirmation, keep Cancel accessible, and update UI only after success or with an explicit rollback path |
| Reorder / file transfer | Expose progress, cancel/retry/error states when supported; local dragging or choosing a file is not proof of persistence/upload |

Use text-safe DOM updates for names, wizard summaries, formatter labels, chat, and file names. The wizard demo interpolates entered values into `innerHTML`; its appearance is reusable, that data handling is not a production requirement. Date pickers expose demo formats but the application chooses timezone, display locale, currency, precision, and serialization. Use localized formatting without altering stored values, distinguish zero from unknown, and pair colored status badges with meaningful text. [S11] [S12]

**Recommended:** set `lang` accurately, test both Chinese and English, let toolbars and labels wrap, preserve visible essential text, and constrain long URLs/file names with wrapping or a named details affordance. An ellipsis/title attribute alone is not a complete mobile or keyboard experience. Right-align comparable numbers, retain units/currency, and avoid conflating display formatting with API data. Existing permissions and authorization behavior must remain authoritative.

## Do's and Don'ts

### Do

- Preserve the chosen shell: side navigation, top navigation, or standalone authentication/error. Do not add a sidebar to a page that has none.
- Prefer Bootstrap semantic colors, spacing, grid, forms, and interaction components; use AdminLTE for the shell and enhanced components.
- Use .container-fluid for content padding and .row with .col-* for responsive grids.
- Give icon controls accessible names and expose current navigation, expanded state, validation, and async feedback.
- Check light, dark, auto, narrow screens, keyboard use, 200% zoom, and prefers-reduced-motion.

### Don't

- Do not mix AdminLTE 3 .main-* classes with the AdminLTE 4 .app-* shell.
- Do not hardcode sidebar width. The current $lte-sidebar-width default is 250px; customize the SCSS variable before import or read computed styles.
- Do not manually maintain sidebar-open, sidebar-collapse, menu-open, or other runtime states in place of plugin APIs.
- Do not communicate critical information through color, icons, placeholders, or Toast alone.
- Do not invent Razor, ABP, ASP.NET Core, permission, routing, data-table plugin, or backend contracts.
- Do not copy the entire AdminLTE or Bootstrap API into a page; implement only the structures and states the page needs.

## Responsive Behavior

Use the Bootstrap 5.3 breakpoints: sm 576px, md 768px, lg 992px, xl 1200px, and xxl 1400px. Start with a single-column mobile layout and add columns progressively. Do not assemble an admin page from fixed pixel widths.

The default sidebar-expand-lg keeps the sidebar inline at 992px and above. Below 992px it becomes off-canvas, starts closed, and displays an overlay when opened through data-lte-toggle="sidebar". PushMenu applies body.sidebar-open or body.sidebar-collapse at runtime. Use sidebar-mini for the desktop mini state and sidebar-without-hover to disable hover expansion.

- xs below 576px: one-column cards, wrapping title and breadcrumb, optionally fullscreen modal, and stackable action groups.
- sm at 576px and above: small-screen utilities become available; touch access and readable text remain priorities.
- md at 768px and above: secondary header text and two-column content may appear according to information priority.
- lg at 992px and above: the default sidebar becomes inline beside main content.
- xl at 1200px and xxl at 1400px: add grid columns only while preserving minimum readable card widths.

Validate at a 320px viewport and 200% zoom without content loss. .table-responsive may prevent overflow, but critical actions cannot be hidden in an undiscoverable horizontal area. For RTL, test dir="rtl", the RTL CSS build, layout-rtl, sidebar placement, spacing, directional icons, and floating UI together.

## Accessibility

### Foundation provided by AdminLTE

AdminLTE 4 targets WCAG 2.1 AA, but it is only a starting point. `accessibility.ts` implements one polite `#live-region` with `announce()`, skip links, generic navigation keys, modal trigger-focus history, and form-error associations/announcements. Treeview synchronizes `aria-expanded`; SCSS supplies focus, reduced-motion, and high-contrast preference styles. These are implementation capabilities, not proof that every demo or generated page uses them correctly. The invoice example has two h1 elements; meaningful headings, breadcrumbs, labels, table headers, and icon names remain page-level obligations. [S6] [S7] [S9]

### Application verification responsibilities

Every delivered page must still verify heading hierarchy, a unique primary heading, landmarks, link names, image alternatives, labels and error associations, table scope, focus order and visibility, focus after Modal close, dynamic announcements, color contrast, 200% zoom, a 320px viewport, the full keyboard path, screen readers such as NVDA, and reduced-motion settings. The template cannot prove that a business application conforms to WCAG.

### Known upstream gaps

- Treeview and PushMenu do not implement dedicated roving tabindex or an ARIA tree keyboard model, and static no-JavaScript markup does not acquire aria-expanded. The global Accessibility module already provides Arrow and Home/End navigation for .nav, including sidebar navigation; do not replace this general behavior.
- Kanban and sortable dashboard-card demos do not provide keyboard drag alternatives.
- A global 44 by 44px touch target is not enforced. Card tool buttons may be smaller; add .touch-target when necessary.
- Arbitrary combinations of Bootstrap color utilities do not guarantee contrast and must be measured.
- `.github/workflows/a11y.yml` does run Playwright/axe on master pushes and PRs, using Node 22 and a built distribution. `tests/a11y.mjs` checks 16 demo paths and gates only serious/critical findings. Missing Playwright produces a skip with no failing exit code; an exit code of zero alone is not test evidence. [S7]
- The upstream accessibility statement is a historical self-report and disagrees with the executable CI on automation. This documentation update did not run that CI, interactive-state audits, contrast measurements, NVDA, or RTL accessibility checks; those results remain unverified.

## Interaction Contracts

| Contract | Owner element | Runtime result or responsibility |
|---|---|---|
| data-lte-toggle="sidebar" | Header button or link | PushMenu toggles the sidebar; cancelable `open/collapse.lte.push-menu` precede `opened/collapsed.lte.push-menu`. |
| data-lte-toggle="treeview" | .sidebar-menu root list | Treeview manages .menu-open, .nav-treeview, aria-expanded, and expanded/collapsed events. |
| data-bs-theme-value | Theme option button | Value is light, dark, or auto; ColorMode synchronizes .active and aria-pressed. |
| lte-theme | localStorage | Stores the user's theme selection and must fail safely when storage is unavailable. |
| sidebar-expand-lg | body | Sidebar is inline at lg 992px and off-canvas below it. |
| compact-mode | body | Reduces shell padding; combined mini selectors require compact and sidebar state classes on the same body. |
| layout-rtl | body | Mirrors the shell when used with dir="rtl" and the RTL CSS build. |
| data-lte-toggle="chat-pane" | Button inside .direct-chat | Toggles .direct-chat-contacts-open. |
| data-bs-toggle="modal" | Modal trigger | Bootstrap owns open, focus constraint, Escape, and close behavior. |

Plugins own runtime state classes. Business code may listen for events to synchronize its own state but must not bypass plugins to imitate it. Layout adds .hold-transition during resize and delays .app-loaded until after DOMContentLoaded. Custom entrance motion begins only after .app-loaded and honors prefers-reduced-motion.

### Plugin configuration and lifecycle

- PushMenu is owned by `.app-sidebar`, accessible through `adminlte.PushMenu.getOrCreateInstance(sidebar)`. The fallback breakpoint is `991.98`; initialization reads the effective `body::before` CSS breakpoint. Persistence defaults to **false**; opt in with `data-enable-persistence="true"` on the sidebar and storage key `lte.sidebar.state`. Desktop preference and mobile overlay state are not interchangeable. `opened/collapsed` are dispatched after state writes, not after the CSS transition ends. [S6]
- Treeview defaults to `accordion:true`, `animationSpeed:300`. Set `data-accordion`/`data-animation-speed` on the root treeview before its first interaction. `expand/collapse.lte.treeview` are cancelable before-events on the parent nav item; `expanded/collapsed.lte.treeview` are after-events. CardWidget similarly offers cancelable `collapse/expand/remove.lte.card-widget` and after-events `collapsed/expanded/removed/maximized/minimized.lte.card-widget` on the card. Maximization has no corresponding cancelable before-event. [S6]
- Fullscreen, sidebar search, and Direct Chat contracts are described above; they do not create routing, messaging, or business services. Bootstrap owns its `data-bs-*` plugins and their configurable focus/Escape behavior; do not bind a second toggle handler to an existing data-API trigger.
- For a framework that renders the shell after initial load, call exported `adminlte.initialize()` once the DOM is attached and `adminlte.teardown()` before unmount. The lifecycle resets AbortController-bound listeners and replays registered initialization. Turbo uses `turbo:before-render`/`turbo:load` automatically. Delegated click handlers already work for later nodes; repeated initialization is not required for every click or row. [S6]
- Bootstrap instances, OverlayScrollbars, editors, charts, and business listeners have their own disposal requirements. AdminLTE teardown does not destroy third-party widgets, cancel application fetches, or reset a router. Test remounts and navigation for duplicate handlers and stale portals.

## Assets and Dependency Boundaries

AdminLTE's core does not require jQuery. The shared demo head loads Source Sans 3, Bootstrap Icons, and OverlayScrollbars independently; `_scripts.astro` uses Popper 2.11.8, Bootstrap 5.3.8 standalone JS, then AdminLTE. A Bootstrap bundle already includes Popper: choose one loading arrangement. `adminlte-docs.css` is documentation-site styling, not a business-page requirement. The demo's OverlayScrollbars initialization is desktop-only (`innerWidth > 992`) and separate from PushMenu's responsive state. [S2] [S5]

| Resource | Exact demo/lock version and package license metadata | Use boundary |
| --- | --- | --- |
| Bootstrap / Popper | [5.3.8, MIT](https://registry.npmjs.org/bootstrap/5.3.8) / [2.11.8, MIT](https://registry.npmjs.org/@popperjs/core/2.11.8) | Bootstrap CSS is already compiled into AdminLTE; JS is separate |
| Bootstrap Icons / Source Sans 3 | [1.13.1, MIT](https://registry.npmjs.org/bootstrap-icons/1.13.1) / [fontsource 5.0.12, OFL-1.1](https://registry.npmjs.org/@fontsource/source-sans-3/5.0.12) | Use `bi bi-*`; decorative icons are hidden from accessibility APIs, controls have names; retain font notices |
| OverlayScrollbars | [2.11.0, MIT](https://registry.npmjs.org/overlayscrollbars/2.11.0) | Optional independent scrollbar initialization and teardown |
| Tom Select / Flatpickr | [2.6.1, Apache-2.0](https://registry.npmjs.org/tom-select/2.6.1) / [4.6.13, MIT](https://registry.npmjs.org/flatpickr/4.6.13) | Advanced-form page integrations, not built into every form |
| Quill | [2.0.3, BSD-3-Clause](https://registry.npmjs.org/quill/2.0.3) | Separate editor theme, toolbar, content validation and persistence |
| Tabulator | [6.4.0, MIT](https://registry.npmjs.org/tabulator-tables/6.4.0) | Separate table CSS/JS and explicit data contract |
| ApexCharts / jsVectorMap | [3.37.1, MIT](https://registry.npmjs.org/apexcharts/3.37.1) / [1.5.3, MIT](https://registry.npmjs.org/jsvectormap/1.5.3) | Demo dashboard/chart/map widgets; do not infer licenses or behavior of later versions |
| SortableJS / FullCalendar | [1.15.0, MIT](https://registry.npmjs.org/sortablejs/1.15.0), [1.15.7, MIT](https://registry.npmjs.org/sortablejs/1.15.7) / [6.1.20, MIT](https://registry.npmjs.org/fullcalendar/6.1.20) | Dashboard and Kanban intentionally reference different Sortable versions; standard calendar demo, not premium extensions |

The license column was checked against exact-version npm metadata, not a legal review of all distributed assets/transitive packages. Do not copy the upstream integration prose's blanket "all MIT" claim. The source README credits Pixeden, Graphicsfuel, Pickaface, Unsplash, Uifaces, and Unavatar; it does not establish that every bundled image can be reused under AdminLTE's MIT license. Keep attribution and verify the particular image's rights before redistribution. [S1] [S14]

`adminlte-select2.css` is an **optional CSS-only** adapter for Select2 4.0.x/4.1.x markup, not a bundled Select2 or jQuery runtime. Load AdminLTE CSS, Select2 CSS, then the adapter. Test dark mode, validation, disabled/multiple selections, and modal dropdown placement; `z-index:1060` alone does not solve a focus trap, so configure a suitable `dropdownParent` when required by the actual integration. Libraries mentioned only in `integrations.mdx`, such as noUiSlider or Dropzone, are recommendations, not evidence that a page loads them. [S14]

Preserve existing asset/CDN policies, CSP, integrity attributes, authentication, authorization, routes, field names, backend validation, request/response shapes, localization, and data ownership. Use version-pinned or self-hosted assets approved by the consuming application. Never turn a demo upload, local chart array, placeholder remote loader, or alert-only submit into a claim of working production data flow.

## Agent Prompt Guide

Copy this frame and replace the bracketed content:

~~~text
You are implementing [page or component] with AdminLTE 4.3.1 and Bootstrap 5.3.8.
Read DESIGN.md first and inspect the page's existing structure. Use only the
business facts supplied by this task.

Goal: [user outcome and success criteria]
Scope: [files or components that may change]
Data and states: [fields, empty, loading, success, failure, disabled, visibility]
Responsive behavior: [priority and collapsible content at each breakpoint]
Accessibility: [headings, labels, keyboard, focus, live region, contrast]

Constraints:
1. Preserve the chosen side-navigation, top-navigation, or standalone shell.
2. If present, use data-lte-toggle="sidebar" and data-lte-toggle="treeview" for navigation.
3. Reuse real AdminLTE and Bootstrap classes, data attributes, and states.
4. Support light, dark, and auto without a first-paint theme flash.
5. sidebar-expand-lg is off-canvas below 992px by default.
6. Use only confirmed dependencies; preserve existing routes, permissions, data and backend contracts.
7. Separate source facts, inherited behavior, application recommendations, and unverified results.

At delivery, list real structures and states used, breakpoint behavior,
accessibility handling, verification evidence, and unverified business boundaries.
~~~

Before coding, identify the existing shell, page type, required components, business states, and all unknowns. Ask about unknown backend, permission, or plugin behavior instead of filling gaps with demo data.

## Iteration Guide

- [ ] Confirm the goal, scope, data contract, and unknowns without adding unauthorized stack assumptions.
- [ ] Check the selected shell, content container, title, and breadcrumb structure without forcing a sidebar into standalone/top-navigation pages.
- [ ] Check navigation active/expanded states and form default/validation/disabled states.
- [ ] Check loading, empty, failure, and success states.
- [ ] Confirm that components use real AdminLTE and Bootstrap classes and data attributes first.
- [ ] Test near 320, 576, 768, 992, 1200, and 1400px.
- [ ] Where a sidebar exists, test sidebar-expand-lg off-canvas/inline transitions, overlay, and keyboard entry.
- [ ] Test light, dark, auto, lte-theme persistence, and first paint without a flash.
- [ ] Test keyboard order, visible focus, Escape, Modal focus restoration, and announcements.
- [ ] Check labels, error associations, table scope, icon names, and non-color status cues.
- [ ] Check 200% zoom, 320px, reduced motion, and required RTL scenarios.
- [ ] Compare the final diff with the task goal and record browser, automation, real-data, and production boundaries.

## Known Gaps

- This specification stays on AdminLTE `4.3.1`, with Bootstrap peer range `^5.3.8` resolved to `5.3.8` in the lockfile. Re-audit implementation and dependencies only when a future upgrade is explicitly requested. [S1]
- Tokens describe the current default design baseline. Runtime colors resolve through Bootstrap custom properties and data-bs-theme; component hardcoding cannot replace theme variables.
- Fixed demo dependencies and their composition are covered, not their complete APIs, every plugin configuration, chart data semantics, asset redistribution rights, or production integration results.
- It does not define a server framework, template engine, authentication implementation, permissions, routing, internationalization resources, or business data contracts.
- Upstream has a limited automated axe gate; dedicated Treeview/PushMenu keyboard patterns, keyboard drag alternatives, touch targets, complete contrast combinations, dynamic states, and RTL still need application verification.
- .table-responsive prevents overflow but does not define column priority, mobile action placement, or alternate complex-table views.
- This update used static source/document checks and isolated theme-snippet logic tests, not a running AdminLTE build, browser screenshots, axe execution, screen-reader testing, or live backend verification. Those results must not be reported as UI acceptance.

## Sources and Verification

Links below are pinned to upstream `v4.3.1` commit `d635f9396035586a092ee25e6045d03567fa48ca`. Paths are relative to the upstream repository; implementation takes precedence over stale explanatory claims. The local working copy is `AdminLTE-4.3.1\` and is not distributed with this specification.

| Source | Key files/directories |
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

For inherited Bootstrap rules, also consult the [5.3.8 source](https://github.com/twbs/bootstrap/tree/v5.3.8), specifically `scss/_variables.scss`, `scss/_variables-dark.scss`, `scss/_buttons.scss`, `scss/forms/`, and `js/src/`. Package-license links use exact versions. Recommended application rules are not represented as built-in upstream features.

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
