# SiteGO Tag and Release Policy

[简体中文](README.zh-CN.md)

Author: vigo. Date: 2026-10-29. Scope: future release rules requested by the project owner; this document does not create a tag or publish an application.

## Versions and Commits

Use `vX.Y.Z` for stable releases and `vX.Y.Z-rc.N` for release candidates, for example `v0.1.0-rc.1`. Examples are not published versions.

Each public version maps to a specific accepted commit, an annotated tag, and a GitHub Release. Prefer Chinese tag annotations, use vigo or langya as the author, and record the actual creation date. Never move or overwrite a published tag; changes to code or artifacts require a new version.

From `v1.0.0`, increase the major version for incompatible changes, the minor version for compatible features, and the patch version for compatible fixes. During `v0` development, use a new minor version for breaking changes and describe them explicitly. Increment `rc.N` for each new candidate; after acceptance, create a separate stable tag on the accepted commit, leaving all candidate tags intact.

Maintain Codeup and GitHub commits and releases separately. Never tag private Codeup history for publication on GitHub. Keep Afu's worker out of public commits, downloadable archives, packages, and images until separately authorized.

## Release Page Order

1. Version and release theme.
2. Important / 重要提示: essential upgrade information, compatibility changes, or affected scope; omit when none apply.
3. Chinese notes: additions, improvements, fixes, upgrades, known issues, and verification scope.
4. English notes matching the Chinese version item by item.
5. What's Changed: actual public commits or pull requests within this tag's scope; never invent references.
6. New Contributors: include only when there are actual first-time contributors.
7. Full Changelog: compare the previous public version with this version; identify the initial release explicitly.
8. Assets: delivered files, checksums, and corresponding image digests.

Start from either the [Chinese-guided template](RELEASE_NOTES_TEMPLATE.zh-CN.md) or the [English-guided template](RELEASE_NOTES_TEMPLATE.md). Each already contains both language sections and one set of shared change, contributor, comparison, and asset sections. Do not concatenate the templates. Fill every placeholder, keep the two languages aligned, and remove sections that do not apply. `VERSION` must be the exact tag name, including `v`. Before publication, confirm that no `{{...}}` placeholders remain and that each section appears only once. Generated commit lists supplement rather than replace user-facing notes.

## Artifacts and Acceptance

- Associate `sitego-control` and `sitego-worker` with one release version, while recording each build's evidence, supported architectures, and image digest.
- Record source publication, container image publication, deployment, and business acceptance separately, with each status, date, and evidence. A published artifact does not establish deployment or business acceptance.
- List only packages, images, and links that have actually been delivered and verified. Do not invent platform downloads to imitate another project's release page.
- Provide SHA-256 checksums for downloads and immutable image digests rather than relying solely on the mutable `latest` tag.
- Mark candidates that have not passed stable release gates as Pre-release, not as the stable Latest release.
- Prepare a draft, bilingual notes, and all artifacts before publication; verify the tag target, release contents, and downloads afterward.
- Report signature status accurately when verifiable signatures exist. `Verified` describes signature verification, not functional testing or business acceptance.

The current public repository contains documentation only and does not warrant an application version tag. Final commercial license terms, source publication, installation, and functional acceptance retain their separate gates.

## Maintenance Record

Record notes, exact commits, tags, artifact digests, verification scope, limitations, and upgrade, rollback, and recovery steps for each version. Keep release notes and version records aligned; do not describe unfinished roadmap items as delivered features.

References: [GitHub release management](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository), [signature verification](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification).
