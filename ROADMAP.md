# SiteGO Public Roadmap

[简体中文](ROADMAP.zh-CN.md) · [Back to README](README.md)

Maintainer: Langya (`langya-ascend`). Document author: vigo. Updated: October 29, 2026.

Make the first public edition installable, verifiable, and operable before expanding providers and use cases. The November-December plan follows the sequence below. Dates are planning windows, not release commitments. Publication moves later if an earlier acceptance gate remains open.

## Reading Progress

- [x] The stated item is complete within its named scope and has recorded evidence.
- [ ] The item is pending, in progress, or still has an unresolved acceptance gate.

**Development foundations and public delivery are tracked separately.** Local verification covers only the named environment and scenarios. It does not establish source publication, production deployment, or support for every provider mode. Development evidence alone does not check off a future public milestone.

## Completed Foundations

These design, development, and documentation baselines were recorded by **October 29, 2026**. They still require revalidation in the public candidate without the Afu worker.

- [x] **Architecture boundary:** one project maintains the `sitego-control` and `sitego-worker` image types; the admin console belongs to control.
- [x] **Separate publication materials:** GitHub README, roadmap, and publication rules are maintained independently of Codeup, with an explicit Afu worker exclusion.
- [x] **Single-question foundation:** local single-question API and result-replay evidence exists for Doubao and Yuanbao; not all modes are accepted.
- [x] **Durable scheduling foundation:** recorded automated checks cover the queue, logical-account exclusion, and account/platform budgets.
- [x] **Duplicate-request protection:** persisted idempotency and original-result replay have verification evidence; an unknown submitted result is not automatically resubmitted.
- [x] **Task-page cleanup:** confirm task-page closure before publishing completion and starting cooldown. Operator pages remain; cleanup failure retains protection.
- [x] **Console foundation:** local browser checks cover accounts, tasks, policies, audits, Chinese/English, and light/dark themes.
- [x] **Operator takeover foundation:** authenticated remote desktop, takeover locks, and release on exit have synthetic verification; real provider operation remains a separate gate.
- [x] **Local Linux foundation:** ARM64 build and isolated synthetic-runtime records exist for both image types; amd64, target hosts, and real providers are not thereby accepted.
- [x] **Product documentation:** bilingual README, real screenshots, system architecture, execution flow, and capability blueprint are prepared.

## November-December Plan

| Phase | Planning window | Objective | Exit gate |
| --- | --- | --- | --- |
| P1 · Public candidate | November 2–15, 2026 | An independently buildable candidate | Afu excluded; license and dependency inventory defined |
| P2 · Reliability | November 16–29, 2026 | Verify task, account, and resource safeguards | Reproducible fault and fixed-load evidence |
| P3 · Integration and installation | November 30–December 13, 2026 | Real business integration and deployment rehearsal | Scoped GEO, gateway, installation, and rollback checks pass |
| P4 · First publication preparation | December 14–27, 2026 | Deliver an accepted version | Publish only after every release gate passes |

### P1 · Public Candidate

- [ ] Prepare a clean public source candidate and file allowlist; inspect shared modules for private implementation.
- [ ] Exclude the Afu worker, related protocols, and samples; inspect every pushed history, branch, tag, and image layer.
- [ ] Finalize the rights holder, authorization contact, noncommercial terms, and third-party notices. Commercial use requires prior written approval.
- [ ] Verify independent builds of control, worker, and admin with Afu omitted.
- [ ] Pin supported Doubao/Yuanbao modes, response/source contracts, and a sanitized candidate-acceptance checklist.

### P2 · Reliability

- [ ] Recheck duplicate requests, cancellation, queue expiry, browser interruption, and process restart in the public candidate; verify no blind resubmission.
- [ ] Verify cross-project queue fairness, ten waiting places per provider, and same-identity exclusion. A shared caller key must not imply independent tenants.
- [ ] Run a fixed workload and at least 30 minutes of resource observation, recording latency, memory, browser-page counts, and failure categories.
- [ ] Recheck protection and audited recovery for unknown outcomes, login/verification, and cleanup failure, without clearing state to bypass protection.
- [ ] Verify each supported provider mode, answer text, and source completeness; explicitly list unsupported or failed items.

### P3 · Integration And Installation

- [ ] Run multiple tasks in a GEO test project and verify task states, answers, and persisted sources.
- [ ] Complete API-gateway integration against the contract, including errors, timeouts, and idempotency keys.
- [ ] Reproduce a fresh install from public-candidate files alone and verify the planned amd64 and ARM64 target environments separately.
- [ ] Rehearse legacy migration, backup, rollback, and key configuration; document which data cannot be reused directly.
- [ ] Verify takeover, disconnect release, login/verification handling, and task-page cleanup on the target environment. Wait for authorization when new infrastructure or accounts are needed.

### P4 · First Publication Preparation

- [ ] Reconcile the candidate's feature comparison, remaining issues, and acceptance evidence; every agreed gate passes.
- [ ] Review source, history, dependencies, credentials, and artifacts for publication; confirm no Afu worker or account profiles are included.
- [ ] Complete bilingual installation/operations documents, contribution guidance, Issue/PR templates, and a security-reporting contact.
- [ ] Publish the GitHub repository, release record, and two image types within the owner's approved scope, recording addresses and digests separately.
- [ ] Revalidate the published version from a fresh environment, align README/topics/changelog/limitations, and track the first reported issues.

## Later Candidates

These directions follow a stable first edition. No version or completion date is committed.

- [ ] **Operational visibility:** account-availability trends, queue latency, failure categories, resource trends, and notification rules.
- [ ] **Integration experience:** caller examples, candidate SDKs, task-progress integration, and reproducible GEO examples.
- [ ] **Adapter expansion:** a public adapter contract and conformance checks before adding providers. Afu still requires separate approval.

## Completion And Publication Rules

Update both languages together, recording completion date, candidate version, actual scope, result, and remaining limitations. Change `[ ]` to `[x]` only when the entire item's acceptance condition is satisfied. Split partial progress into independently verifiable items.

Implementation, source publication, image publication, server deployment, and business acceptance are distinct states. Publish sanitized progress summaries, not raw account data, private logs, or deployment configuration.

This roadmap governs the GitHub edition only. It does not change Codeup tasks, branches, release cadence, or private capabilities. See the [publication rules](PUBLISHING.md).
