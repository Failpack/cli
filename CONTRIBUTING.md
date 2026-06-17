# Contributing to FailPack

Thanks for your interest in FailPack.

This repository is used for public documentation, issue tracking, support information and release communication for FailPack CLI.

FailPack is not currently an open-source project. Public contributions are limited to issues, feedback, documentation suggestions and safe reproduction reports.

## Good ways to contribute

You can help by opening issues for:

- CLI bugs,
- install problems,
- confusing command output,
- documentation mistakes,
- unclear onboarding,
- feature requests,
- safe reproduction reports,
- status page or service availability problems.

## Before opening an issue

Please check:

- https://failpack.dev/docs
- existing GitHub issues
- https://status.failpack.dev

If the service is degraded or unavailable, check the status page first.

## Bug reports

A good bug report includes:

- operating system,
- Node.js version,
- npm version,
- FailPack CLI version,
- command you ran,
- expected result,
- actual result,
- sanitized logs,
- whether the project uses Git,
- whether the issue happens in a clean test folder.

Example:

```text
OS: Windows 11
Node.js: 22.x
npm: 10.x
FailPack CLI: 0.x.x
Command: failpack capture --cmd "npm run build"
Expected: report created in .failpack/reports
Actual: command failed with ...
```

## Security issues

Do not report security issues publicly.

Use:

```text
security@failpack.dev
```

See `SECURITY.md` for details.

## Pull requests

This repository may accept small documentation-only pull requests in the future, but product code contributions are not currently accepted here.

Before spending time on a pull request, open an issue first and ask whether the change fits the current repository scope.

## Do not submit

Please do not submit:

- secrets,
- tokens,
- private keys,
- `.env` files,
- private source code,
- customer data,
- logs containing credentials,
- copyrighted material you do not own,
- large generated files,
- unrelated promotional content.

## Repository rights

This repository is not published under an open-source license.

See `NOTICE.md` for repository usage terms.
