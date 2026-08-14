# AdminLTE-admin-design-md

[简体中文](README.md) | [English](README.en-US.md)

[![AdminLTE](https://img.shields.io/badge/AdminLTE-4.3.1-0d6efd)](https://github.com/ColorlibHQ/AdminLTE/releases/tag/v4.3.1)
[![DESIGN.md](https://img.shields.io/badge/DESIGN.md-AI%20ready-198754)](https://stitch.withgoogle.com/docs/design-md/overview/)
[![License](https://img.shields.io/badge/license-MIT-212529)](LICENSE)

面向 AI 编码 Agent、按上游版本维护的 AdminLTE 后台设计系统文档。

`DESIGN.md` 是 Google Stitch 提出的设计系统文档格式：用纯文本 Markdown 记录设计系统，让 AI 编码 Agent 能够生成风格一致的 UI。它描述界面应当呈现的视觉结果、组件结构、交互状态和响应式规则，不替代 AdminLTE 或 Bootstrap 的组件 API 文档。

本仓库从 [ColorlibHQ/AdminLTE](https://github.com/ColorlibHQ/AdminLTE) 官方版本源码提取真实的颜色、字体、尺寸、间距、圆角、阴影、布局与交互契约，并按 AdminLTE 版本独立维护。

## DESIGN.md 的目的与用途

AdminLTE 的设计决策分散在 Bootstrap 变量、SCSS、HTML 示例、TypeScript 插件和无障碍说明中。本规范将这些事实整理为 AI Agent 可以直接读取的上下文，适合：

- 新建后台页面时复用同一套应用壳、主题、密度和组件规则
- 修改现有页面时避免混入 AdminLTE 3 或另一套仪表盘视觉语言
- 评审亮色、暗色、移动端、RTL、键盘和交互状态的一致性
- 升级 AdminLTE 时明确选择与源码版本匹配的规范

## 设计场景

本仓库服务后台 Admin 管理系统，而不是官网或营销落地页。规范重点覆盖：

- 仪表盘、指标卡、进度、时间线和实时状态
- 数据列表、表格、筛选、表单、验证和批量操作
- 顶栏、侧栏、树形菜单、内容标题、面包屑和响应式壳层
- Card、Small Box、Info Box、Callout、Toast、Alert 和 Modal
- Direct Chat、登录、注册、锁屏、空态、加载态和错误反馈
- light、dark、auto 主题，折叠/off-canvas 侧栏，RTL 和无障碍状态

## 支持版本

| AdminLTE 版本 | 英文标准版 | 简体中文版 | GitHub Release |
| --- | --- | --- | --- |
| `4.3.1` | [DESIGN.md](versions/4.3.1/DESIGN.md) | [DESIGN.zh-CN.md](versions/4.3.1/DESIGN.zh-CN.md) | [v4.3.1](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/releases/tag/v4.3.1) |

英文 `DESIGN.md` 是生态兼容的标准版本；中文版保持相同章节、令牌、数值和规则。后续版本使用独立的 `versions\<版本号>` 目录，旧版本不原地覆盖。

## 使用方法

1. 选择与项目所用 AdminLTE 版本一致的目录。
2. 将英文版或中文版下载到项目根目录，并命名为 `DESIGN.md`。
3. 要求 AI 编码 Agent 在生成或修改后台界面前先读取该文件。

Windows PowerShell 下载英文标准版：

```powershell
Invoke-WebRequest `
  -Uri "https://raw.githubusercontent.com/turtoncarllyle/AdminLTE-admin-design-md/main/versions/4.3.1/DESIGN.md" `
  -OutFile ".\DESIGN.md"
```

下载简体中文版：

```powershell
Invoke-WebRequest `
  -Uri "https://raw.githubusercontent.com/turtoncarllyle/AdminLTE-admin-design-md/main/versions/4.3.1/DESIGN.zh-CN.md" `
  -OutFile ".\DESIGN.md"
```

示例提示词：

```text
请读取项目根目录的 DESIGN.md，严格按照 AdminLTE 4.3.1 与 Bootstrap 5.3.8
的应用壳、主题令牌、组件结构、交互契约和响应式规则实现这个后台页面。
请复用真实的 .app-* 类和 data-lte-* 属性，不要混用 AdminLTE 3。
```

## 规范覆盖范围

- Bootstrap 5.3 语义颜色与 light、dark、auto 主题
- Source Sans 3 字体层级、间距、圆角、边框、阴影和动效
- `.app-wrapper`、顶栏、250px 默认侧栏、主内容与可选页脚
- Card、按钮、表单、表格、Small Box、Info Box、Callout 和 Progress
- Timeline、Direct Chat、Toast、Alert、Modal 与认证/锁屏表面
- `576 / 768 / 992 / 1200 / 1400px` 响应式边界、RTL 与 compact mode
- PushMenu、Treeview、CardWidget、ColorMode 的真实数据属性和状态
- 面向 AI Agent 的 Do / Don't、提示词、迭代清单和已知缺口

## 版本与来源

当前规范基于 [AdminLTE v4.3.1](https://github.com/ColorlibHQ/AdminLTE/tree/v4.3.1)，其 Bootstrap peer dependency 为 `^5.3.8`。主要事实来源为 `package.json`、`src\scss\`、`src\ts\`、`src\html\` 与 `ACCESSIBILITY-COMPLIANCE.md`。

本仓库是独立维护的设计系统文档，不隶属于 AdminLTE、ColorlibHQ 或 Google Stitch，也不代表其官方认可。相关名称和标识归各自权利人所有。

## 许可证

本仓库原创文档使用 [MIT License](LICENSE)。AdminLTE 源码仍适用其自身的 [MIT License](https://github.com/ColorlibHQ/AdminLTE/blob/v4.3.1/LICENSE)，第三方依赖遵循各自许可证。
