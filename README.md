<div align="center">

<img src="https://failpack.dev/icon-512.png" alt="FailPack logo" width="120" height="120" />

# FailPack CLI

**AI-ready failure reports from your terminal.**

FailPack CLI captures the exact context behind broken builds, command errors and regressions — then turns it into clean, redacted reports for AI assistants, GitHub issues, teammates and support.

<p>
  <a href="https://failpack.dev">
    <img src="https://img.shields.io/badge/website-failpack.dev-111827?style=for-the-badge" alt="FailPack website" />
  </a>
  <a href="https://failpack.dev/docs">
    <img src="https://img.shields.io/badge/docs-failpack.dev%2Fdocs-2563eb?style=for-the-badge" alt="FailPack documentation" />
  </a>
  <a href="https://www.npmjs.com/package/@failpack/cli">
    <img src="https://img.shields.io/npm/v/@failpack/cli?style=for-the-badge&label=npm&color=cb3837" alt="npm package version" />
  </a>
  <a href="https://status.failpack.dev">
    <img src="https://img.shields.io/badge/status-status.failpack.dev-16a34a?style=for-the-badge" alt="FailPack status page" />
  </a>
</p>

<p>
  <a href="https://status.failpack.dev">
    <img src="https://uptime.betterstack.com/status-badges/v3/monitor/2ph1a.svg" alt="FailPack dashboard uptime" />
  </a>
  <a href="https://status.failpack.dev">
    <img src="https://uptime.betterstack.com/status-badges/v3/monitor/2ph96.svg" alt="FailPack API uptime" />
  </a>
</p>

</div>

---

## About this repository

This repository is the public home for FailPack CLI documentation, issue tracking, support information and release notes.

The FailPack CLI package is published on npm as:

```bash
@failpack/cli
```

Global command:

```bash
failpack
```

---

## Install

Install FailPack CLI globally:

```bash
npm install -g @failpack/cli
```

Run it inside your project:

```bash
failpack
```

On first run, FailPack asks whether you trust the current folder before creating local configuration.

---

## Quick start

Capture a failing command:

```bash
failpack capture --cmd "npm run build"
```

Capture test output:

```bash
failpack capture --cmd "npm test"
```

Generate AI-ready context from an error log:

```bash
failpack ai --error ./error.log --include-diff
```

Check local report status:

```bash
failpack status
```

Run diagnostics:

```bash
failpack doctor
```

---

## What FailPack CLI does

FailPack helps developers turn messy failure context into structured reports.

It can collect and organize:

* failed command output,
* error logs,
* project metadata,
* Git branch and diff context,
* selected environment details,
* relevant debugging context,
* local report history,
* AI-ready Markdown prompts,
* optional ZIP bundles for sharing.

The goal is to make debugging easier without manually pasting random logs, screenshots and files into an issue or AI assistant.

---

## Output files

FailPack writes local reports to:

```txt
.failpack/reports
```

A report may include:

### `failpack-report.md`

Readable report for GitHub issues, teammates, support channels and internal debugging.

### `failpack-ai-prompt.md`

AI-ready debugging prompt with structured context.

### `failpack-context.json`

Machine-readable metadata for tooling, dashboards and automation.

### `failpack-bundle.zip`

Optional portable bundle for private sharing.

---

## Common commands

```bash
failpack
failpack init
failpack capture --cmd "npm run build"
failpack capture --cmd "npm test" --project ./my-app --no-zip
failpack ai --error ./error.log --include-diff
failpack report --github --discord
failpack status
failpack fix v1
failpack unfix v2
failpack doctor
failpack clean --yes
```

Cloud and AI commands:

```bash
failpack login
failpack whoami
failpack cloud upload
failpack cloud sync
failpack cloud open <id>
failpack cloud delete <id>
failpack analyze
failpack security
```

---

## Local-first by default

FailPack CLI is designed to work locally first.

By default:

* reports are generated on your machine,
* local commands work without login,
* files are not uploaded automatically,
* generated reports can be reviewed before sharing,
* cloud upload requires an explicit command or confirmation.

Cloud features are available when you want hosted report history, workspace visibility, AI analysis or team workflows.

---

## Security model

FailPack is built to collect useful debugging context while reducing the risk of leaking sensitive project data.

Security-focused defaults include:

* common keys, tokens and credentials are redacted,
* `.env` files are ignored by default,
* private keys are ignored by default,
* cloud upload is explicit,
* AI and Cloud actions require a logged-in FailPack account.

Automatic redaction helps, but it is not a replacement for review. Always check generated reports before sharing them outside your machine or team.

---

## Documentation

Main documentation:

* Website: https://failpack.dev
* Docs: https://failpack.dev/docs
* CLI docs: https://github.com/Failpack/cli/blob/main/docs/cli.md
* Cloud docs: https://github.com/Failpack/cli/blob/main/docs/cloud.md
* Security docs: https://github.com/Failpack/cli/blob/main/docs/security.md
* Security policy: https://github.com/Failpack/cli/blob/main/SECURITY.md

---

## Status

FailPack service status is available at:

**https://status.failpack.dev**

Monitored services:

* FailPack Dashboard

<p>
  <a href="https://status.failpack.dev">
    <img src="https://uptime.betterstack.com/status-badges/v3/monitor/2ph1a.svg" alt="FailPack dashboard uptime" />
  </a>
</p>

* FailPack API

<p>
  <a href="https://status.failpack.dev">
    <img src="https://uptime.betterstack.com/status-badges/v3/monitor/2ph96.svg" alt="FailPack API uptime" />
  </a>
</p>

---

## Reporting issues

Use GitHub Issues for:

* CLI bugs,
* documentation problems,
* install issues,
* confusing command output,
* feature requests,
* security-safe reproduction reports.

When reporting a bug, include:

* your operating system,
* Node.js version,
* FailPack CLI version,
* command you ran,
* expected result,
* actual result,
* relevant sanitized output.

Do not paste secrets, tokens, private keys, `.env` files or sensitive customer data into public issues.

---

## Links

* Website: https://failpack.dev
* Documentation: https://failpack.dev/docs
* Status page: https://status.failpack.dev
* NPM package: https://www.npmjs.com/package/@failpack/cli
* Repository: https://github.com/Failpack/cli

---

## Development status

FailPack is currently in early development.

The CLI, Cloud dashboard, AI analysis and security tooling are being improved continuously. Commands, output formats and Cloud features may change while the product moves toward a stable public release.
