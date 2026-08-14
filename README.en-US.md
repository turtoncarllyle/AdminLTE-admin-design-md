# AdminLTE-admin-design-md

[简体中文](README.md) | [English](README.en-US.md)

[![AdminLTE](https://img.shields.io/badge/AdminLTE-4.3.1-0d6efd)](https://github.com/ColorlibHQ/AdminLTE/releases/tag/v4.3.1)
[![DESIGN.md](https://img.shields.io/badge/DESIGN.md-AI%20ready-198754)](https://stitch.withgoogle.com/docs/design-md/overview/)
[![License](https://img.shields.io/badge/license-MIT-212529)](LICENSE)

A versioned AdminLTE admin design-system document for AI coding agents.

`DESIGN.md` is a design-system document format introduced by Google Stitch. It records a design system in plain-text Markdown so AI coding agents can generate consistent UI. It describes the intended visual result, component structure, interaction states, and responsive rules; it does not replace the AdminLTE or Bootstrap component API documentation.

This repository extracts real colors, typography, dimensions, spacing, radii, shadows, layouts, and interaction contracts from official [ColorlibHQ/AdminLTE](https://github.com/ColorlibHQ/AdminLTE) releases and maintains them separately for each AdminLTE version.

## Purpose and Use

AdminLTE design decisions are distributed across Bootstrap variables, SCSS, HTML examples, TypeScript plugins, and accessibility notes. This specification turns those facts into context that an AI agent can read directly. Use it to:

- Reuse the same application shell, theme, density, and component rules on new admin pages
- Keep changes from introducing AdminLTE 3 conventions or another dashboard visual language
- Review light, dark, mobile, RTL, keyboard, and interaction states consistently
- Select the specification that matches the source version during AdminLTE upgrades

## Design Scenarios

This repository is for operational admin systems, not marketing sites. It focuses on:

- Dashboards, metric cards, progress, timelines, and live status
- Data lists, tables, filters, forms, validation, and bulk actions
- Headers, sidebars, tree navigation, content headers, breadcrumbs, and the responsive shell
- Cards, Small Boxes, Info Boxes, Callouts, Toasts, Alerts, and Modals
- Direct Chat, sign-in, registration, lockscreen, empty, loading, and error states
- Light, dark, and auto themes; collapsed/off-canvas sidebars; RTL; and accessibility states

## Supported Versions

| AdminLTE version | Canonical English | Simplified Chinese | GitHub Release |
| --- | --- | --- | --- |
| `4.3.1` | [DESIGN.md](versions/4.3.1/DESIGN.md) | [DESIGN.zh-CN.md](versions/4.3.1/DESIGN.zh-CN.md) | [v4.3.1](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/releases/tag/v4.3.1) |

The English `DESIGN.md` is the canonical ecosystem-compatible edition. The Chinese edition preserves the same sections, tokens, values, and rules. Future versions use separate `versions\<version>` directories; published versions are not overwritten in place.

## Usage

1. Select the directory that matches your project's AdminLTE version.
2. Download either language edition to the project root and name it `DESIGN.md`.
3. Tell the AI coding agent to read the file before generating or changing admin UI.

Download the canonical English edition with Windows PowerShell:

```powershell
Invoke-WebRequest `
  -Uri "https://raw.githubusercontent.com/turtoncarllyle/AdminLTE-admin-design-md/main/versions/4.3.1/DESIGN.md" `
  -OutFile ".\DESIGN.md"
```

Download the Simplified Chinese edition:

```powershell
Invoke-WebRequest `
  -Uri "https://raw.githubusercontent.com/turtoncarllyle/AdminLTE-admin-design-md/main/versions/4.3.1/DESIGN.zh-CN.md" `
  -OutFile ".\DESIGN.md"
```

Example prompt:

```text
Read DESIGN.md in the project root. Implement this admin page using the real
AdminLTE 4.3.1 and Bootstrap 5.3.8 shell, theme tokens, component structures,
interaction contracts, and responsive rules. Reuse .app-* classes and
data-lte-* attributes; do not mix in AdminLTE 3 conventions.
```

## Coverage

- Bootstrap 5.3 semantic colors and light, dark, and auto themes
- Source Sans 3 type hierarchy, spacing, radii, borders, shadows, and motion
- `.app-wrapper`, header, 250px default sidebar, main content, and optional footer
- Cards, buttons, forms, tables, Small Boxes, Info Boxes, Callouts, and Progress
- Timeline, Direct Chat, Toast, Alert, Modal, authentication, and lockscreen surfaces
- `576 / 768 / 992 / 1200 / 1400px` breakpoints, RTL, and compact mode
- Real PushMenu, Treeview, CardWidget, and ColorMode attributes and states
- Agent-facing Do / Don't rules, prompts, iteration checks, and known gaps

## Version and Source

The current specification is based on [AdminLTE v4.3.1](https://github.com/ColorlibHQ/AdminLTE/tree/v4.3.1), whose Bootstrap peer dependency is `^5.3.8`. Primary evidence comes from `package.json`, `src\scss\`, `src\ts\`, `src\html\`, and `ACCESSIBILITY-COMPLIANCE.md`.

This is an independently maintained design-system document. It is not affiliated with or endorsed by AdminLTE, ColorlibHQ, or Google Stitch. Related names and marks belong to their respective owners.

## License

Original documentation in this repository is released under the [MIT License](LICENSE). AdminLTE source remains subject to [its own MIT license](https://github.com/ColorlibHQ/AdminLTE/blob/v4.3.1/LICENSE), and third-party dependencies remain subject to their respective licenses.
