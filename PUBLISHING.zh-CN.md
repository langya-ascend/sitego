# GitHub 公开发布规范

[English](PUBLISHING.md)

文档作者：vigo。更新日期：2026-10-29。范围：独立维护的文档；应用公开仍须通过下方发布门槛。

- README 素材放在 `assets/`，保留来源和许可说明；`preview/` 仅用于本地评阅，`profile/` 属于个人主页仓库，均不进入本仓库。项目所有者提供的截图展示阿福界面，不代表获准公开其 worker 或宣称公开版支持阿福。

## 仓库分开维护

Codeup 是项目在阿里云上的私有开发托管平台，GitHub 承载独立维护的公开文档版。

- GitHub 版 README、路线图、许可证、标签与公开变更记录独立维护。
- Codeup 可保存经核验的文档快照，并维护自己的中英文开发说明；不改变其完整私有功能范围、源码、包许可、发布配置或验收门槛。文档提交进入已授权的开发分支，不将未验收的应用改动合并到主干。
- 使用独立公开准备目录及明确审核的文件白名单，不将私有仓库及其历史整体镜像推送到 GitHub。
- 后续源码导出采用新的公开历史或经验证的过滤历史，核对所有待推送分支、标签与产物，不能只检查最新目录。
- 当前仓库仅包含文档和经审核的视觉素材；文档提交或推送不等于应用源码或镜像发布。

## 文档发布

项目所有者于 2026-10-29 授权向 Codeup 和 GitHub 分别提交文档，范围仅含中英文 README、路线图、许可草案、发布规范和经审核的视觉素材，不包含应用源码、包、镜像、私有历史或阿福 worker。

每次文档推送前，核对完整文件清单、相对链接、双语一致性、进度声明、图片来源及敏感信息与私有环境数据。确认远端提交后再记录交付；下方应用发布清单仍独立执行。

## 排除阿福

项目所有者另行明确同意前，排除阿福 worker、平台实现、协议与解析材料、夹具、私有样本、生成代码、source map、包、镜像层以及包含这些内容的历史。共享文件也要检查是否嵌入相关实现，不能只按文件名搜索。

公开版不将阿福展示为可启用的平台，也不添加 `afu` 或阿福搜索标签。路线图可以说明该 worker 暂不公开、等待项目所有者同意。对一般 GitHub 发布、新版本或其他平台的批准，不能覆盖此限制。

## 搜索与展示

仓库简介候选：

> Site-to-API for Doubao and Yuanbao, with account scheduling and source evidence for GEO. 豆包/元宝站点转 API，面向 GEO 检测。Preparing for release; commercial use requires written permission.

待对应公开范围准备好后再应用以下 Topics：

```text
sitego doubao yuanbao site-to-api web-to-api browser-automation
geo generative-engine-optimization ai-search source-citation
account-scheduling self-hosted typescript docker
source-available noncommercial
```

GitHub Topics 使用小写字母、数字与连字符，每个不超过 50 字符，总计不超过 20 个；上述候选共 16 个。中文关键词自然写进简介与中文 README。私有仓库的 Topic 名称也公开，不放内部标识。

不使用无关热门标签、与许可矛盾的 `open-source` 标签、未支持的兼容性声明、虚构性能或刷 Star。通过可复现安装、明确限制、公开示例、问题回复和有效版本更新提高可发现性，不承诺 Star 数量或搜索排名。

## 应用发布检查

- [ ] 对应公开候选完成全部已约定验收。
- [ ] 审核的文件白名单排除私有代码及阿福 worker 内容，覆盖历史与产物。
- [ ] 两种语言的 README 与路线图在公开范围、验证结果、限制和版本上保持一致。
- [ ] 权利主体、授权联系方式、商用书面许可定稿及第三方声明齐备。
- [ ] 公开候选与历史完成密钥、账号数据、私有环境及未公开实现扫描。
- [ ] 独立构建与测试公开版，包含移除阿福后的正常运行验证。
- [ ] 仅使用公开文件与已发布依赖完成全新安装。
- [ ] 复核标签与简介，仅在项目所有者授权范围内执行公开发布。

## 维护节奏

公开文档采用小步、经验证的中文备注提交。README 保留简明进度，路线图维护里程碑和待办缺口。功能完成记录必须有日期与公开版本证据，发布说明区分源码发布、镜像发布、部署和业务验收。

## Tag 与版本说明

已验收的应用版本遵循 [Tag 与 Release 规范](releases/README.zh-CN.md)。正式版使用附注 Tag `vX.Y.Z`，候选版使用 `vX.Y.Z-rc.N`，每个版本对应一个双语 GitHub Release。已发布的 Tag 不移动、不覆盖。

从[中文指引](releases/RELEASE_NOTES_TEMPLATE.zh-CN.md)或[英文指引](releases/RELEASE_NOTES_TEMPLATE.md)的双语模板中任选一份准备版本说明，包含已验证改动、升级、回退与恢复步骤、已知问题、验收范围，以及真实产物的校验值和镜像摘要。纯文档更新不创建应用 Tag，也不绕过上述发布检查。

参考：[GitHub Topics](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics)、[Open Source Definition](https://opensource.org/osd)。
