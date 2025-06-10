# CLI usage and controls

> Learn how to use Claude Code from the command line, including CLI commands, flags, and slash commands.

## Getting started

Claude Code provides two main ways to interact:

* **Interactive mode**: Run `claude` to start a REPL session
* **One-shot mode**: Use `claude -p "query"` for quick commands

```bash
# Start interactive mode
claude

# Start with an initial query
claude "explain this project"

# Run a single command and exit
claude -p "what does this function do?"

# Process piped content
cat logs.txt | claude -p "analyze these errors"
```

## CLI commands

| Command                            | Description                    | Example                                |
| :--------------------------------- | :----------------------------- | :------------------------------------- |
| `claude`                           | Start interactive REPL         | `claude`                               |
| `claude "query"`                   | Start REPL with initial prompt | `claude "explain this project"`        |
| `claude -p "query"`                | Run one-off query, then exit   | `claude -p "explain this function"`    |
| `cat file \| claude -p "query"`    | Process piped content          | `cat logs.txt \| claude -p "explain"`  |
| `claude -c`                        | Continue recent conversation   | `claude -c`                            |
| `claude -c -p "query"`             | Continue in print mode         | `claude -c -p "Check for type errors"` |
| `claude -r "<session-id>" "query"` | Resume session by ID           | `claude -r "abc123" "Finish this PR"`  |
| `claude update`                    | Update to latest version       | `claude update`                        |
| `claude mcp`                       | Configure MCP servers          |                                        |

## CLI flags

Customize Claude Code's behavior with these command-line flags:

| Flag                             | Description                                    | Example                                                    |
| :------------------------------- | :--------------------------------------------- | :--------------------------------------------------------- |
| `--allowedTools`                 | Tools allowed without permission               | `"Bash(git log:*)" "Bash(git diff:*)" "Write"`             |
| `--disallowedTools`              | Tools disallowed without permission            | `"Bash(git log:*)" "Bash(git diff:*)" "Write"`             |
| `--print`, `-p`                  | Print response without interactive mode        | `claude -p "query"`                                        |
| `--output-format`                | Print format (`text`, `json`, `stream-json`)   | `claude -p "query" --output-format json`                   |
| `--verbose`                      | Enable verbose turn-by-turn debugging output   | `claude --verbose`                                         |
| `--max-turns`                    | Limit agentic turns in non-interactive mode    | `claude -p --max-turns 3 "query"`                          |
| `--model`                        | Set session model via alias `sonnet` or `opus` | `claude --model claude-sonnet-4-20250514`                  |
| `--permission-prompt-tool`       | MCP tool to handle permission prompts          | `claude -p --permission-prompt-tool mcp_auth_tool "query"` |
| `--resume`                       | Resume specific session by ID                  | `claude --resume abc123 "query"`                           |
| `--continue`                     | Load most recent conversation                  | `claude --continue`                                        |
| `--dangerously-skip-permissions` | Skip permission prompts                        | `claude --dangerously-skip-permissions`                    |

<Tip>
  The `--output-format json` flag is particularly useful for scripting and
  automation, allowing you to parse Claude's responses programmatically.
</Tip>

For detailed information about print mode (`-p`) including output formats,
streaming, verbose logging, and programmatic usage, see the
[SDK documentation](./CLAUDE_CODE_SDK.md). 

## Slash commands

Control Claude's behavior during an interactive session:

| Command                   | Purpose                                                 |
| :------------------------ | :------------------------------------------------------ |
| `/bug`                    | Report bugs (sends conversation to Anthropic)           |
| `/clear`                  | Clear conversation history                              |
| `/compact [instructions]` | Compact conversation with optional focus instructions   |
| `/config`                 | View/modify configuration                               |
| `/cost`                   | Show token usage statistics                             |
| `/doctor`                 | Checks the health of your Claude Code installation      |
| `/help`                   | Get usage help                                          |
| `/init`                   | Initialize project with CLAUDE.md guide                 |
| `/login`                  | Switch Anthropic accounts                               |
| `/logout`                 | Sign out from your Anthropic account                    |
| `/memory`                 | Edit CLAUDE.md memory files                             |
| `/model`                  | Select or change the AI model                           |
| `/permissions`            | View or update permissions                              |
| `/pr_comments`            | View pull request comments                              |
| `/review`                 | Request code review                                     |
| `/status`                 | View account and system statuses                        |
| `/vim`                    | Enter vim mode for alternating insert and command modes |

## Special shortcuts

### Quick memory with `#`

Add memories instantly by starting your input with `#`:

```
# Always use descriptive variable names
```

You'll be prompted to select which memory file to store this in.

### Line breaks in terminal

Enter multiline commands using:

* **Quick escape**: Type `\` followed by Enter
* **Keyboard shortcut**: Option+Enter (or Shift+Enter if configured)

To set up Option+Enter in your terminal:

**For Mac Terminal.app:**

1. Open Settings → Profiles → Keyboard
2. Check "Use Option as Meta Key"

**For iTerm2 and VSCode terminal:**

1. Open Settings → Profiles → Keys
2. Under General, set Left/Right Option key to "Esc+"

**Tip for iTerm2 and VSCode users**: Run `/terminal-setup` within Claude Code to
automatically configure Shift+Enter as a more intuitive alternative.

See [terminal setup in settings](/en/docs/claude-code/settings#line-breaks) for
configuration details.

## Vim Mode

Claude Code supports a subset of Vim keybindings that can be enabled with `/vim`
or configured via `/config`.

The supported subset includes:

* Mode switching: `Esc` (to NORMAL), `i`/`I`, `a`/`A`, `o`/`O` (to INSERT)
* Navigation: `h`/`j`/`k`/`l`, `w`/`e`/`b`, `0`/`$`/`^`, `gg`/`G`
* Editing: `x`, `dw`/`de`/`db`/`dd`/`D`, `cw`/`ce`/`cb`/`cc`/`C`, `.` (repeat)
