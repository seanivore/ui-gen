# Claude Code Infinite Agentic UI Generation

  - SOURCE: [IndyDevDan Youtube Tutorial](https://youtu.be/9ipM_vDwflI)
  - CLAUDE CODE CLI: [CLAUDE_CODE_CLI.md](ai_docs/CLAUDE_CODE_CLI.md)

## Overview

- Project utilizing Claude Code's Infinite Agentic Loop 
- Uses a two prompt system, to orchestrator and to agents 
  - Carefully defined SPEC files defining best practices 
  - A custom Claude Code slash command (`/project:infinite`) 
    - Orchestrate multiple AI agents in parallel 
    - Generating evolving iterations of content based on specifications 

### Quick Start 

1. Confirm permissions allowed in `.claude/settings.json` file 
2. Start Claude Code by running `claude` in the terminal
3. Confirm that the project structure reflects the structure below 
4. Claude Code recognizes the custom command from the `.claude/commands/infinite.md` file 
5. Type slash custom command to start the infinite agentic loop
6. Add specifics to the command and generate new iterations  

```bash
claude
/project:infinite
/project:infinite spec_file output_dir count # Infinite command takes three arguments 
```

### Command Variants

```bash
/project:infinite specs/invent_new_ui_v3.md src 1 # Single Generation of 1 iteration
/project:infinite specs/invent_new_ui_v3.md src_new 5 # Deploy 5 agents in parallel; generate 5 UI
/project:infinite specs/invent_new_ui_v3.md src_new 20 # 20 agents, groups of 5, optimal resource management, generate 20 UI
/project:infinite specs/invent_new_ui_v3.md infinite_src_new/ infinite # Continuous generation, stops with context limits 
```

### Project Structure

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

## This Project 

- **Goal**: Generate 50+ unique themed UI components 
- **Cost**: 30k tokens per UI (~$0.45 each) 
- **Time**: 2-3 minutes per UI 

## How It Works

1. **Specification Analysis**: Reads and understands the spec file requirements
2. **Directory Reconnaissance**: Analyzes existing iterations to determine starting point
3. **Parallel Coordination**: Deploys Sub Agents with unique creative directions
4. **Quality Assurance**: Ensures each iteration is unique and spec-compliant
5. **Wave Management**: For infinite mode, manages successive waves of agents

### Just use the command, define the spec, the output directory, and the number of iterations you want to generate. That's it. 