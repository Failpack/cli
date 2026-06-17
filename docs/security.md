# FailPack Security

FailPack helps developers package debugging context safely.

## Default security principles

- Local-first by default.
- No automatic uploads.
- Secret redaction before reports are saved.
- `.env` files ignored by default.
- Private keys ignored by default.
- Cloud features require explicit confirmation.
- Generated reports should be reviewed before sharing.

## Local-first behavior

Reports are generated on your machine.

Nothing is uploaded unless you explicitly run or confirm a cloud command.

Local commands work without login. Cloud and AI commands require FailPack Cloud and a logged-in account.

## Review before sharing

Automatic redaction is helpful, but not perfect.

Always review generated reports before sharing them with teammates, support, public issues, AI assistants or FailPack Cloud.

## Vulnerability reports

Please report security issues privately. See `SECURITY.md` for the full policy.
