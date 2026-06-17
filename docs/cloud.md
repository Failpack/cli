# FailPack Cloud

FailPack Cloud is the hosted layer for report history, workspace visibility, AI analysis and team workflows.

FailPack remains local-first: capture starts on your machine, and cloud upload is explicit.

## When to use Cloud

Use Cloud when debugging context needs to leave your machine safely, for example:

- keeping report history,
- syncing report versions,
- tracking fixed, unfixed and investigated states,
- opening report links from the dashboard,
- running AI-assisted analysis,
- sharing context with a team workspace.

## Cloud commands

```bash
failpack login
failpack whoami
failpack cloud upload
failpack cloud sync
failpack cloud open <id>
failpack cloud delete <id>
```

## AI commands

Cloud and AI commands require a logged-in FailPack account.

```bash
failpack analyze
failpack security
```

## Production API

Published builds use:

```text
https://api.failpack.dev/v1
```

## Privacy

Cloud upload is never automatic.

Users must explicitly run or confirm a cloud command before local report data leaves the machine.

Before uploading, review generated reports and make sure they do not contain sensitive data you do not want to share.

## Status

FailPack service status is available at:

https://status.failpack.dev
