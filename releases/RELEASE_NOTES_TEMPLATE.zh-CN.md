# SiteGO {{VERSION}} · {{RELEASE_THEME}}

<!-- 作者：vigo；模板日期：2026-10-29。本文件是一份完整双语模板，不是已发布版本。从本文件或英文指引版中任选一份起草，不要拼接。VERSION 填包含 v 的完整 Tag 名。替换全部占位符，保持双语一致，删除不适用章节并完成发布检查。 -->

> [!IMPORTANT]
> {{UPGRADE_OR_COMPATIBILITY_NOTICE_ZH}}
>
> {{UPGRADE_OR_COMPATIBILITY_NOTICE_EN}}

## 中文

### 新增与改进

- {{ADDITIONS_AND_IMPROVEMENTS_ZH}}

### 修复

- {{FIXES_WITH_TRIGGER_BEFORE_AND_AFTER_ZH}}

### 升级与兼容性

- 适用版本：{{SUPPORTED_UPGRADE_PATH}}
- 配置与数据变化：{{CONFIG_AND_MIGRATION_ZH}}
- 升级步骤：{{UPGRADE_STEPS_ZH}}
- 回退与恢复方式及限制：{{ROLLBACK_AND_RECOVERY_ZH}}

### 已知问题与验证范围

- 已验证：{{EXACT_COMMIT_ENVIRONMENT_AND_CHECKS_ZH}}
- 尚未覆盖：{{UNVERIFIED_SCOPE_ZH}}
- 已知问题：{{KNOWN_ISSUES_AND_WORKAROUNDS_ZH}}

### 发布与验收状态

各项分别填写实际状态、日期与证据；未执行的项目如实标注，不用产物发布代替部署或业务验收。

- 源码发布：{{SOURCE_PUBLICATION_STATUS_DATE_EVIDENCE_ZH}}
- 容器镜像发布：{{IMAGE_PUBLICATION_STATUS_DATE_EVIDENCE_ZH}}
- 部署：{{DEPLOYMENT_STATUS_DATE_EVIDENCE_ZH}}
- 业务验收：{{BUSINESS_ACCEPTANCE_STATUS_DATE_EVIDENCE_ZH}}

## English

### Additions and Improvements

- {{ADDITIONS_AND_IMPROVEMENTS_EN}}

### Fixes

- {{FIXES_WITH_TRIGGER_BEFORE_AND_AFTER_EN}}

### Upgrade and Compatibility

- Supported versions: {{SUPPORTED_UPGRADE_PATH}}
- Configuration and data changes: {{CONFIG_AND_MIGRATION_EN}}
- Upgrade steps: {{UPGRADE_STEPS_EN}}
- Rollback and recovery steps and limits: {{ROLLBACK_AND_RECOVERY_EN}}

### Known Issues and Verification Scope

- Verified: {{EXACT_COMMIT_ENVIRONMENT_AND_CHECKS_EN}}
- Not yet covered: {{UNVERIFIED_SCOPE_EN}}
- Known issues: {{KNOWN_ISSUES_AND_WORKAROUNDS_EN}}

### Publication and Acceptance Status

Record each actual status, date, and evidence separately. Mark unperformed steps explicitly; artifact publication does not establish deployment or business acceptance.

- Source publication: {{SOURCE_PUBLICATION_STATUS_DATE_EVIDENCE_EN}}
- Container image publication: {{IMAGE_PUBLICATION_STATUS_DATE_EVIDENCE_EN}}
- Deployment: {{DEPLOYMENT_STATUS_DATE_EVIDENCE_EN}}
- Business acceptance: {{BUSINESS_ACCEPTANCE_STATUS_DATE_EVIDENCE_EN}}

## What's Changed

{{ACTUAL_PUBLIC_COMMITS_AND_PULL_REQUESTS}}

## New Contributors

{{ACTUAL_FIRST_TIME_CONTRIBUTORS_OR_REMOVE_SECTION}}

**Full Changelog**: {{PREVIOUS_PUBLIC_TAG_TO_CURRENT_TAG_COMPARISON_OR_INITIAL_RELEASE}}

## Assets

<!-- 与英文指引模板同步维护双语正文；两份仅指引注释语言不同。RELEASE_THEME 包含中英主题。每个实际交付文件或镜像单独一行，sitego-control 与 sitego-worker 分别列行；末列按类型填写文件 SHA-256 或镜像不可变摘要。 -->

| 文件或镜像 / File or image | 版本与平台 / Version and platform | SHA-256 / digest |
| --- | --- | --- |
| {{VERIFIED_DOWNLOAD_OR_IMAGE}} | {{VERSION_AND_ARCHITECTURE}} | {{VERIFIED_DIGEST}} |

{{VERIFIED_DOWNLOAD_LINKS_AND_LICENSE_REFERENCE}}

<!-- 发布检查：核对附注 Tag 指向已验收提交；rc 勾选 Pre-release，并核对正式版与 Latest 设置；核对许可与公开范围、下载文件、校验值和镜像摘要；确保没有模板占位符或重复章节。发布后回读 Tag、Release 设置、正文和产物，在版本记录中保存核验人、时间与证据。 -->
