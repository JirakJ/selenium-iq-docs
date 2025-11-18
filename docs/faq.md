---
layout: default
title: FAQ
---

# Frequently Asked Questions

## Does SeleniumIQ send my test code to the cloud?
No. Only DOM snippets and metadata required for locator generation leave your machine. Code is processed locally inside IntelliJ.

## Which languages are supported?
Java, Kotlin, and Groovy are fully supported. JavaScript/TypeScript bindings are on the roadmap.

## How do I reset my API key?
Open the SeleniumIQ tool window → `Account` → `Regenerate API Key`. Update CI secrets immediately to avoid failed pipelines.

## Can I run SeleniumIQ without internet access?
Core IDE tooling works offline, but AI locator generation and self-healing require connectivity. Enterprise customers can request a private SaaS region for data residency.

## What telemetry is collected?
Anonymous usage stats (feature toggles, error codes). Logs, DOM snapshots, and code never leave your machine unless you explicitly export them for support.

## How are updates delivered?
Through JetBrains Marketplace. Enable automatic updates under `Settings → Plugins → ⚙ → Manage Plugin Repositories`.

## Does SeleniumIQ support Playwright or Cypress?
Not yet. The roadmap focuses on Selenium/WebDriver tooling inside IntelliJ, with API parity available for IDE-based test authoring.

## Where should I report security issues?
Email `security@JirakJ.com` with reproduction details. Expect a response within 48 hours.

Still have questions? File a [Docs Update]({{ '/issue-tracker/' | relative_url }}) issue and tag it with `question`.

