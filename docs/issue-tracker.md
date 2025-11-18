---
layout: default
title: Issue Tracker
---

# Issue Tracking Workflow

SeleniumIQ uses two repositories side-by-side: `selenium-iq-plugin` for code and `selenium-iq-docs` for documentation. This page describes how we categorize, template, and automate issues.

## Label Taxonomy

| Label | Meaning |
| --- | --- |
| `bug` | Regression or incorrect behavior in plugin/docs |
| `feature` | Net-new capability or enhancement request |
| `docs` | Documentation-specific content updates |
| `ux` | Workflow or usability pain points |
| `needs-info` | Waiting for reporter to provide logs or repro details |
| `premium` | Requests tied to paid tiers |

## Issue Templates

We standardize triage via `.github/ISSUE_TEMPLATE`.

### Bug Report
- Observed vs expected behavior
- Environment (IDE, OS, plugin version)
- Reproduction steps and logs or screenshots

### Feature Request
- Problem statement explaining the need
- Proposed solution or UX flow
- Acceptance criteria and dependencies

### Docs Update
- Link to the affected page
- Summary of missing/incorrect content
- Suggested wording or resources

## Project Board Flow

1. **Backlog** – new items awaiting grooming
2. **In Progress** – active sprint work (link related PRs)
3. **Docs Ready** – engineering change merged; documentation pending
4. **Done** – deployed to Marketplace + docs published

## Cross-Repo Best Practices

- Reference plugin issues from docs using `JirakJ/selenium-iq-plugin#123`
- Mention docs PRs in plugin release notes when they affect user-facing behavior
- Keep changelog entries mirrored across both repos each release

## Automation

- GitHub Actions workflow adds `needs-info` if templates are incomplete
- Label sync bot mirrors labels between repos for shared issues
- Deploy workflow comments on linked plugin issues after docs publish

Need assistance? Contact `docs@JirakJ.com` or drop by the `#JirakJ-support` Slack channel (Team plan and above).
