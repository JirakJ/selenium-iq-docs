---
layout: default
title: Contributing
---

# Contributing

Help keep the SeleniumIQ docs accurate and approachable. Follow this workflow for changes:

## 1. Open an Issue
- Choose the issue template that fits (bug, feature, docs update)
- Include reproduction steps, screenshots, or context links
- Tag `needs-info` if triage should request more details

## 2. Branch Strategy
- Fork the repo if you lack write access
- Create a feature branch: `docs/<short-topic>`
- Keep pull requests focused—one area per PR

## 3. Writing Guidelines
- Use concise, action-oriented English
- Prefer ordered lists for step-by-step instructions
- Include code blocks with language hints (` ```bash `, ` ```kotlin `)
- Update cross-links when adding new pages (e.g., nav table on `index.md`)

## 4. Local Preview

```bash
bundle install
bundle exec jekyll serve --source docs --destination _site --livereload
```

Confirm the page renders correctly before opening a PR.

## 5. Pull Request Checklist

- [ ] Links tested locally
- [ ] Screenshots attached if the layout changes
- [ ] Issue reference included (e.g., `Closes #42`)
- [ ] Release notes updated when user-facing behavior changes

## 6. After Merge
- Ensure GitHub Pages deployment succeeds (see workflow logs)
- Cross-link any relevant plugin PRs or releases so end-to-end documentation stays current

Thanks for keeping SeleniumIQ documentation healthy!

