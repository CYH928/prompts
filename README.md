# Prompts for Harness Agents

Global prompts / settings for coding-agent harnesses (Claude Code, OpenCode).

## Structure

```
.
├── claude/
│   └── CLAUDE.md      # Claude Code global instructions (template, personal info left blank)
└── opencode/
    ├── AGENTS.md      # OpenCode global instructions
    └── cli.json       # OpenCode CLI/TUI settings (theme, session, tabs, diffs, notifications)
```

Shared conventions across the prompts:

- Reply language: zh-Hant; short, key-point answers to save tokens
- Discuss options (with pros/cons + recommendation) before deciding or acting
- Ask when unclear; don't guess; use web search for up-to-date info
- No dangerous actions without consent; summarize what was done on completion
- Loop: plan → discuss → code → test (V&V, code-review, Playwright for web UI) → commit/push (consent required)

## Usage

1. Copy the file to the harness's global config location.
   - Claude Code: `claude/CLAUDE.md` → `~/.claude/CLAUDE.md`
   - OpenCode: `opencode/AGENTS.md` and `opencode/cli.json` → your OpenCode config directory
2. Edit the **Role** section (name, email, role) and tools/MCPs to fit your setup.
3. Restart the harness so the changes are loaded.

## Privacy

`claude/CLAUDE.md` is a template with placeholders (`XXX`). Do **not** commit real personal details (name, birth date, email, etc.) to this repo, especially if it is or may become public. Keep your filled-in copy only in your local config directory.
