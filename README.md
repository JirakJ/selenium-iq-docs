# SeleniumIQ Docs

Centralized documentation and lightweight issue tracking for the SeleniumIQ IntelliJ plugin. These pages are published via GitHub Pages so release notes, onboarding guides, and troubleshooting playbooks stay in sync with the main codebase.

## Repository Layout

```
selenium-iq-docs/
├── README.md
├── LICENSE
├── Gemfile
├── Gemfile.lock
├── _config.yml
├── docs/
│   ├── _layouts/default.html
│   ├── index.md
│   ├── getting-started.md
│   ├── features.md
│   ├── premium-tiers.md
│   ├── troubleshooting.md
│   ├── faq.md
│   ├── changelog.md
│   ├── contributing.md
│   └── issue-tracker.md
└── .github/
    ├── ISSUE_TEMPLATE/
    │   ├── bug-report.yml
    │   ├── feature-request.yml
    │   ├── docs-update.yml
    │   └── config.yml
    └── workflows/docs.yml
```

## Local Preview

```bash
bundle install
bundle exec jekyll serve --source docs --destination _site --livereload
```

Open http://127.0.0.1:4000 once the server reports "Server running". Jekyll watches the `docs/` folder, so edits refresh automatically.

## Deployment

- Push changes to `main`; the `Deploy Docs` GitHub Actions workflow builds the site with Jekyll and publishes the `_site` artifact to the `gh-pages` branch.
- GitHub Pages settings should target **Branch: gh-pages** with the default root folder.
- For custom domains, add a `CNAME` file under `docs/` and configure the DNS records.

## Issue Tracking Overview

Documentation-specific requests live in this repository using the pre-filled issue templates:
- `Bug Report` for incorrect docs or plugin regressions that require doc updates.
- `Feature Request` for new content or product enhancements that impact the docs.
- `Docs Update` for typos, reorganizations, or missing sections.

Development work for the IntelliJ plugin remains in [`selenium-iq-plugin`](https://github.com/JirakJ/selenium-iq-plugin), but cross-links between repos keep releases aligned.
