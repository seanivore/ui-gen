# Claude Code Infinite Agentic UI Generation

  - SOURCE: [IndyDevDan Youtube Tutorial](https://youtu.be/9ipM_vDwflI)
  - CLAUDE CODE CLI: [CLAUDE_CODE_CLI.md](ai_docs/CLAUDE_CODE_CLI.md)

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

## This Project 
- **Goal**: Generate 3-30+ unique themed UI components using parallel subagents
- **Cost**: ~30k tokens per UI (~$0.45 each) 
- **Time**: 2-3 minutes per UI
- **Method**: Controlled batches (not infinite looping)

## Current Project Structure
```
/Users/seanivore/Development/infinite-ui-gen/
├── .claude/
│   ├── commands/
│   │   ├── infinite.md     # ← Custom command (needs setup)
│   │   └── prime.md        # ← Context priming
│   └── settings.json       # ← Permissions config
├── specs/
│   └── ios_ui_spec.md # Themed iOS UI spec 
├── src_agent_1/            # ← Output directory (empty, ready)
├── src_agent_2/            # ← Output directory (empty, ready)
├── src_agent_3/            # ← Output directory (empty, ready)
└── src_agent_4/            # ← Output directory (empty, ready)
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