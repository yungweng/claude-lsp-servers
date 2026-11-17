# claude-lsp-servers

LSP plugin for [Claude Code](https://claude.ai/code) — TypeScript, Python, and Go code intelligence that actually works.

## Prerequisites

### 1. Enable LSP Tool

```bash
export ENABLE_LSP_TOOL=1  # Add to your shell profile
```

### 2. Install Language Servers

```bash
# TypeScript/JavaScript
npm install -g typescript-language-server typescript

# Python
npm install -g pyright

# Go
go install golang.org/x/tools/gopls@latest
```

## Installation

```bash
claude plugin marketplace add yonnock/claude-lsp-servers
claude plugin install lsp-servers@claude-lsp-servers
```

Restart Claude Code.

## Verify

Run `/plugin` — you should see `lsp-servers@claude-lsp-servers` without errors.

## Why This Exists

The official LSP plugins are broken ([#15148](https://github.com/anthropics/claude-code/issues/15148)). This is a working alternative.

## Features

| Operation | Description |
|-----------|-------------|
| `hover` | Type info and docs |
| `goToDefinition` | Jump to definitions |
| `findReferences` | Find all usages |
| `documentSymbol` | List symbols in file |
| `goToImplementation` | Find implementations |
| `incomingCalls` | What calls this |
| `outgoingCalls` | What this calls |

## Troubleshooting

**"No LSP server available"** — Set `ENABLE_LSP_TOOL=1` and restart.

**"Executable not found"** — Install the language server binary.

**Debug mode** — `claude --enable-lsp-logging`

## License

MIT
