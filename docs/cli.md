# FailPack CLI Documentation

FailPack CLI captures failed commands, logs, Git state, project metadata and sanitized context into reports that are ready for AI assistants, GitHub issues, teammates and support.

## Installation

Install the CLI globally and run it from inside the project you want to debug.

```bash
npm install -g @failpack/cli
failpack
```

On first run in a repository, FailPack asks whether you trust the current folder and creates a local `.failpackrc.json` when accepted.

## Your first capture

Run a failing command through FailPack to create a local report package.

```bash
failpack capture --cmd "npm run build"
failpack capture --cmd "npm test" --project ./my-app --no-zip
```

## Interactive app

Running `failpack` opens a terminal app with project status, recent report state, account/cloud state, activity log and command suggestions.

Available interactive commands include:

```text
run <command>
report
status
fix [version]
unfix [version]
clean
doctor
analyze
security
login
logout
whoami
cloud upload
cloud sync
cloud open <id>
cloud delete <id>
```

## One-shot commands

Use direct commands in scripts, CI reproductions or when you already know the action.

```bash
failpack ai --error ./error.log --include-diff
failpack report --github --discord
failpack status
failpack fix v1
failpack unfix v2
failpack doctor
failpack init
failpack clean --yes
```

## Capture options

Tune what gets captured, how much output is preserved and where reports are written.

| Option | Purpose |
| --- | --- |
| `--cmd "npm run build"` | Command to run and capture. |
| `--project ./my-app` | Project directory. |
| `--no-zip` | Skip ZIP bundle creation. |
| `--no-git` | Skip Git context. |
| `--include-source` | Include a limited source snapshot. |
| `--max-log-lines 800` | Keep the last N output lines. |
| `--timeout 600` | Command timeout in seconds. |
| `--output .failpack/reports` | Output directory. |
| `--no-redact` | Disable redaction for local output. |

## Output files

By default, FailPack writes local files to:

```text
.failpack/reports
```

A capture may include:

### `failpack-report.md`

Readable local report for teammates, support or GitHub.

### `failpack-ai-prompt.md`

Prompt-shaped failure context for AI assistants.

### `failpack-context.json`

Structured metadata, logs, Git state and environment signal.

### `failpack-bundle.zip`

Optional portable bundle for private sharing.

## Report status

Each report version has its own status, so fix tracking remains explicit.

```bash
failpack status
failpack fix v1
failpack unfix v2
failpack fix v1 --yes
```

## Cloud and AI

Local commands work without login. Cloud and AI commands require FailPack Cloud and a logged-in account.

Production API builds use:

```text
https://api.failpack.dev/v1
```

AI analysis is available through:

```bash
failpack analyze
failpack security
```

Cloud commands include:

```bash
failpack login
failpack whoami
failpack cloud upload
failpack cloud sync
failpack cloud open <id>
failpack cloud delete <id>
```

## Security model

FailPack is designed to collect debugging context without turning reports into secret dumps.

- Common keys, tokens and credentials are redacted before reports are saved.
- `.env` files and private keys are ignored by default.
- Nothing is uploaded unless you explicitly run or confirm a cloud command.
- Generated reports should be reviewed before sharing.
