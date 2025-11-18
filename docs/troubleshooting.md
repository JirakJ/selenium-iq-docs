---
layout: default
title: Troubleshooting
---

# Troubleshooting

Quick fixes for the most common SeleniumIQ hiccups. If an issue persists, attach logs and open a [Bug Report](https://github.com/JirakJ/selenium-iq-docs/issues/new/choose).

## Installation Problems

### Plugin Not Visible in Marketplace
- Ensure your IDE version is 2021.3+ (Help → About)
- Check "Early Access" channel toggle inside the Marketplace dialog
- For air-gapped networks, install from disk using the latest `.zip`

### Verification Failed During Install
- Clear IntelliJ caches: `File → Invalidate Caches / Restart`
- Remove remnants under `~/Library/Application Support/JetBrains/<IDE>/plugins/selenium-iq`
- Retry installation

## Runtime Issues

### AI Request Times Out
- Verify outbound HTTPS to `api.JirakJ.com` is allowed
- Re-authenticate via the SeleniumIQ tool window → `Sign In`
- Downgrade concurrency (Settings → SeleniumIQ → "Max concurrent AI jobs")

### Tool Window Missing
- `View → Tool Windows → SeleniumIQ`
- Reset window layout via `Window → Restore Default Layout`
- Disable conflicting plugins that override tool windows

### Self-Heal Does Not Trigger
- Confirm tests run with the `SeleniumIQ Self-Heal` run configuration
- Ensure premium license is active (Team tier or above for CI heals)
- Add `--enable-self-heal` flag when running via CLI or CI

## CI/CD Failures

| Symptom | Action |
| --- | --- |
| GitHub Actions job stuck on "Waiting for SeleniumIQ" | Ensure `SELENIUMIQ_API_KEY` secret exists and is referenced in the workflow |
| Headless Chromium crashes | Update to SeleniumIQ v1.1.2 and set `--disable-features=VizDisplayCompositor`
| Missing DOM snapshots in CI | Enable artifact upload (`upload-artifact` step) or configure the SeleniumIQ agent to emit snapshots to `/tmp/JirakJ` |

## Collecting Diagnostics

1. Open the SeleniumIQ tool window → `⋮ → Export Diagnostics`
2. Attach the generated `.zip` to the GitHub issue
3. Include IDE logs via `Help → Collect Logs and Diagnostic Data`

## Still Stuck?

- Email: support@JirakJ.com (Team SLA 4h, Enterprise 1h)
- Slack: `#JirakJ-support` (available for Team+ customers)
- Community forum: https://community.JirakJ.com

Remember to sanitize any proprietary data before sharing logs.

