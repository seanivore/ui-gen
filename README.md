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


## Project Overview
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

## Phase 1: Setup Verification ✅

### Step 1: Check Custom Command Setup
1. Navigate to project directory:
   ```bash
   cd /Users/seanivore/Development/infinite-ui-gen/
   ```

2. Verify `.claude/commands/infinite.md` exists and is properly formatted

3. Check `.claude/settings.json` permissions are set

### Step 2: Test Claude Code Connection
1. Start Claude Code:
   ```bash
   claude
   ```

2. Test if custom command is recognized:
   ```
   /project:infinite
   ```
   *(Should show command help or prompt for arguments)*

## Phase 2: First Test Batch (3 iOS-Style UIs)

### iOS App Interface Focus
Since MAO will likely launch as an iOS app for non-tech users, we're focusing on mobile app interface components rather than web components.

### Command Structure
```bash
/project:infinite [spec_file] [output_dir] [count]
```

### Test Run Command
```bash
/project:infinite specs/ios_ui_spec.md src_agent_1 3
```

**Arguments Explained:**
- `specs/ios_ui_spec.md` = Our iOS-focused themed hybrid spec
- `src_agent_1` = Output directory for this batch
- `3` = Generate 3 UIs in parallel

### Expected Results
- 3 HTML files simulating iOS app interfaces in `src_agent_1/` directory
- Each with unique theme (e.g., "Neural Interface Controller", "Quantum Task Manager", "Bioelectric Communication Hub")
- Mobile-first responsive design with app-like interactions
- Self-contained with CSS, JavaScript, and touch-friendly elements
- Total cost: ~$1.35 (3 × $0.45)
- Total time: ~6-9 minutes

## Commands Reference
```bash
# Start Claude Code
claude

# Basic infinite command
/project:infinite specs/invent_new_ui_v3.md src_agent_1 3

# Check command help
/project:infinite --help

# Exit Claude Code
exit
```
