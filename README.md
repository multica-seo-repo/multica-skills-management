# Multica Skills Management

Central catalog for Multica skills maintained by [multica-seo-repo](https://github.com/multica-seo-repo), grouped by series.

Each skill keeps its own repository, files, and Git history. This repository provides navigation and a place for confirmed Multica-to-GitHub bindings.

## Series index

| Series | Repositories | Location |
| --- | ---: | --- |
| [Onsite Audit](#onsite-audit) | 9 | multica-seo-repo |

Catalog checked against GitHub on **2026-11-02**. The catalog contains 9 repositories; one is an empty repository awaiting its first commit. These are repository counts, not confirmed Multica registration counts.

## Onsite Audit

Series topic: `onsite-audit`. The following repositories belong to this Organization and currently have the `multica` and `onsite-audit` topics.

| Skill / purpose | Repository | Status |
| --- | --- | --- |
| Shared Screaming Frog configuration | [Onsite_audit_SF_shared_config](https://github.com/multica-seo-repo/Onsite_audit_SF_shared_config) | Has commits |
| HTTPS and hostname consistency | [Onsite_audit_HTTPS_related_checking](https://github.com/multica-seo-repo/Onsite_audit_HTTPS_related_checking) | Has commits |
| robots.txt checks | [Onsite_audit_robot_txt_checking](https://github.com/multica-seo-repo/Onsite_audit_robot_txt_checking) | Has commits |
| Robots meta tag checks | [Onsite_audit_12_robots_meta_tag](https://github.com/multica-seo-repo/Onsite_audit_12_robots_meta_tag) | Empty repository — awaiting first commit |
| XML sitemap checks | [Onsite_audit_sitemap_check](https://github.com/multica-seo-repo/Onsite_audit_sitemap_check) | Has commits |
| Pagination checks | [Onsite_audit_pagination_check](https://github.com/multica-seo-repo/Onsite_audit_pagination_check) | Has commits |
| Hreflang and multilingual checks | [Onsite_audit_hreflang_check](https://github.com/multica-seo-repo/Onsite_audit_hreflang_check) | Has commits |
| Page titles, meta descriptions, headings, and images | [Onsite_content_audit_pagetitle-meta_description__heading_image](https://github.com/multica-seo-repo/Onsite_content_audit_pagetitle-meta_description__heading_image) | Has commits |
| Audit report consolidation | [Onsite_audit_Report_Consolidator](https://github.com/multica-seo-repo/Onsite_audit_Report_Consolidator) | Has commits |

## Catalog and publishing bindings

- **This README** is the human-readable repository catalog. A link can be listed before its Multica identity is confirmed.
- **[skills-map.json](skills-map.json)** is reserved for confirmed, machine-readable publishing bindings. It starts with an empty `skills` array because real Multica workspace IDs and skill IDs have not yet been supplied or verified.
- Catalog inclusion, matching names, and GitHub topics do **not** establish a publishing binding.
- Before adding a binding, a human must confirm the target repository, branch, and skill-relative path. The root directory is represented by `.`.
- A binding identifies the source by `workspace_id` and `skill_id`, and the target by repository ID, name, branch, and relative path. Do not store credentials or personal machine paths.
- When confirmed bindings are added, keep the README catalog aligned. Keep unbound entries clearly identified.

## Publishing workflow

1. The Agent and Skills Governor completes and validates an approved skill change in Multica.
2. The Governor preserves the exact final snapshot and asynchronously hands it to the GitHub Agent. The Governor can finish its current run after recording the handover.
3. The GitHub Agent reads and validates the confirmed binding. Missing or invalid bindings require human guidance and confirmation before publishing.
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

The private companion repository, [multica_workspace_backup](https://github.com/multica-seo-repo/multica_workspace_backup), stores versioned backups of agent system prompts, workspace General Rules, and explicitly selected workspace settings.

- Configuration bindings belong in its `config-map.json`; skill publishing bindings remain in this repository's `skills-map.json`.
- Workspace files are grouped by workspace ID, and agent prompts by agent ID. See the [backup repository README](https://github.com/multica-seo-repo/multica_workspace_backup#readme) for the layout and publishing rules.
- Access to the backup repository requires the appropriate GitHub permissions. This public catalog contains navigation only; it does not contain the backed-up prompts or rules.
- The repository starts without confirmed Multica bindings or exported workspace content. Creating it does not deploy the GitHub Agent or enable synchronization.

Do not store secrets, SSH keys, tokens, or runtime credentials in either repository.
