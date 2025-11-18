---
layout: default
title: Docs Update Template
permalink: /docs-update/
---

# Docs Update Template

Use the **Docs Update** issue type when you spot missing or incorrect content. Provide the information below so the maintainers can reproduce and fix quickly:

1. **Page URL** – e.g., `/getting-started/`
2. **Current Text** – quote the sentence or section to adjust
3. **Expected Change** – describe the fix or paste suggested wording
4. **Reason** – clarify why the change is needed (new feature, typo, outdated)
5. **Screenshots** – optional but appreciated for layout issues

File a new issue via [GitHub](https://github.com/JirakJ/selenium-iq-docs/issues/new/choose) and select `Docs Update`.

## Recent Fixes

- 2025-11-18: Added `docs/assets/css/style.scss` so GitHub Pages can compile styles without failing in `Jekyll::Converters::Scss`.
- 2025-11-18: Noted that GitHub Pages now requires the `faraday-retry` gem, which is included automatically when using the `github-pages` bundle locally.
