# SiteGO {{VERSION}} · {{RELEASE_THEME}}

<!-- Author: vigo. Template date: 2026-10-29. This is one complete bilingual template, not a published release. Start from this file OR the Chinese-guided equivalent, never concatenate them. VERSION is the exact tag name including v. Fill every placeholder, keep both languages aligned, remove inapplicable sections and complete the preflight check. -->

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

<!-- Keep the bilingual body synchronized with the Chinese-guided template; only the guidance comments differ. Include both languages in RELEASE_THEME. Add one row per delivered file/image and separate rows for sitego-control and sitego-worker. Use the last column for the file SHA-256 or immutable image digest as applicable. -->

| 文件或镜像 / File or image | 版本与平台 / Version and platform | SHA-256 / digest |
| --- | --- | --- |
| {{VERIFIED_DOWNLOAD_OR_IMAGE}} | {{VERSION_AND_ARCHITECTURE}} | {{VERIFIED_DIGEST}} |

{{VERIFIED_DOWNLOAD_LINKS_AND_LICENSE_REFERENCE}}

<!-- Preflight: verify an annotated tag at the accepted commit; select Pre-release for rc and verify the stable/latest setting; check license and public scope, downloads, checksums, and image digests; ensure no template placeholders or duplicate sections remain. After publication, read back the tag, release settings, text, and artifacts; record verifier, time, and evidence in the release record. -->
