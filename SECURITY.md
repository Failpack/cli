# Security Policy

FailPack is a local-first developer tool that captures failure context, logs, Git state, project metadata and sanitized report data for debugging, AI review and support workflows.

Security reports are taken seriously.

## Reporting a vulnerability

Please do not open a public GitHub issue for security vulnerabilities.

Report security issues privately:

```text
security@failpack.dev
```

If this email is unavailable, use GitHub's private vulnerability reporting feature if it is enabled for this repository.

## What to include

When reporting a security issue, include as much safe context as possible:

- affected FailPack area,
- CLI version,
- operating system,
- command used,
- expected behavior,
- actual behavior,
- impact,
- reproduction steps,
- sanitized logs or screenshots.

Do not include real secrets, tokens, private keys, production credentials, customer data or private source code in the report.

## Security model

FailPack is designed around local-first capture.

By default:

- reports are generated on your machine,
- local commands work without login,
- cloud upload is explicit,
- common keys, tokens and credentials are redacted before reports are saved,
- `.env` files are ignored by default,
- private keys are ignored by default,
- generated reports should be reviewed before sharing.

Cloud and AI commands require FailPack Cloud and a logged-in account.

## Redaction limitations

FailPack attempts to redact common secrets automatically, but no automated redaction system is perfect.

Always review generated reports before sharing them with teammates, support, public issues, AI assistants or FailPack Cloud.

## Public issue warning

Do not paste sensitive data into public issues, including:

- API keys,
- JWT secrets,
- access tokens,
- database URLs,
- `.env` files,
- private keys,
- customer data,
- internal infrastructure details,
- unreleased proprietary source code.

## Status

FailPack service status is available at:

https://status.failpack.dev
