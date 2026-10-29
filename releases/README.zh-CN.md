# SiteGO Tag 与 Release 规范

[English](README.md)

作者：vigo。日期：2026-10-29。范围：按项目所有者要求记录的后续发布规则；本文件不创建 Tag 或发布应用。

## 版本与提交

正式版本采用 `vX.Y.Z`，候选版本采用 `vX.Y.Z-rc.N`，例如 `v0.1.0-rc.1`。示例不是已发布版本。

每个对外版本对应一个明确的已验收提交、一个附注 Tag 和一个 GitHub Release。附注说明优先使用中文，署名 vigo 或 langya，日期采用实际创建时间。已发布 Tag 不移动、不覆盖；代码或产物修复使用新版本。

从 `v1.0.0` 起，不兼容变更递增主版本，兼容新增递增次版本，兼容修复递增补丁版本。`v0` 开发阶段的不兼容变更使用新的次版本并明确说明。每个新候选递增 `rc.N`；验收通过后，在已验收提交上新建正式 Tag，保留全部候选 Tag。

Codeup 与 GitHub 独立维护提交和发布记录；不能把 Codeup 私有历史直接作为 GitHub Tag 的来源。公开提交、所有可下载归档、安装包和镜像中继续排除阿福 worker，直至另获明确授权。

## Release 页面顺序

1. 版本号与本次主题。
2. 重要提示 / Important：升级必读、兼容变化或影响范围；无实际提示时省略。
3. 中文说明：新增、改进、修复、升级方式、已知问题及验证范围。
4. English：与中文版逐项一致。
5. What's Changed：该 Tag 范围内真实的公开提交或 PR；不虚构编号。
6. New Contributors：仅在确有首次贡献者时列出。
7. Full Changelog：上一公开版本到本次版本的对比；首版明确写“首次公开版本”。
8. Assets：实际交付的文件、校验值和对应镜像摘要。

从[中文指引模板](RELEASE_NOTES_TEMPLATE.zh-CN.md)或[英文指引模板](RELEASE_NOTES_TEMPLATE.md)中任选一份起草。每份已包含完整中英文段落，以及一套共用的变更、贡献者、版本对比和产物章节，不要将两份文件直接拼接。替换全部占位符，保持双语一致，删除不适用章节；`VERSION` 填写包含 `v` 前缀的完整 Tag 名。发布前检查没有残留的 `{{...}}` 占位符，各章节仅出现一次。自动生成的提交清单是补充材料，不能替代面向用户的说明。

## 产物与验收

- `sitego-control` 与 `sitego-worker` 关联到同一发布版本，并分别记录各自构建证据、支持架构和镜像摘要。
- 分别记录源码发布、容器镜像发布、部署和业务验收的状态、日期与证据。产物已发布不代表已部署或通过业务验收。
- 仅列出真正提供并验证过的包、镜像和下载链接。不为模仿示例项目列出不存在的平台安装包。
- 提供下载文件的 SHA-256 清单；注明镜像不可变摘要，不能只依赖可变的 `latest` 标签。
- 未通过正式发布门槛的候选版本标记为 Pre-release，不列为正式 Latest。
- 发布前先准备 Draft、双语说明和全部产物；发布后回读 Tag 指向、Release 内容与下载文件。
- 有可验证签名时如实展示签名状态；`Verified` 是签名验证状态，不代表功能测试或业务验收通过。

当前公开仓库仅含文档，不因此创建应用版本 Tag。商业许可最终条款、公开源码、安装和功能验收仍按各自门槛推进。

## 维护记录

每次版本保存发布说明、精确提交、Tag、制品摘要、验证范围、已知限制、升级、回退与恢复方式。Release Notes 与版本记录同步更新，不把未完成规划写成已交付功能。

参考：[GitHub Release 管理](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository)、[签名验证](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification)。
