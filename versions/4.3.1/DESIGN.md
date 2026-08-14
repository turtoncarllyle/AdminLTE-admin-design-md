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

# AdminLTE 4.3.1 Design and Development Specification

## Overview

This document is an executable design constraint for the AdminLTE 4.3.1 source snapshot, intended for developers and AI agents. AdminLTE is a responsive admin interface built on Bootstrap 5.3.8. Its visual language centers on Bootstrap semantic colors, Source Sans 3, compact information density, clear regions, and composable utility classes.

Preserve the real .app-* application shell and interaction contracts. Reuse AdminLTE and Bootstrap classes and data attributes before adding narrowly scoped custom styles. This document does not define ASP.NET Core, ABP, Razor, routing, permissions, backend data, or third-party plugin contracts.

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

## Typography

The default family comes from AdminLTE's Bootstrap override: "Source Sans 3", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif. Use {typography.body} as the baseline. .fs-7 is 0.875rem and .fs-8 is 0.75rem. Every page needs one recognizable primary title; card titles default to 1.1rem with regular weight.

- Choose heading elements by document hierarchy, not visual size. .card-title is a style class, not a fixed heading level.
- Use .text-body-secondary and a smaller size for metadata, timestamps, and supporting details. Do not hide important information with low opacity.
- Keep button and form-label text concise and explicit. An icon cannot replace required text or an accessible name.
- Keep numbers in tables scannable, and never express a status with color alone.

## Layout

### Application shell

Every standard page uses the following real regions. .app-wrapper is a CSS Grid container directly inside body. Child class names map to grid areas, so source order does not determine visual placement.

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

Body modifiers may be combined deliberately. layout-fixed gives the sidebar an independent scroll region. fixed-header pins the header and sidebar to the viewport. fixed-footer pins the footer. Fixed regions reduce available main-content height; validate long pages, keyboard navigation, 200% zoom, and mobile viewports before using them. Do not recreate these behaviors with custom fixed positioning inside .app-main.

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

Add .compact-mode to .app-wrapper or an ancestor to reduce shell padding on data-dense pages. RTL requires the RTL build, html[dir="rtl"], and body.layout-rtl together. Validate directional icons, charts, and third-party controls separately.

## Elevation & Depth

A .card uses the light two-layer shadow 0 0 1px rgba(var(--bs-body-color-rgb), .125), 0 1px 3px rgba(var(--bs-body-color-rgb), .2). Sidebar examples may use .shadow; avatars or icons use .shadow-sm only when separation is necessary. Express hierarchy primarily with surfaces, borders, and spacing instead of heavy shadows on every block.

- Normal content uses the default .card shadow.
- Flat information uses Bootstrap borders and .bg-body without another shadow.
- Floating UI uses Bootstrap Dropdown, Toast, and Modal stacking. Do not invent arbitrary z-index values.
- CardWidget owns fixed positioning for .maximized-card; do not duplicate it.

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

Use Bootstrap .progress > .progress-bar. AdminLTE adds .progress-sm at 10px, .progress-xs at 7px, .progress-xxs at 3px, .progress.vertical, and .progress-group. A dynamic progress bar needs role="progressbar", aria-valuenow, aria-valuemin, and aria-valuemax. Visible text must explain what the percentage represents.

### Badge

Use .badge.text-bg-* and optionally .rounded-pill. Badges represent short states, counts, and categories. They are not non-keyboard buttons. A clickable badge must use a real a or button element while retaining badge styling.

### Timeline

Inside .timeline, divide dates with .time-label. Each event uses a plain wrapper containing .timeline-icon and .timeline-item, which may contain .time, .timeline-header, .timeline-body, and .timeline-footer. Use .timeline-inverse for the flat variant. Time, actor, and action require readable text.

### Direct Chat

Use .card.direct-chat with .direct-chat-messages and .direct-chat-contacts. The in-card toggle uses data-lte-toggle="chat-pane"; the plugin owns .direct-chat-contacts-open. Listen for expanded.lte.direct-chat and collapsed.lte.direct-chat when business state must follow the pane, but do not copy the plugin's toggle logic.

