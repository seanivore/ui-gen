# Claude Code Infinite UI Setup Guide
*Step-by-step documentation for Sean's reference*

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

## Phase 3: Documentation During Execution

### What to Document
1. **Exact commands used**
2. **Error messages and solutions**
3. **Token usage and costs**
4. **Quality of results**
5. **Interesting themes generated**
6. **Hidden interactions discovered**

### Documentation Template
```markdown
## Batch [NUMBER] - [DATE]
**Command:** [exact command]
**Results:** [number] UIs generated
**Themes:** [list unique themes created]
**Standout Features:** [interesting interactions/animations]
**Issues:** [any problems encountered]
**Cost:** $[amount] ([tokens] tokens)
**Time:** [duration]
```

## Phase 4: Iteration and Optimization

### Potential Variations to Test
1. Different specs (v1, v2, v3)
2. Different batch sizes (3, 5, 10)
3. Different output directories (parallel batches)
4. Custom spec modifications

### Success Metrics
- **Creativity**: Novel themes and interactions
- **Quality**: Professional polish and functionality  
- **Variety**: No repetitive patterns
- **Cost Efficiency**: Value per dollar spent
- **Portfolio Potential**: Showcase-worthy results

## Next Steps
- [ ] Verify custom command setup
- [ ] Run first 3-UI test batch
- [ ] Document results and learnings
- [ ] Analyze themes and interactions
- [ ] Plan next batch parameters

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

## Troubleshooting Notes
*To be filled in during execution*

---
*This guide will be updated as we learn the system*