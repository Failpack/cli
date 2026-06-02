# FailPack CLI

Create safe, shareable bug context packages for AI, GitHub issues and support.

> Pack your bug. Share the truth. Fix faster.

## Install

```bash
npm install -g @failpack/cli
```

## Usage

```bash
failpack
```

Current placeholder version:

```bash
failpack
```

Future versions of FailPack will help developers collect error logs, project context, environment details, Git changes and relevant config files into safe, shareable debug reports.

## What is FailPack?

FailPack is a local-first developer tool for packaging debugging context.

When a build fails, an app crashes, or a command throws confusing logs, FailPack helps generate a structured report that can be shared with:

- AI assistants
- GitHub issues
- teammates
- support channels
- clients

## Planned features

- Local debug reports
- AI-ready prompts
- GitHub issue reports
- Secret redaction
- ZIP debug bundles
- Project stack detection
- Git diff summaries
- Cloud reports
- Private share links
- Premium AI analysis

## Local-first by default

FailPack is designed to run locally first. Local reports are generated on your machine and are not uploaded anywhere unless you explicitly use cloud features in future versions.

## Security

FailPack will automatically redact common secrets such as API keys, tokens, private keys and database URLs.

You should still review generated reports before sharing them publicly.

## Package

NPM package:

```bash
@failpack/cli
```

Global command:

```bash
failpack
```

## Website

Coming soon:

```text
https://failpack.dev
```

## Repository

This repository is used for public documentation, issue tracking and release information for FailPack CLI.

## License

MIT
