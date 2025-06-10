# Infinite Agentic Loop POC

  - SOURCE: [IndyDevDan Youtube Tutorial](https://youtu.be/9ipM_vDwflI)
  - VIDEO TRANSCRIPT: [Infinite Agentic Loop with Claude Code](ai_docs/VIDEO_TRANSCRIPT.md)

## Overview

- An experimental project demonstrating Infinite Agentic Loop in a two prompt system using Claude Code.
- This project uses a custom Claude Code slash command (`/project:infinite`) 
  - Orchestrate multiple AI agents in parallel 
  - Generating evolving iterations of content based on specifications 

## Quick Start 

1. Read `.claude/settings.json` to see the permissions and commands allowed.
2. Start Claude Code. 
3. Type slash command to start the infinite agentic loop. 
4. Generate new iterations using the UI specification and four command variants.

```bash
claude
/project:infinite
/project:infinite spec_file output_dir count # Infinite command takes three arguments 
```

### Four Command Variants

```bash
/project:infinite specs/invent_new_ui_v3.md src 1 # Single Generation of 1 iteration
/project:infinite specs/invent_new_ui_v3.md src_new 5 # Deploy 5 agents in parallel; generate 5 UI
/project:infinite specs/invent_new_ui_v3.md src_new 20 # 20 agents, groups of 5, optimal resource management, generate 20 UI
/project:infinite specs/invent_new_ui_v3.md infinite_src_new/ infinite # Continuous generation, stops with context limits 
```

## How It Works

1. **Specification Analysis**: Reads and understands the spec file requirements
2. **Directory Reconnaissance**: Analyzes existing iterations to determine starting point
3. **Parallel Coordination**: Deploys Sub Agents with unique creative directions
4. **Quality Assurance**: Ensures each iteration is unique and spec-compliant
5. **Wave Management**: For infinite mode, manages successive waves of agents

## Ideas for Enhancing the Pattern 

- Apply this to a use case of your choice.
- Build an MCP Server that enables reuse of the infinite agentic loop.
- Get the `.claude/commands/infinite.md` into your `~/.claude/commands/` directory for global use.
- Update `.claude/commands/infinite.md` to generate sets of files instead of a single file.
