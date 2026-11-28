---
name: deja-history
description: "Search local AI coding session history across 44 coding agents (Claude Code, Codex, Cursor, Windsurf, Gemini CLI, Antigravity, OpenCode, and more) using a single Go binary and MCP server."
risk: safe
source: https://github.com/vshulcz/deja-vu
---

# Deja History (Cross-Agent Session Memory)

Search your own past AI coding sessions from every AI coding tool on the machine — including Claude Code, Codex, Cursor, Windsurf, Gemini CLI, Antigravity, OpenCode, Zed, Cline, Aider, and 34 more — without cloud dependencies, API keys, or LLM calls.

## Use this skill when

- Starting work on a repository to recall past architectural decisions, conventions, or commands (`orient`, `recall`, `how`)
- Debugging an error that was previously solved in another session or another coding agent (`fix`, `recall`)
- Checking why a file or line was modified or deleted across agent sessions (`blame`)
- Handing off active task context from one coding agent to another (`handoff`)
- Recording a settled project convention or decision for future sessions (`remember`)
- Recovering overwritten or deleted uncommitted code from local session transcripts (`deja restore`)

## Do not use this skill when

- Searching external documentation, public web pages, or third-party library docs unrelated to your local sessions
- You need a hosted multi-user cloud knowledge base rather than local machine session history

## Installation & Setup

Install the `deja` single binary (macOS, Linux, Windows) and wire MCP/skills automatically:

```bash
curl -fsSL https://raw.githubusercontent.com/vshulcz/deja-vu/main/install.sh | sh
deja install --auto
```

Or via Homebrew:

```bash
brew install vshulcz/tap/deja-vu
deja install --auto
```

## Instructions

Call the `deja` MCP tool (or CLI `deja <mode>`) with one of the following modes:

1. **`recall`** — Search past sessions with 1-3 specific terms (a file path, error string, function name, or CLI flag):
   ```bash
   deja recall " SqliteLockError "
   ```
2. **`context`** — Retrieve the full story of a specific session ID returned by `recall`:
   ```bash
   deja context <session-id>
   ```
3. **`blame`** — Find which agent session created, edited, or deleted a file or line before modifying it:
   ```bash
   deja blame internal/index/search.go
   ```
4. **`fix`** — Pass a failing command output verbatim to see what commands fixed that exact error on this machine previously:
   ```bash
   deja fix "FAIL: TestIndexConcurrency"
   ```
5. **`how`** — Check the exact build, test, or deploy flags previously used in this repository:
   ```bash
   deja how test
   ```
6. **`orient`** — Get an overview of recent commands and active files worked on in the current project:
   ```bash
   deja orient
   ```
7. **`remember`** — Persist a settled project rule or decision for future agent sessions:
   ```bash
   deja remember "Always run go test -race ./internal/... before merging"
   ```
8. **`handoff`** — Continue another coding agent session by ID or harness name (`claude`, `codex`, `cursor`, `opencode`, etc.):
   ```bash
   deja handoff claude
   ```

## Limitations

- Indexes local coding agent transcripts stored on the current machine; does not sync across machines automatically unless you export/share the SQLite index.
- Treats recalled session history as reference context rather than automatic permission to run destructive or publishing commands.