### Toast

Use Bootstrap .toast. AdminLTE adds .toast-{color} to synchronize the header, subtle body, and border. Match announcements to urgency: blocking errors that require immediate attention use role="alert", aria-live="assertive", and aria-atomic="true"; ordinary success notices and low-priority status updates use role="status", aria-live="polite", and aria-atomic="true". Close controls use data-bs-dismiss="toast" and aria-label. A critical failure must also leave recoverable information on the page instead of existing only in a temporary Toast.

### Alert

Use .alert.alert-{color}. A dismissible alert adds .alert-dismissible and a .btn-close with data-bs-dismiss="alert" plus aria-label="Close". AdminLTE's live region can announce dynamically inserted alerts. Error, warning, and success messages need explicit text.

### Modal

Triggers use data-bs-toggle="modal" and data-bs-target="#id". Structure the dialog as .modal > .modal-dialog > .modal-content, followed by .modal-header, .modal-body, and .modal-footer. Use .modal-dialog-scrollable for long content and .modal-fullscreen-lg-down when a narrow viewport requires it. Bootstrap constrains focus and handles Escape; AdminLTE restores trigger focus after close. The application must provide an accessible title, description, and close path.

### Authentication and lockscreen surfaces

Sign-in and registration use body.login-page.bg-body-secondary or body.register-page.bg-body-secondary with main.login-box or main.register-box. Content uses .card > .login-card-body or .register-card-body with .login-box-msg or .register-box-msg. .card.card-outline.card-primary is available for the v2 surface. Lockscreen uses body.lockscreen.bg-body-secondary and main.lockscreen-wrapper with .lockscreen-name, .lockscreen-item, .lockscreen-image, and .lockscreen-credentials. Inputs require explicit or .visually-hidden labels. Identity, errors, session recovery, and user switching are application responsibilities.

## Do's and Don'ts

### Do

- Preserve the real .app-wrapper, .app-header, .app-sidebar, .app-main, and optional .app-footer shell.
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

AdminLTE 4 targets WCAG 2.1 AA, but it is only a starting point. The current source documents a semantic shell; one primary heading per demo page; breadcrumbs with aria-label and aria-current; named icon controls; associated labels and inputs; table-header scope; one polite #live-region with announce(); skip links to main content and navigation; Treeview aria-expanded synchronization; Modal trigger-focus restoration; directional menu and dropdown navigation; reduced-motion and high-contrast preference styles; and form errors using .invalid-feedback, aria-describedby, and assertive announcements.

### Application verification responsibilities

Every delivered page must still verify heading hierarchy, a unique primary heading, landmarks, link names, image alternatives, labels and error associations, table scope, focus order and visibility, focus after Modal close, dynamic announcements, color contrast, 200% zoom, a 320px viewport, the full keyboard path, screen readers such as NVDA, and reduced-motion settings. The template cannot prove that a business application conforms to WCAG.

### Known upstream gaps

- Treeview and PushMenu do not implement dedicated roving tabindex or an ARIA tree keyboard model, and static no-JavaScript markup does not acquire aria-expanded. The global Accessibility module already provides Arrow and Home/End navigation for .nav, including sidebar navigation; do not replace this general behavior.
- Kanban and sortable dashboard-card demos do not provide keyboard drag alternatives.
- A global 44 by 44px touch target is not enforced. Card tool buttons may be smaller; add .touch-target when necessary.
- Arbitrary combinations of Bootstrap color utilities do not guarantee contrast and must be measured.
- There is no automated axe or pa11y CI gate; upstream describes manual, point-in-time testing.
- RTL accessibility review remains on the upstream roadmap.

## Interaction Contracts

