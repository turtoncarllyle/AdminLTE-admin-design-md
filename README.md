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

| AdminLTE 版本 | 英文当前维护版 | 中文当前维护版 | 首次发布快照 |
| --- | --- | --- | --- |
| `4.3.1` | [DESIGN.md](versions/4.3.1/DESIGN.md) | [DESIGN.zh-CN.md](versions/4.3.1/DESIGN.zh-CN.md) | [v4.3.1](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/releases/tag/v4.3.1) |

英文 `DESIGN.md` 是生态兼容的标准版本；中文版保持相同章节、令牌、数值和规则。本次继续在 `versions\4.3.1` 补充当前规范，元数据仍为 `4.3.1`，不新增修订版本号，也不升级前端依赖。不同上游版本才使用新的版本目录。

`main` 指向同一版本的最新维护内容；原 `v4.3.1` 标签、Release 和附件保留首次发布快照，不代表本次更新。查看 [完整性审计与验收记录](AUDIT.md) 了解证据、补充范围和未验证事项。

## 使用方法

1. 选择与项目所用 AdminLTE 版本一致的目录。
2. 将英文版或中文版下载到项目根目录，并命名为 `DESIGN.md`。
3. 要求 AI 编码 Agent 在生成或修改后台界面前先读取该文件。
4. 提供所选壳类型、业务目标、真实数据/权限/路由合同和允许修改范围；不要让 Agent 将 demo 控件当作已实现服务。

以下地址下载的是 `4.3.1` 当前维护版。需要固定结果时，将 URL 中的 `main` 替换为所采用的完整 Git commit SHA，并在项目中记录它。版本号说明上游基线，提交 SHA 区分同版本的文档更新。

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

- Bootstrap 5.3.8 锁定基线、语义颜色、侧栏独立色板与 light、dark、auto 主题
- Source Sans 3 字体层级、间距、圆角、边框、阴影和动效
- 侧导航、顶导航、独立认证/异常壳、sticky 顶栏/页脚、250px 默认侧栏
- Card、按钮、表单、表格、Small Box、Info Box、Callout 和 Progress
- Timeline、Direct Chat、Toast、Alert、Modal 与认证/锁屏表面
- `576 / 768 / 992 / 1200 / 1400px` 响应式边界、RTL 与 compact mode
- PushMenu、Treeview、CardWidget、ColorMode、SidebarSearch、Fullscreen 与挂载/销毁生命周期
- 高级表单 Tom Select/Flatpickr/Quill、Tabulator 数据表、标签页/抽屉、Ribbon 和社交组件
- 资料/设置、项目、文件管理、图库、邮件、聊天、日历、Kanban、发票、FAQ 与异常页面模式
- 资源版本与许可、业务成功/失败恢复、键盘边界、真实 axe CI 范围与未验证项
- 面向 AI Agent 的 Do / Don't、提示词、迭代清单和已知缺口

## 版本与来源

当前规范基于 [AdminLTE v4.3.1 固定提交](https://github.com/ColorlibHQ/AdminLTE/tree/d635f9396035586a092ee25e6045d03567fa48ca)，Bootstrap peer dependency 为 `^5.3.8`，锁文件解析为 `5.3.8`。事实来自 `package.json`、`package-lock.json`、SCSS/编译 CSS、TypeScript、Astro 页面以及实际 `.github\workflows\a11y.yml`/`tests\a11y.mjs`。上游无障碍自述存在过时内容，不能替代实现或测试结果。

规范区分“源码事实”“依赖继承”“应用建议”“待验证”。本轮只验证文档、版本化来源和隔离的主题片段逻辑，没有安装前端依赖、运行页面或完成 UI/无障碍验收。

历史可追溯入口：[首次文档提交 5edbd12](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/tree/5edbd128e519e0319df5f4372277f192be60a300)、[4.3.1 维护历史](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/commits/main/versions/4.3.1)、[原 v4.3.1 Release](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/releases/tag/v4.3.1)。不移动历史标签、不替换旧附件；后续如需正式重发，另行确认发布范围。

本仓库是独立维护的设计系统文档，不隶属于 AdminLTE、ColorlibHQ 或 Google Stitch，也不代表其官方认可。相关名称和标识归各自权利人所有。

## 许可证

本仓库原创文档使用 [MIT License](LICENSE)。AdminLTE 源码仍适用其自身的 [MIT License](https://github.com/ColorlibHQ/AdminLTE/blob/v4.3.1/LICENSE)，第三方依赖遵循各自许可证。
