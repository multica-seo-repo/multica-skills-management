# Multica Skills Management

Central catalog for Multica skills maintained by [multica-seo-repo](https://github.com/multica-seo-repo), grouped by series.

Each skill keeps its own repository, files, and Git history. This repository provides navigation and a place for confirmed Multica-to-GitHub bindings.

## Series index

| Series | Repositories | Location |
| --- | ---: | --- |
| [Onsite Audit](#onsite-audit) | 9 | multica-seo-repo |
| [Content Publishing](#content-publishing) | 3 | multica-seo-repo |

Catalog checked against GitHub and Multica on **2026-11-05**. The Onsite Audit series contains 9 repositories in `multica-seo-repo`, all with confirmed Multica skill bindings. One additional imported skill has a confirmed binding in `firstpage-seo`.

## Onsite Audit

Series topic: `onsite-audit`. The following repositories belong to this Organization and currently have the `multica` and `onsite-audit` topics.

| Skill / purpose | Repository | Status |
| --- | --- | --- |
| Shared Screaming Frog configuration | [Onsite_audit_SF_shared_config](https://github.com/multica-seo-repo/Onsite_audit_SF_shared_config) | Has commits |
| HTTPS and hostname consistency | [Onsite_audit_HTTPS_related_checking](https://github.com/multica-seo-repo/Onsite_audit_HTTPS_related_checking) | Has commits |
| robots.txt checks | [Onsite_audit_robot_txt_checking](https://github.com/multica-seo-repo/Onsite_audit_robot_txt_checking) | Has commits |
| Audit robots meta tags for filters, utility pages and unintended noindex using supplied Screaming Frog exports; produce Checklist and issue workbook (12.1–12.3) | [Onsite_audit_12_robots_meta_tag](https://github.com/multica-seo-repo/Onsite_audit_12_robots_meta_tag) | Confirmed binding and published snapshot |
| XML sitemap checks | [Onsite_audit_sitemap_check](https://github.com/multica-seo-repo/Onsite_audit_sitemap_check) | Has commits |
| Pagination checks | [Onsite_audit_pagination_check](https://github.com/multica-seo-repo/Onsite_audit_pagination_check) | Has commits |
| Hreflang and multilingual checks | [Onsite_audit_hreflang_check](https://github.com/multica-seo-repo/Onsite_audit_hreflang_check) | Has commits |
| Page titles, meta descriptions, headings, and images | [Onsite_content_audit_pagetitle-meta_description__heading_image](https://github.com/multica-seo-repo/Onsite_content_audit_pagetitle-meta_description__heading_image) | Has commits |
| Audit report consolidation | [Onsite_audit_Report_Consolidator](https://github.com/multica-seo-repo/Onsite_audit_Report_Consolidator) | Has commits |

### Imported skill in firstpage-seo

| Skill | Repository path | Status |
| --- | --- | --- |
| Canonical, meta tags and images extraction | [onsite-canonical-meta-images-extraction-multica](https://github.com/firstpage-seo/onsite-checking-AI-workflows/tree/main/.claude/skills/onsite-canonical-meta-images-extraction-multica) | Confirmed binding and published snapshot |

## Content Publishing

Series topic: `content-publishing`. All repositories share `multica` and `content-publishing`; skill-specific topics include `blog-upload`, `wordpress`, `blog-writing` and `docx`.

| Skill / purpose | Repository | Status |
| --- | --- | --- |
| Upload ready HTML article fragments with an explicit title and selected featured image to WordPress as verified drafts using project-local credentials | [blog-upload-v2](https://github.com/multica-seo-repo/blog-upload-v2) | Confirmed binding and published snapshot |
| Write a finished article TXT with meta title and meta description from a completed brief or outline | [blog-writing-from-brief](https://github.com/multica-seo-repo/blog-writing-from-brief) | Confirmed binding and published snapshot |
| Insert finished article TXT and metadata into a supplied brief DOCX while preserving unrelated content | [filling-article-to-brief](https://github.com/multica-seo-repo/filling-article-to-brief) | Confirmed binding and published snapshot |

Added on **2026-11-05**. The complete skill package lives in its independent repository; this catalog contains navigation and its publishing binding.

## Catalog and publishing bindings

- **This README** is the human-readable repository catalog. A link can be listed before its Multica identity is confirmed.
- **[skills-map.json](skills-map.json)** contains thirteen confirmed, machine-readable skill bindings. Each entry records a `workspace_id`, `skill_id`, GitHub repository ID/name/branch, skill-relative `path`, and `sync_enabled` state. Binding confirmation does not mean a new content publication has completed.
- Catalog inclusion, matching names, and GitHub topics do **not** establish a publishing binding.
- Within verified publishing authorization, the GitHub Agent may establish deterministic bindings after validating source and repository identity, branch and path. New destinations or ambiguous ownership require human confirmation. The root directory is represented by `.`.
- A binding identifies the source by `workspace_id` and `skill_id`, and the target by repository ID, name, branch, and relative path. Do not store credentials or personal machine paths.
- When confirmed bindings are added, keep the README catalog aligned. Keep unbound entries clearly identified.

## Publishing workflow

1. The Agent and Skills Governor completes and validates an approved skill change in Multica.
2. The Governor preserves the exact final snapshot and dispatches it to the GitHub Agent. The Governor may finish after confirming actual assignment or queueing and completing required delivery steps; a handover note alone is not dispatch.
3. The GitHub Agent reads and validates the confirmed binding. Missing or deterministically invalid bindings may be created or repaired within verified authorization. Ambiguous ownership or a new destination requires human confirmation.
4. The GitHub Agent compares the snapshot with the remote baseline, validates the change, commits, pushes, and verifies the remote result. No difference means no new commit.
5. The GitHub Agent records the repository, commit SHA, and sync status on the original or linked sync issue.

This workflow is the agreed operating design; creating this catalog does not deploy an agent or enable synchronization.

## Recovery and maintenance

- No scheduled auto-check or webhook is configured.
- A handover, manual sync request, retry request, or approved restore request triggers work.
- Preserve final snapshots and completed-stage records after failures. Check the remote state before retrying; resume only incomplete steps.
- Restore an approved historical version through the authorized Multica editor, then publish a **new commit**.
- Do not delete repositories, force-push, rewrite Git history, or infer a replacement binding from a missing repository.
- Changes to repository names, locations, series, or confirmed bindings must be reflected in the catalog and mapping as applicable. Ordinary content commits do not require catalog changes.

## Workspace configuration backups

The public companion repository, [multica_workspace_backup](https://github.com/multica-seo-repo/multica_workspace_backup), stores versioned backups of agent system prompts, workspace General Rules, and explicitly selected workspace settings.

- Configuration bindings belong in its `config-map.json`; skill publishing bindings remain in this repository's `skills-map.json`.
- Workspace files are grouped by workspace ID, and agent prompts by agent ID. See the [backup repository README](https://github.com/multica-seo-repo/multica_workspace_backup#readme) for the layout and publishing rules.
- The backup repository is publicly readable; publishing still requires write access. Include only configuration content approved for public sharing. This catalog contains navigation only; the backed-up prompts and rules belong in the companion repository.
- The repository starts without confirmed Multica bindings or exported workspace content. Creating it does not deploy the GitHub Agent or enable synchronization.

Do not store secrets, SSH keys, tokens, or runtime credentials in either repository.

## First publication: NEW repository proposal

For a verified completed skill with no confirmed repository, first inspect mappings and repository evidence to avoid duplicates. Failed authentication or a broken binding is not evidence that no repository exists.

Present this confirmation card before creating a repository:

| Field | Required proposal |
| --- | --- |
| Action | **NEW — create an independent skill repository** |
| Source | Workspace ID, skill ID, name and source revision |
| Destination | Organization, repository name and full organization/repository |
| Visibility | Public or private; explicitly disclose public publication |
| Branch and package path | Proposed default branch and relative path, usually main and . |
| Catalog | Catalog repository and branch |
| Mapping | Source binding in the current skills-map.json schema using the verified repository ID |
| README | Skill purpose, inputs/outputs, agent boundaries, usage and tests; catalog summary and link |
| Topics and series | Prefer relevant existing classifications; label proposed additions NEW |
| Recurring authorization | Ask whether future completed versions of this same skill and corresponding README/catalog maintenance are authorized within the confirmed destination, branch, path and visibility |

Retain the original member-authored confirmation. After confirmation, proceed with the included repository creation, package and README publication, mapping, catalog and topics without asking separately for each step. Verify actual repository identity and visibility, and report content and catalog commits separately. Topics mean GitHub repository topics and catalog classifications, not Git release tags.

Keep publisher-authored documentation distinct from the immutable source package. Do not silently alter source files or overwrite a supplied README. Reuse recurring authorization only within its confirmed scope; a new repository, changed visibility or additional skill is not automatically covered. Track each stage independently and resume incomplete stages after failures without creating duplicates.
