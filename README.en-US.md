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

| AdminLTE version | Maintained English | Maintained Chinese | Initial release snapshot |
| --- | --- | --- | --- |
| `4.3.1` | [DESIGN.md](versions/4.3.1/DESIGN.md) | [DESIGN.zh-CN.md](versions/4.3.1/DESIGN.zh-CN.md) | [v4.3.1](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/releases/tag/v4.3.1) |

The English `DESIGN.md` is the canonical ecosystem-compatible edition. The Chinese edition preserves the same sections, tokens, values, and rules. This update improves `versions\4.3.1` in place, keeping metadata at `4.3.1` without a new revision number or frontend dependency upgrade. A different upstream version would use a separate directory.

`main` contains the latest maintained documentation for this version. The original `v4.3.1` tag, Release, and assets remain the initial snapshot, not this update. Read the [completeness audit and verification record](AUDIT.md) (Simplified Chinese) for evidence, changes, and unverified areas.

## Usage

1. Select the directory that matches your project's AdminLTE version.
2. Download either language edition to the project root and name it `DESIGN.md`.
3. Tell the AI coding agent to read the file before generating or changing admin UI.
4. Supply the selected shell, business goal, real data/permission/routing contracts, and permitted scope; do not let the agent mistake demo controls for working services.

The URLs below download the maintained `4.3.1` edition. For reproducible results, replace `main` with the full Git commit SHA you selected and record it in the consuming project. The version identifies the upstream baseline; the commit SHA distinguishes documentation updates within that version.

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

- Locked Bootstrap 5.3.8 baseline, semantic colors, independent sidebar palette, and light/dark/auto themes
- Source Sans 3 type hierarchy, spacing, radii, borders, shadows, and motion
- Side navigation, top navigation, standalone authentication/errors, sticky header/footer, and 250px default sidebar
- Cards, buttons, forms, tables, Small Boxes, Info Boxes, Callouts, and Progress
- Timeline, Direct Chat, Toast, Alert, Modal, authentication, and lockscreen surfaces
- `576 / 768 / 992 / 1200 / 1400px` breakpoints, RTL, and compact mode
- PushMenu, Treeview, CardWidget, ColorMode, SidebarSearch, Fullscreen, and mount/teardown lifecycles
- Tom Select/Flatpickr/Quill forms, Tabulator tables, tabs/drawers, ribbons, and social widgets
- Profile/settings, projects, file manager, gallery, mailbox, chat, calendar, Kanban, invoice, FAQ, and error page patterns
- Versioned assets/licenses, success/failure recovery, keyboard boundaries, actual axe CI scope, and unverified areas
- Agent-facing Do / Don't rules, prompts, iteration checks, and known gaps

## Version and Source

The specification is based on the [fixed AdminLTE v4.3.1 commit](https://github.com/ColorlibHQ/AdminLTE/tree/d635f9396035586a092ee25e6045d03567fa48ca). Bootstrap's peer range is `^5.3.8`, resolved to `5.3.8` in the lockfile. Evidence comes from package metadata, SCSS/compiled CSS, TypeScript, Astro pages, and the executable `.github\workflows\a11y.yml`/`tests\a11y.mjs`. The upstream accessibility self-report has stale statements and cannot replace implementation or test evidence.

The specification separates source facts, inherited behavior, application recommendations, and unverified results. This update checked documents, versioned sources, and isolated theme-snippet logic. It did not install frontend dependencies, run the application, or complete UI/accessibility acceptance.

Traceability: [initial document commit 5edbd12](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/tree/5edbd128e519e0319df5f4372277f192be60a300), [4.3.1 maintenance history](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/commits/main/versions/4.3.1), and [original v4.3.1 Release](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/releases/tag/v4.3.1). Historical tags and attachments are not replaced; any future republication needs a separately confirmed scope.

This is an independently maintained design-system document. It is not affiliated with or endorsed by AdminLTE, ColorlibHQ, or Google Stitch. Related names and marks belong to their respective owners.

## License

Original documentation in this repository is released under the [MIT License](LICENSE). AdminLTE source remains subject to [its own MIT license](https://github.com/ColorlibHQ/AdminLTE/blob/v4.3.1/LICENSE), and third-party dependencies remain subject to their respective licenses.