| Contract | Owner element | Runtime result or responsibility |
|---|---|---|
| data-lte-toggle="sidebar" | Header button or link | PushMenu toggles the sidebar and emits open.lte.push-menu or collapse.lte.push-menu. |
| data-lte-toggle="treeview" | .sidebar-menu root list | Treeview manages .menu-open, .nav-treeview, aria-expanded, and expanded/collapsed events. |
| data-bs-theme-value | Theme option button | Value is light, dark, or auto; ColorMode synchronizes .active and aria-pressed. |
| lte-theme | localStorage | Stores the user's theme selection and must fail safely when storage is unavailable. |
| sidebar-expand-lg | body | Sidebar is inline at lg 992px and off-canvas below it. |
| compact-mode | .app-wrapper or ancestor | Reduces shell padding for data-dense interfaces. |
| layout-rtl | body | Mirrors the shell when used with dir="rtl" and the RTL CSS build. |
| data-lte-toggle="chat-pane" | Button inside .direct-chat | Toggles .direct-chat-contacts-open. |
| data-bs-toggle="modal" | Modal trigger | Bootstrap owns open, focus constraint, Escape, and close behavior. |

Plugins own runtime state classes. Business code may listen for events to synchronize its own state but must not bypass plugins to imitate it. Layout adds .hold-transition during resize and delays .app-loaded until after DOMContentLoaded. Custom entrance motion begins only after .app-loaded and honors prefers-reduced-motion.

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
1. Preserve .app-wrapper/.app-header/.app-sidebar/.app-main/optional .app-footer.
2. Use data-lte-toggle="sidebar" and data-lte-toggle="treeview" for navigation.
3. Reuse real AdminLTE and Bootstrap classes, data attributes, and states.
4. Support light, dark, and auto without a first-paint theme flash.
5. sidebar-expand-lg is off-canvas below 992px by default.
6. Do not assume ASP.NET Core, ABP, Razor, plugins, routes, permissions, or backend contracts.

At delivery, list real structures and states used, breakpoint behavior,
accessibility handling, verification evidence, and unverified business boundaries.
~~~

Before coding, identify the existing shell, page type, required components, business states, and all unknowns. Ask about unknown backend, permission, or plugin behavior instead of filling gaps with demo data.

## Iteration Guide

- [ ] Confirm the goal, scope, data contract, and unknowns without adding unauthorized stack assumptions.
- [ ] Check the .app-* shell, .container-fluid, title, and breadcrumb structure.
- [ ] Check navigation active/expanded states and form default/validation/disabled states.
- [ ] Check loading, empty, failure, and success states.
- [ ] Confirm that components use real AdminLTE and Bootstrap classes and data attributes first.
- [ ] Test near 320, 576, 768, 992, 1200, and 1400px.
- [ ] Test sidebar-expand-lg off-canvas/inline transitions, overlay, and keyboard entry.
- [ ] Test light, dark, auto, lte-theme persistence, and first paint without a flash.
- [ ] Test keyboard order, visible focus, Escape, Modal focus restoration, and announcements.
- [ ] Check labels, error associations, table scope, icon names, and non-color status cues.
- [ ] Check 200% zoom, 320px, reduced motion, and required RTL scenarios.
- [ ] Compare the final diff with the task goal and record browser, automation, real-data, and production boundaries.

## Known Gaps

- This specification is based on the local AdminLTE 4.3.1 source snapshot and Bootstrap peer dependency 5.3.8. Re-audit classes, events, theme scripts, and accessibility statements after an upgrade.
- Tokens describe the current default design baseline. Runtime colors resolve through Bootstrap custom properties and data-bs-theme; component hardcoding cannot replace theme variables.
- This document does not define asset choices beyond icon-library usage, chart semantics, data visualization, editors, calendars, data tables, or other third-party integrations.
- It does not define a server framework, template engine, authentication implementation, permissions, routing, internationalization resources, or business data contracts.
- Upstream accessibility gaps remain around dedicated Treeview/PushMenu keyboard patterns, drag alternatives, global touch targets, complete color-combination contrast, automated CI, and RTL audit.
- .table-responsive prevents overflow but does not define column priority, mobile action placement, or alternate complex-table views.
