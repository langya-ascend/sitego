<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/brand/sitego-dark.svg">
    <img src="assets/brand/sitego-light.svg" width="340" alt="SiteGO">
  </picture>
</p>

<h3 align="center">Website Q&A. One API.</h3>

<p align="center">
  Designed to bring Doubao and Yuanbao into your GEO workflows.<br>
  Managed accounts, traceable answers, and a clear view of every task.
</p>

<p align="center">
  <img src="assets/badges/status-en.svg" height="26" alt="Stage: In preparation">
  <img src="assets/badges/architecture-en.svg" height="26" alt="Services: Control + Worker">
  <img src="assets/badges/languages-en.svg" height="26" alt="UI: 中文 / EN">
  <a href="LICENSE-DRAFT.md"><img src="assets/badges/license-en.svg" height="26" alt="License: NC draft"></a>
</p>

<p align="center"><b>English</b> · <a href="README.zh-CN.md">简体中文</a></p>

<p align="center">
  <a href="#product-preview">Product Preview</a> · <a href="#capabilities">Capabilities</a> · <a href="#capability-blueprint">Blueprint</a> · <a href="#progress">Progress</a> · <a href="#architecture">Architecture</a> ·
  <a href="ROADMAP.md">Roadmap</a> · <a href="releases/README.md">Release Policy</a> · <a href="#license-and-commercial-use">License</a>
</p>

---

SiteGO connects website Q&A to **GEO (Generative Engine Optimization) evaluation, source collection, and business integrations**. Submit an independent question, track its execution, and collect the answer and its sources through a shared API and operations console.

> **Documentation preview · Application release in preparation** · Updated October 29, 2026
>
> This repository currently contains product documentation, screenshots, diagrams, a roadmap, draft licensing, publication rules, and brand assets. Application source, installation packages, and public images have not been released. The first public application edition targets Doubao and Yuanbao. Afu's worker remains private pending separate owner approval.

## Product Preview

### Channels And Managed Accounts

See provider availability, account state, queue counts, and operator actions in one workspace.

<p align="center">
  <a href="assets/screenshots/channels-accounts.png"><img src="assets/screenshots/channels-accounts.png" width="1000" alt="SiteGO development console: channels, managed accounts, queue counts, and operator actions"></a>
</p>

### Account Inspection And Scheduling Limits

Inspect service status, account budgets, and recent operations before returning an account to the scheduler.

<p align="center">
  <a href="assets/screenshots/account-detail.png"><img src="assets/screenshots/account-detail.png" width="1000" alt="SiteGO development console: account detail, request budgets, inspection history, and account actions"></a>
</p>

<sub>Owner-supplied screenshots of the complete development edition, including Afu UI. They do not establish public feature availability or provider acceptance. Afu's worker is excluded from the public scope. Displayed budgets are example configuration, not provider-approved safe rates. Select an image to inspect the original.</sub>

## Capabilities

| Capability | What it is designed to do |
| --- | --- |
| **One question, one task** | Handle independent requests and reclaim task pages after completion while retaining operator pages. |
| **Managed account scheduling** | Coordinate a durable queue, account/platform budgets, and mutual exclusion for the same logical account. |
| **Answers with evidence** | Keep answer text, candidate sources, direct citations, and excerpts distinct; show missing or partial evidence explicitly. |
| **Recovery without blind resubmission** | Persist idempotency and execution records. An unknown submitted outcome must not trigger another question automatically. |
| **An operations console** | Review accounts, tasks, policies, and audits in Chinese or English, with light and dark themes. |
| **Operator intervention** | Use authenticated remote desktop access for manual login or verification; takeover blocks task submissions. |

