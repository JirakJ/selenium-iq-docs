# SeleniumIQ Docs

Public documentation hub for the SeleniumIQ IntelliJ plugin. This repo is structured for GitHub Pages so we can publish release notes, onboarding guides, and issue-tracking workflows next to the codebase.

## Repository Layout

```
selenium-iq-docs/
├── README.md
├── LICENSE
├── Gemfile
├── _config.yml
└── docs/
    ├── _layouts/
    │   └── default.html
    ├── index.md
    ├── getting-started.md
    ├── features.md
    └── issue-tracker.md
```

## Local Preview

```bash
bundle install
bundle exec jekyll serve --source docs --destination _site
```

Open http://127.0.0.1:4000 after the server starts.

## Deploying to GitHub Pages

1. Push this repo to GitHub as `selenium-iq-docs`.
2. In the repository settings → **Pages**, choose branch `main` and folder `/docs`.
3. (Optional) Configure a custom domain via `CNAME`.

## Related Repositories

- Plugin source: https://github.com/jakubjirak/selenium-iq-plugin
- Documentation: https://github.com/jakubjirak/selenium-iq-docs

# selenium-iq-docs
