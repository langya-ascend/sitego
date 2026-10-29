# README 视觉素材说明

[English](README.md)

文档作者：vigo。更新日期：2026-10-29。

## 产品截图

`screenshots/` 中的两张图片由项目所有者为本次 README 提供，原样复制，不修改像素。可见内容包括完整开发版界面、阿福入口、示例账号别名、时间、状态和调度额度。图注明确区分截图与公开版范围、验收证据及安全频率。

可见区域未发现密码、Token、邮箱、IP、浏览器资料路径或私有配置值。更换图片及正式发布前仍须复核。没有导出浏览器会话或应用源码。

## 品牌与平台标志

字标保留现有绿色图形和蓝色 GO，使用与后台相同、来自 `@lucide/svelte` 版本 `1.29.0` 的 Lucide Waypoints 图标。随附[许可证](licenses/lucide-LICENSE.txt)已与实际安装包逐字节核对一致，包含原有 2026 版权行，未改写原文。字标排版、静态徽章和流程图为本文档版本整理。

豆包与元宝图片原样沿用后台站点图标，已有来源记录指向对应平台官网。仅用于识别平台，不表示官方背书、合作关系或商标所有权。

## 发布边界

徽章只说明准备状态、架构、语言和许可草案，不是实时构建、测试、Release 或人气数据。品牌和流程图提供亮暗版本。

本地 HTML 预览、检查截图与生成记录不进入本仓库，阅读本文档不需要预览目录。截图可以展示阿福界面，但未包含阿福 worker 源码、协议材料、夹具或产物。

早期的精简流程图保留为轻量预览的可选素材：[英文亮色](diagrams/workflow-en-light.svg)、[英文暗色](diagrams/workflow-en-dark.svg)、[中文亮色](diagrams/workflow-zh-light.svg)、[中文暗色](diagrams/workflow-zh-dark.svg)。README 使用下方更详细的 PNG 图。

## 架构与功能蓝图

新增三张中英双语 PNG：系统架构、单次任务流程和功能蓝图。采用统一的轻手绘技术蓝图风格，由 imagegen-api MCP 根据人工整理的公开概念生成，逐张核对文字、连接关系和发布边界。图中不包含阿福实现、生产地址、凭据或私有代码；流程图不是运行证据，功能蓝图也不是公开验收结论。原始截图未修改。

每张图可点击查看原尺寸；README 相邻正文提供可搜索的说明。若架构或状态变化，先更新正文和路线图，再同步修订图片。

## 原件完整性与文档检查

已核验原件的 SHA-256：

| 文件 | SHA-256 |
| --- | --- |
| `screenshots/channels-accounts.png` | `2632e5edfc5fa5244758933f1d64984595db110921a90de6ff51fac558ddfe82` |
| `screenshots/account-detail.png` | `507a4bf92a6e6962fd5cd6c0fe073e555ab54a408c5832befc8497641c443ff8` |
| `diagrams/system-architecture.png` | `e30307f10d9812dfd885ec4bdaedc605e0640e59d8778b6fda7637864d6aae7e` |
| `diagrams/request-lifecycle.png` | `991023e072aefed6be121045b6d66d2d482ffbbfa883eb058358ffbb436a16a3` |
| `diagrams/capability-blueprint.png` | `47766334f19d471aa08b22de9e51054dd6360b26b9af2f01670fbfffb50bb1ff` |
| `providers/doubao.png` | `bf8e41bcc864c00099a98080825ea42aba7cf481303dad3312f44a5da68c3f3b` |
| `providers/yuanbao.png` | `43bdb989125d45e484520a98a50c6def611a0242d0f381c2ec6a9092c7b264d8` |
| `licenses/lucide-LICENSE.txt` | `b495047bd93a9b06913511076f504daba17d5bbeb3e0650f3bb53a4220329c57` |

2026-10-29 的文档检查覆盖完整发布白名单、相对链接与锚点、中英文勾选数、敏感文本扫描及原图哈希。两种语言的 README 均检查了 1440px、390px、360px 宽度及桌面暗色模式，包含图片加载与语言切换。这些属于文档检查，不是应用验收。截图元数据已另行核查，仅保留非敏感的尺寸、分辨率及颜色信息。
