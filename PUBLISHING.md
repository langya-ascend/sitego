# GitHub Publication Rules

[简体中文](PUBLISHING.zh-CN.md)

Author: vigo. Updated: 2026-10-29. Scope: independently maintained documentation; application publication remains subject to the release gates below.

- README assets live under `assets/`, with provenance and license notices. `preview/` is local review output and `profile/` belongs to the personal profile repository; neither is included in this repository. Owner-supplied screenshots showing Afu UI do not authorize publishing its worker or claiming public support.

## Repository Separation

Codeup is the project's private development host on Alibaba Cloud. GitHub hosts the separately maintained public documentation edition.

- Maintain GitHub README, roadmap, license, topics, and public changelog independently from Codeup.
- Codeup may retain a reviewed documentation snapshot and its own bilingual development READMEs. This does not change its full private feature scope, source, package license, release configuration, or acceptance gates. Documentation commits go to its authorized development branch without merging unaccepted application changes into the trunk.
- Use a separate public preparation workspace and an explicit reviewed file allowlist. Never mirror/push the entire private repository or its history to GitHub.
- Future source exports need a clean public history or a verified filtered history. Check every pushed branch/tag and artifact, not just the latest directory contents.
- This repository contains documentation and reviewed visual assets only. A documentation commit or push is not an application source or image release.

## Documentation Publication

The owner authorized separate documentation submissions to Codeup and GitHub on October 29, 2026. That authorization covers the bilingual READMEs, roadmap, draft license, publication rules, and reviewed visual assets only. It does not authorize application source, packages, images, private history, or Afu's worker.

Before each documentation push, verify the complete file list, relative links, language parity, progress claims, image provenance, and absence of secrets or private environment data. Record delivery only after the remote commit is verified. The application release checklist below remains separate.

## Afu Exclusion

Until the owner explicitly approves publication, exclude Afu's worker, provider implementation, protocol/parser material, fixtures, private samples, generated code, source maps, packages, image layers, and histories containing them. Review shared files for embedded implementation; a filename search alone is insufficient.

Do not expose Afu as an enabled public provider or add `afu`/阿福 discovery labels. A roadmap may state that the worker is withheld pending owner approval. Approval for general GitHub publication, a new release, or another provider does not override this restriction.

## Discovery Metadata

Proposed description:

> Site-to-API for Doubao and Yuanbao, with account scheduling and source evidence for GEO. 豆包/元宝站点转 API，面向 GEO 检测。Preparing for release; commercial use requires written permission.

Proposed topics, to apply only when the corresponding public scope is ready:

```text
sitego doubao yuanbao site-to-api web-to-api browser-automation
geo generative-engine-optimization ai-search source-citation
account-scheduling self-hosted typescript docker
source-available noncommercial
```

GitHub topics use lowercase letters, numbers and hyphens, with at most 50 characters per topic and 20 topics total. The list above contains 16 topics. Chinese terms belong naturally in the description and Chinese README. Topic names are public even on private repositories; do not place private identifiers in them.

Do not use unrelated trending tags, an `open-source` label inconsistent with the license, unsupported compatibility claims, fabricated benchmarks, or purchased/artificial Stars. Improve discovery through reproducible installation, clear limitations, public examples, issue responses, and useful releases. No Star count or search ranking is promised.

## Application Release Checklist

- [ ] All agreed acceptance gates pass for the exact public candidate.
- [ ] The reviewed file allowlist excludes private code and Afu worker content, including history and artifacts.
- [ ] Both READMEs and roadmaps agree on public scope, checked behavior, limitations, and version.
- [ ] Rights-holder identity, authorization contact, final commercial permission terms, and third-party notices are complete.
- [ ] Scan the public candidate and its history for secrets, account data, private environments, and unpublished implementation.
- [ ] Build and test the public edition independently, including operation with Afu omitted.
- [ ] Verify a fresh install using only public files and published dependencies.
- [ ] Review topics/description and publish only within the owner's authorized scope.

## Maintenance Rhythm

Use small, verified Chinese-described commits for public documentation. Keep README progress concise; put milestones and known gaps in the roadmap. Each feature completion needs dated public-version evidence. Release notes should distinguish source publication, image publication, deployment, and business acceptance.

References: [GitHub topics](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics), [Open Source Definition](https://opensource.org/osd).