These describe development capabilities and the planned public scope. Public-edition acceptance is tracked [below](#progress).

## Capability Blueprint

Capabilities are organized into API, scheduling, execution, and operations layers. Solid outlines identify development foundations; dashed outlines distinguish acceptance work and later plans. Diagram status does not establish public delivery.

<p align="center">
  <a href="assets/diagrams/capability-blueprint.png"><img src="assets/diagrams/capability-blueprint.png" width="1000" alt="SiteGO capability blueprint: single-question APIs, scheduling, evidence, operations, and planned capabilities; bilingual labels"></a>
</p>

Real GEO/gateway integration, alerting, and capacity observability remain future work. See the [roadmap](ROADMAP.md).

## Provider Scope

| Provider | Public-edition plan | Current boundary |
| --- | --- | --- |
| <img src="assets/providers/doubao.png" width="24" height="24" alt="Doubao"> **Doubao / 豆包** | First release candidate | Local single-question evidence exists; complete public acceptance is pending. |
| <img src="assets/providers/yuanbao.png" width="24" height="24" alt="Yuanbao"> **Yuanbao / 元宝** | First release candidate | Local single-question evidence exists; supported modes must be verified explicitly. |

Afu's worker is excluded from public source, packages, image layers, and Git history until the owner explicitly approves it. It is not a disabled feature shipped inside a public build.

Request budgets are operational safeguards, not guaranteed safe frequencies. SiteGO does not promise to bypass provider verification or keep third-party websites permanently available.

## Progress

**Development progress and public delivery are separate.** The following is the recorded position on October 29, 2026.

| Area | Development evidence | Public-edition acceptance |
| --- | --- | --- |
| Doubao and Yuanbao | Local single-question API results and persisted replay. | Export, supported-mode coverage, and complete acceptance pending. |
| Scheduler and lifecycle | Automated coverage of queues, account exclusion, idempotency, and task-page cleanup. | Sustained-load and recovery acceptance pending. |
| Operations console | Account, task, policy, audit, bilingual UI, and operator workflows. | Public configuration and end-to-end acceptance pending. |
| Remote desktop and images | Local synthetic browser checks and ARM64 Linux runtime evidence. | Target builds, packaging, and installation acceptance pending. |
| GEO and API gateways | Compatibility requirements and local contracts. | Real integration and citation-persistence acceptance pending. |

The [public roadmap](ROADMAP.md) tracks milestones, release gates, and remaining work. A feature is not marked released solely because it exists in the private edition.

## Architecture

One project, two image types: the admin console ships with control; workers are deployed for managed accounts. This is a design view, not a live production topology.

<p align="center">
  <a href="assets/diagrams/system-architecture.png"><img src="assets/diagrams/system-architecture.png" width="1000" alt="SiteGO system architecture: API callers and operators, sitego-control, durable state, and Doubao/Yuanbao workers"></a>
</p>

| Layer | Responsibility and boundary |
| --- | --- |
| Entry points | Business callers submit questions through APIs; operators inspect and manage accounts through the console. |
| `sitego-control` | Business/admin APIs, durable scheduling, tasks, and audits. The admin console belongs to this image. |
| Durable state | Persists queues, tasks, idempotency, and audits. SQLite is not a third externally exposed service. |
| `sitego-worker` | Isolates each logical account's browser environment, runs provider adapters, and keeps an execution journal. Multiple instances use one image type. |
| Operator takeover | Authenticated console access opens controlled remote desktop; takeover blocks dispatch and submission. |

Workers sharing a logical account share exclusion and budgets. More containers do not automatically increase platform allowances. GitHub publication history/materials and Codeup development remain independently maintained.

### A Single Task From Request To Result

<p align="center">
  <a href="assets/diagrams/request-lifecycle.png"><img src="assets/diagrams/request-lifecycle.png" width="1000" alt="SiteGO request lifecycle: request, queue, submit, verify, close task page, and publish result; exceptions retain protection"></a>
</p>

1. Receive an independent question and check identity/idempotency. Replay an eligible original result without asking again.
2. Queue durably; check account exclusion, platform budgets, and cooldown before assigning a worker.
3. Persist the submission boundary before sending. Never automatically resubmit a question whose submitted outcome is unknown.
4. Collect and verify answer text and sources, then stage the validated result.
5. Confirm this task's page is closed while preserving the operator page. Cleanup failure retains protection.
6. Publish completion and begin cooldown. People handle login or official verification; this does not automatically clear unknown-task protection.

## Near-Term Roadmap

Baseline: **October 29, 2026**. Checked items describe recorded development/documentation outcomes, not public-edition acceptance.

- [x] Control/Worker architecture and separate publication materials.
- [x] Local single-question APIs and result-replay foundations for Doubao and Yuanbao.
- [x] Local checks for durable scheduling, same-account exclusion, and task-page cleanup.
- [x] Bilingual console, controlled remote desktop, and bilingual product documentation.
- [ ] **Early November:** prepare a public candidate without Afu and finalize licensing/support scope.
- [ ] **Late November:** complete candidate fault, fixed-load, and resource acceptance.
- [ ] **Late November to mid-December:** complete GEO/gateway integration, target installation, and rollback rehearsal.
- [ ] **Mid-to-late December:** prepare initial source/image publication only after every agreed gate passes.

Dates are planning windows and will move with acceptance results. The [full roadmap](ROADMAP.md) contains individual checklists, exit conditions, and later candidates.

## Getting Started

The first verified public release will include installation instructions, configuration examples, supported image digests, and a reproducible acceptance scope. **There is no public application package or image to install yet.**

For now, use the product preview, progress table, and roadmap to assess whether SiteGO matches your workflow.

Future accepted versions will use annotated **tags and GitHub Releases**, with Chinese and English notes covering changes, upgrades, known limitations, and verified artifacts. Read the [release policy and templates](releases/README.md). This documentation preview is not an application release.

## License And Commercial Use

> **Commercial use requires the copyright holder's prior written authorization.**

The planned model is **source-available for noncommercial use**, not an MIT, Apache-2.0, or OSI-approved open-source licensing claim. The [English license draft](LICENSE-DRAFT.md) and [Chinese draft](LICENSE-DRAFT.zh-CN.md) describe the intended terms; they do not currently grant software usage rights.

The rights-holder identity, authorization contact, final terms, and third-party notices must be finalized before source publication. Third-party components and provider brands retain their own rights. See the [visual-asset notes](assets/README.md).

## Maintenance And Feedback

SiteGO is maintained by **Langya (`langya-ascend`)** for long-term use and improvement. Useful feedback includes the public version, provider, reproduction steps, and sanitized logs. Never share passwords, cookies, account profiles, or private question content.

If the project is useful to you, a Star or a reproducible issue helps others discover and improve it. Contribution workflows will accompany the first verified source release.

---

<p align="center">
  <b>SiteGO</b> · Connect websites to your workflow.<br>
  <a href="README.zh-CN.md">简体中文</a> · <a href="ROADMAP.md">Roadmap</a> · <a href="LICENSE-DRAFT.md">License draft</a>
</p>
