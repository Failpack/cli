# FailPack Security

FailPack is designed to help developers package debugging context safely.

## Default security principles

- Local-first by default
- No automatic uploads
- Secret redaction before saving reports
- `.env` files ignored by default
- Private keys ignored by default
- Cloud features require explicit confirmation

## User responsibility

Automatic redaction is helpful, but not perfect. Always review generated reports before sharing them publicly.
