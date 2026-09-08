# AdminLTE 4.3.1 完整性审计与更新记录

审计日期：2026-09-08。范围是同一上游版本的规范完善，不是升级 AdminLTE 或 Bootstrap。本轮已按用户要求进入实施阶段；提交只包含设计文档，不包含参考源码、构建产物或依赖安装。

## 基线与仓库边界

- 文档仓库：[turtoncarllyle/AdminLTE-admin-design-md](https://github.com/turtoncarllyle/AdminLTE-admin-design-md)，本地 `E:\github\admin-ui-design-md\AdminLTE-design-md`。
- 审计前 `main`、`origin/main` 和 `v4.3.1` 指向 [5edbd128e519e0319df5f4372277f192be60a300](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/tree/5edbd128e519e0319df5f4372277f192be60a300)，工作区干净。
- 参考源码为本地 `AdminLTE-4.3.1\`，已被 Git 忽略。官方 `v4.3.1` 对应 [d635f9396035586a092ee25e6045d03567fa48ca](https://github.com/ColorlibHQ/AdminLTE/tree/d635f9396035586a092ee25e6045d03567fa48ca)。包声明和锁文件都核对，Bootstrap 的 `^5.3.8` 范围实际锁定 `5.3.8`。
- 文档入口：[英文标准版](versions/4.3.1/DESIGN.md)、[简体中文版](versions/4.3.1/DESIGN.zh-CN.md)。两份规范有相同章节顺序、令牌、技术值和规则。
- 参考任务“设计 layui 2.13.9 规范并推送”用于双语入口和版本组织，不将其框架、组件、数值或账户历史套用到 AdminLTE。

## 总体结论

旧规范可以指导侧导航壳、Bootstrap 基础组件、指标卡、基础表单、认证表面及一般响应式页面，但不能充分支持顶导航、完整页面族、真实第三方组件、延迟挂载/卸载和复杂业务状态。部分错误直接改变视觉结果；另有将历史无障碍声明当作当前事实的问题。

本轮补充后，Agent 可以据此选择真实壳与页面组合，理解核心插件所有权和生命周期，接入固定版本高级表单/数据表，并知道哪些控件仍只是 demo。它仍不代替插件完整 API、业务合同、第三方许可审查或实际页面验收。未发现需要切换上游版本的理由。

## 重要问题与处理

严重程度针对规范误导风险，不等同于已经验证的生产事故。审计前文档位置均可在 [旧英文规范](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/blob/5edbd128e519e0319df5f4372277f192be60a300/versions/4.3.1/DESIGN.md) 与 [旧中文规范](https://github.com/turtoncarllyle/AdminLTE-admin-design-md/blob/5edbd128e519e0319df5f4372277f192be60a300/versions/4.3.1/DESIGN.zh-CN.md) 核实。

| 优先级 | 问题及证据 | 影响 | 本轮处理与验证方式 |
| --- | --- | --- | --- |
| P1 | front matter 把 label/button 字重写为 600、页面标题写为 400、卡片标题行高固定 1.5，按钮/输入 padding 用统一 `.5rem`；侧栏文字引用全局 body，认证内容按 1rem；Badge 套用普通 caption。实际 SCSS/编译 CSS 的作用域与值不同 [S2] [S3] | AI 重建时密度、标题、侧栏对比、徽章与认证页面偏离 | 修正 label/button 400、页面标题 500、标题型卡片行高 1.2、控件 `.375rem .75rem`、侧栏独立变量、认证 20px 与 secondary-color；Badge 为 `.75em/700/1`。补作用域、控件尺寸和覆盖顺序；以 YAML 及 CSS 声明核对 |
| P1 | Layout、Do、Prompt 强制每页有侧栏，忽略 `layout/top-nav.astro` 和独立异常页；fixed-header/footer 实际使用 sticky；compact mini 要求组合类在同一 body [S3] [S8] [S9] | 生成错误壳，窄屏与固定定位行为不符 | 按三种壳分类；修正定位说明和组合选择器；静态核对 Astro 与 SCSS，真实滚动/缩放待浏览器验证 |
| P1 | Colors 只有主题规则，没有可直接核对的首屏片段及 `data-lte-theme-resolved`；上游 `_head.astro` 对 stored auto + authored light/dark 的分支与 ColorMode 不一致 [S4] | 首屏主题错误、OS 自动跟随被误当作固定偏好 | 给出标记为“建议修正”的片段，明确 CSP、off、存储失败、事件边界；隔离执行主题组合测试，首屏绘制仍待浏览器验证 |
| P1 | Known Gaps 将第三方一概排除，但源码真实加载 Tom Select、Flatpickr、Quill、Tabulator 等 [S11] [S12] | Agent 可能误用 jQuery DataTables，或为已存在组件另造方案 | 补精确版本、CSS、配置、状态、数据契约和清理边界；与页面脚本/精确版本 npm 元数据核对 |
| P1 | 页面族、提交/上传/拖动等 demo 边界缺失；Wizard 输入插入 innerHTML，最终只 alert；文件管理没有真实上传服务 [S9] [S11] | 视觉按钮被当作成功流程，生产代码可能照搬不安全的数据处理 | 新增 Page Patterns 与 State and Content Rules，要求安全文本、真实成功确认、失败恢复、防重复提交、危险操作确认；不修改上游源码，不声称业务已实现 |
| P2 | Accessibility 和 Known Gaps 写“无自动 axe CI”，实际存在 workflow 和 16 路径 smoke test；无 Playwright 时会 skip [S7] | 错报现有质量保障，也可能把退出码零误判为测试通过 | 修正为实际触发范围、严重度门禁和 skip 条件；静态检查工作流/脚本，本轮未执行 axe |
| P2 | Interaction Contracts 缺 SidebarSearch、Fullscreen、持久化和 initialize/teardown；before/after 事件未区分 [S6] | 重复监听、错误状态同步、SPA 导航后失效 | 补配置位置、默认值、可取消事件、事件目标、动画时序及 Turbo/框架生命周期；源码核对，重复挂载待运行验证 |
| P2 | 资源和许可边界不足；上游 integrations.mdx 的“全部 MIT”不能照抄：Tom Select 是 Apache-2.0，Quill 是 BSD-3-Clause，字体包是 OFL-1.1 [S14] | 错误依赖假设、样式重复加载及再分发风险 | 新增固定版本资源/许可表、Select2 纯 CSS 边界、图片归属与待核实项；查精确版本包元数据，不把元数据检查称为法律审查 |
| P2 | 原组件和状态覆盖缺标签页/抽屉/分页、高级表单、Ribbon/social；Toast demo 的 data-bs-toggle 依赖页面 listener [S10] [S13] | 组件组合失真，部分按钮无法实际触发 | 补继承行为、真实初始化和销毁责任；Progress 使用 Bootstrap 5.3 外层 progressbar 语义；核对版本实现与 demo |
| P2 | 对“每个 demo 一个主标题”等无障碍能力概括过强；Invoice 有两个 h1，Chat <=768px 隐藏联系人却无替代入口，拖放无键盘替代 [S7] [S9] | 直接复制保留实际可访问性缺口 | 区分框架能力与页面义务，提出具体修正/验收项；未做屏幕阅读器、对比度或移动端操作验证 |
| P2 | README 原“旧版本不原地覆盖”不适合本次同版本维护；缺 commit 级来源与当前版/首次 Release 下载区别 | 用户可能下载旧附件并误认为已获得补充版 | 更新双语版本约定、维护入口、固定 SHA 使用和历史链接；版本、标签和旧附件保持不变 |

## 覆盖矩阵

“完整”只表示本轮指定范围的静态设计规则及边界可用，不表示完整 API 覆盖或 UI 验收通过。“部分”说明仍需应用选择或实际运行证据。

| 模块 | 审计前 | 本轮后 | 依据与剩余边界 |
| --- | --- | --- | --- |
| 目的、非目标、读取方法与 Agent 提示词 | 部分 | 完整 | 双语 README、Overview、Prompt；保留真实业务合同 |
| 版本/锁定依赖/来源优先级 | 部分 | 完整 | package/lock、固定上游 SHA、Sources and Verification |
| 颜色、字体、间距、圆角、边框、阴影、层级、动效 | 部分 | 完整 | SCSS 与编译 CSS；组件特定值不可当全局令牌 |
| 侧导航、顶导航、固定/mini/compact/RTL 壳 | 部分 | 完整 | Layout 和真实 layout/*.astro；实际滚动/RTL 仍待验证 |
| SidebarSearch、全屏、持久化、插件生命周期 | 缺失/部分 | 完整 | TypeScript 配置、事件、生命周期；不等于路由框架 |
| light/dark/auto、浮层与第三方主题 | 部分 | 部分 | Theme 片段及继承规则已补；第三方组件逐态显示待验证 |
| 基础组件、表单状态、标签页、抽屉、反馈 | 部分 | 完整 | Bootstrap 5.3.8 与 UI/general、forms/elements |
| 高级表单、编辑器、数据表 | 缺失 | 部分 | 已补真实配置和状态；不包含完整插件 API/真实接口 |
| Ribbon、社交、指标、Timeline、Direct Chat | 部分 | 完整 | 对应 SCSS、widgets 与 UI 页面 |
| 业务页面组合、认证、详情/编辑、异常 | 部分 | 部分 | 16 组页面模式；真实保存、搜索、上传、计费等仍由应用负责 |
| 加载/空/失败/成功、批量、重复提交、危险操作 | 部分 | 完整 | 推荐规则与恢复路径明确；非框架自动功能 |
| 窄屏表单、表格溢出、长文本、中英文内容 | 部分 | 部分 | 已给规则与已知 Chat 缺口；页面级选择/运行待验证 |
| 键盘、焦点、播报、减弱动效、自动 CI | 部分且有误 | 部分 | 实现能力、上游缺口、16 页 axe 门禁已区分；无 WCAG 合规结论 |
| 图标/字体/图片、依赖加载与许可 | 部分 | 部分 | 精确包版本/元数据已核对；逐图权利、全依赖审查待验证 |
| 双语、版本索引、固定来源与历史追溯 | 部分 | 完整 | 同 4.3.1 维护，旧标签/Release/附件不变 |
| 路由标签缓存、权限路由、通用混合导航控制器 | 不适用 | 不适用 | 上游没有这些业务基础设施；不能为凑覆盖而新增 |

未发现需改变的基础规则：Bootstrap 语义主色与五个常用断点、Source Sans 3 基线、250px 默认侧栏、Card/Small Box/Info Box 的基本结构、AdminLTE 3 与 4 类名边界均有版本源码支持；本轮保留并补充作用域，而不是替换设计语言。

## 升级文件与章节

| 文件 | 优先级与具体改动 |
| --- | --- |
| `versions\4.3.1\DESIGN.md` | P1：令牌、主题、壳、组件/页面模式与业务状态；P2：插件事件、生命周期、资源/许可、可访问性和固定来源 |
| `versions\4.3.1\DESIGN.zh-CN.md` | 与英文相同规则、值、表格、代码逻辑和未验证边界；同步 Prompt/Do/Iteration/Known Gaps |
| `README.md`、`README.en-US.md` | 当前维护版入口、同版本更新约定、精确上游来源、审计入口和 commit 固定下载说明 |
| `AUDIT.md` | 本记录：问题、证据、覆盖、处理、版本和验收边界 |

## 版本与发布策略

本轮仅完善 `4.3.1`，不创建 `4.3.1-r1`、`4.3.1.1` 或其他修订号。文档变更以新的普通 Git 提交推送 `main`，保留旧提交作为祖先；不重写分支历史。

原标签 `v4.3.1` 仍指向 `5edbd128e519e0319df5f4372277f192be60a300`。原 Release 和附件不覆盖、不更名、不重新上传。当前维护版从 README 的 main 链接读取；需要复现时固定所选完整 commit SHA。这样保持用户要求的原版本号，同时不破坏历史下载内容。

发布核验基线：Release ID `370417751`；英文附件 ID `514095784`，SHA256 `d293dcf7d4074715b9c78857867bfe89ba5a5543bbe38d745e8001e4cffbd7d8`；中文附件 ID `514095786`，SHA256 `872eb5491b9d5b3be9135aba0a6089e6700e4e6deae3214194485d728948d439`。GitHub 仓库中英文描述保留。

## 验收标准与实际范围

| 检查层 | 验收标准 | 本轮状态 |
| --- | --- | --- |
| 文档 | UTF-8 严格解码；YAML 实际解析；令牌引用可解析；双语章节/数值/源链接/代码规则一致；Markdown 表格与相对链接有效 | 5 个文档通过 UTF-8、YAML/Markdown 解析、链接检查及 GitHub Markdown API 渲染；双语令牌、56 个标题层级、7 张表结构、14 组来源及主题片段一致；自然语言规则另行人工对照 |
| 源码 | 官方固定提交与本地引用文件内容匹配；核对 SCSS/CSS、TypeScript、Astro、锁文件与实际 CI；固定包版本/许可 | 264 个文件 Git blob SHA 精确一致，无需换行归一化；含 src/scss、src/ts、src/html 与选定包/锁/CI/编译产物。14 个精确版本 npm 元数据已核对 |
| 片段逻辑 | stored light/dark/auto/非法/缺失、markup、OS、off、存储异常组合；解析标记及 ColorMode 后续行为一致 | 200 组隔离测试通过；运行文档片段与该版本编译出的 ColorMode，验证初始化、OS 变化、setTheme 事件/持久化和 off 边界；不是首屏 UI 验收 |
| 发布 | main 指向本轮提交，预期五文件内容匹配，本地干净；旧标签与附件身份/摘要不变 | 作为发布后回读条件；具体提交和结果由本轮交付说明提供 |
| 必要运行验收 | 按选中页面测试 320/576/768/992/1200/1400px、light/dark/auto、长表单/表格、浮层、键盘/焦点、缩放、减弱动效、RTL；第三方暗色与重复挂载；真实提交/失败恢复 | 本轮未运行前端、未装依赖、未执行浏览器/axe/NVDA/后端流程，全部待消费项目验证 |

运行验收需要真实页面与业务上下文。未来执行 `test-a11y` 时必须看到每条页面结果，且没有 skipping；即使 serious/critical 为零，也不能证明动态状态、键盘流程或全站合规。静态文档检查不能替代这些验收。

## 固定证据索引

各问题的 [S1] 至 [S14] 对应规范的 Sources and Verification。以下入口固定到同一上游提交；相关文件路径见规范索引，许可证的精确包链接见 Assets and Dependency Boundaries。

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
