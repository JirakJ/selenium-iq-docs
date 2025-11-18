---
layout: default
title: Getting Started
---

# Getting Started with SeleniumIQ

This guide walks you from installation to your first AI-generated locator inside IntelliJ IDEA.

## Prerequisites

- IntelliJ IDEA 2021.3 or newer (Community or Ultimate)
- Java 11+ configured in the IDE
- Existing Selenium project (Maven/Gradle) or a fresh template
- Internet access for AI-powered capabilities

## 1. Install the Plugin

1. Open IntelliJ IDEA → `Settings` → `Plugins`
2. Search for **SeleniumIQ**
3. Click `Install` and restart the IDE

### Offline Installation

If your machine has limited connectivity, download the latest `.zip` from the [releases page](https://github.com/JirakJ/selenium-iq-plugin/releases) and install via `Settings → Plugins → ⚙ → Install Plugin from Disk`.

## 2. Prepare Your Project

- Ensure WebDriver binaries are resolvable via PATH or Maven/Gradle dependencies
- Verify your test framework (JUnit/TestNG) runs locally before adding AI steps
- Enable "Delegate build/run actions to Gradle" for more accurate instrumentation

## 3. Generate Locators with AI

1. Open a test class and place the caret inside a failing locator
2. Right-click → `SeleniumIQ → Generate AI Locator`
3. Provide DOM context if prompted and accept the recommended selector

> **Tip:** Keep the SeleniumIQ tool window open to compare proposed selectors side-by-side.

## 4. Self-Healing During Test Runs

- Run tests with `SeleniumIQ Self-Heal` configuration (auto-created after install)
- When a locator fails, SeleniumIQ pauses execution, offers candidate replacements, and patches the code upon confirmation
- All changes are tracked as IDE-local patches so you can review before committing

## 5. CI/CD Integration

- Export CI snippets from the SeleniumIQ panel (`⋮ → Export Pipeline`)
- Commit generated YAML to your pipeline (GitHub Actions, Jenkins, GitLab CI)
- Use the `SELENIUMIQ_API_KEY` secret to authenticate premium self-healing in CI

## Troubleshooting Checklist

| Symptom | Recommendation |
| --- | --- |
| Plugin not visible | Confirm IDE version ≥ 2021.3 and restart after install |
| AI locator fails | Provide more DOM context; use the "Capture DOM" button before requesting |
| Headless run hangs | Update to v1.1.2, which skips the welcome dialog automatically |
| Self-heal not triggered in CI | Ensure the `--enable-self-heal` flag is present in the runner command |

## Next Steps

- Explore the [Feature Guide]({{ '/features/' | relative_url }}) to discover analytics dashboards, flakiness scoring, and page-object generation
- Compare plans in [Premium Tiers]({{ '/premium-tiers/' | relative_url }}) to unlock advanced coordination features for your team
- File a [Docs Update]({{ '/issue-tracker/' | relative_url }}) if any step above needs clarification
