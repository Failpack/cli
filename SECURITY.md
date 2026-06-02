# Security Policy

## Reporting a vulnerability

If you discover a security issue in FailPack, please do not open a public issue with sensitive details.

Contact:

```text
security@failpack.dev
```

If this email is not active yet, please open a private report through the GitHub Security tab if available.

## Security model

FailPack is designed as a local-first CLI.

By default:

- reports are generated locally,
- files are not uploaded automatically,
- common secrets are redacted,
- `.env` files are not included by default,
- private keys are not included by default.

Future cloud features will require explicit user action and authentication.

## Sensitive data warning

FailPack attempts to redact common secrets automatically, but users should always review generated reports before sharing them publicly.
