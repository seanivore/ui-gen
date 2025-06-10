# Master Task List 
For human to keep track of the project and to introduce the project to Claude to help me complete the tutorial and understand everything. 

## Infinite Agentic Loop with UI Generator 

- README.md `/Users/seanivore/Development/infinite-ui-gen/README.md` 
- Claude Code Context Prime `/Users/seanivore/Development/infinite-ui-gen/.claude/commands/prime.md` 
- Infinite Agentic Loop Claude Code Command `/Users/seanivore/Development/infinite-ui-gen/.claude/commands/infinite.md`
- Tutorial Video Transcript `/Users/seanivore/Development/infinite-ui-gen/ai_docs/VIDEO_TRANSCRIPT.md` 
- Specs `/Users/seanivore/Development/infinite-ui-gen/specs/` 
  - "UI Component Innovation Specification" `/Users/seanivore/Development/infinite-ui-gen/specs/invent_new_ui_v1.md` 
  - "Practical UI Component Enhancement Specification" `/Users/seanivore/Development/infinite-ui-gen/specs/invent_new_ui_v2.md` 
  - "Themed Hybrid UI Component Specification" `/Users/seanivore/Development/infinite-ui-gen/specs/invent_new_ui_v3.md` 

### Tutorial HTML File Results 

- ROUND 1: 
  - 'Innovation' SPEC-v1 `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/html_batch_1/src` (10 files)
  - 'Enhanced' SPEC-v2 `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/html_batch_1/src_enhanced` (10 files)
  - 'Themed Hybrid' SPEC-v3 `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/html_batch_1/themed_hybrid_all` (15 files)

- ROUND 2: 
  - 'Hybrid' batch-1 `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/html_batch_2/src` (35 files)
  - 'Hybrid' batch-2 `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/html_batch_2/src_infinite` (25 files)

### Tutorial Video Screenshots of UI Examples 

- infinite_ui_gen_1.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_1.png`
- infinite_ui_gen_2.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_2.png`
- infinite_ui_gen_3.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_3.png`
- infinite_ui_gen_4.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_4.png`
- infinite_ui_gen_5.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_5.png`
- infinite_ui_gen_6.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_6.png`
- infinite_ui_gen_7.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_7.png`
- infinite_ui_gen_8.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_8.png`
- infinite_ui_gen_9.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_9.png`
- infinite_ui_gen_10.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_10.png`
- infinite_ui_gen_11.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_11.png`
- infinite_ui_gen_12.png: `/Users/seanivore/Development/infinite-ui-gen/examples-from-tutorial/ui_screenshots/infinite_ui_gen_12.png`

## Tutorial Review 

- The examples from the tutorial look really great
- They're all interactive and have engaging animations 
- Concepts are created on the fly by the AI 
- Here and there there was a sort of 'meh' UI generated 
- But even in the 'meh' UI you could find unique little elements 

### Doing The Tutorial  

1. Try to figure out which spec prompt he used for the visuals he used in the videos. 
   - I'm assuming 'Themed Hybrid' SPEC-v3, but am curious if he tweaked anything 
   - Keep our eyes peeled for ways that we might be able to improve results of subsequent iterations 
2. I'm honestly not even that interested in the idea of "infinite" looping 
   - I'd rather run a controlled number in a batch 
   - Then there is room to make improvements as needed 
   - The idea of "infinity" is interesting I guess, but seems sort of not helpful 

### Recreation Plan 

- Do the tutorial 
- Create a bunch of iterations of UI components 
- Publish them as a new portfolio section 
- Be open about the fact that they're created by AI in parallel 
- Sort of like split-testing but with AI design/development 

## Claude Code Usage Calculations 

### API Cost 

- $15/million tokens 
- Each UI took 2-4 minutes to generate 
- They each used ~30,000 tokens 
- 1 million tokens / 30,000 tokens = 33.33 iterations aka about 33 UI web pages  

### Claude Pro Subscription 
[Claude Code with Claude Pro Subscription](https://support.anthropic.com/en/articles/11145838-using-claude-code-with-your-pro-or-max-plan) 

- Claude Pro subscription comes with "10-40 Claude Code prompts"
- Rate limit is shared between both Claude Pro and Claude Code 
  - Average users can send approximately 45 messages with Claude every 5 hours 
  - OR send approximately 10-40 prompts with Claude Code every 5 hours
- Pro plan subscribers can access Sonnet 4, but **won’t be able to use Opus 4** with Claude Code

## Project Usage Plan 

- Tutorial creates iterations of UI components 
  - Re: Opus 4, the tutorial uses Opus 4 
  - Let's try Sonnet 4 for a first batch of iterations
  - Then switch to my API key for batches of Opus 4 iterations 

1. See how many iterations we can get out of the Pro subscription in the token limit and rate limit 
2. The move to the API and create more iterations according to how many were already created and their quality 

## Arguments for Running Tutorial Commands 

Output directories `output_dir`:
- /Users/seanivore/Development/infinite-ui-gen/src_agent_1
- /Users/seanivore/Development/infinite-ui-gen/src_agent_2
- /Users/seanivore/Development/infinite-ui-gen/src_agent_3
- /Users/seanivore/Development/infinite-ui-gen/src_agent_4

Spec files `spec_file`: 
- /Users/seanivore/Development/infinite-ui-gen/specs/invent_new_ui_v1.md
- /Users/seanivore/Development/infinite-ui-gen/specs/invent_new_ui_v2.md
- /Users/seanivore/Development/infinite-ui-gen/specs/invent_new_ui_v3.md



## Project Structure 

```
├── ai_docs
│   ├── claude_code_fresh_tutorials.md
│   └── VIDEO_TRANSCRIPT.md   <-- "Watch" the tutorial here 
├── claude
│   ├── commands
│   │   ├── infinite.md   <-- I think needs be be made a command or something? see readme.md 
│   │   └── prime.md    <-- For Claude Code 
│   ├── MASTER_TASK_LIST.md 
│   └── settings.json <-- telling Claude Code they don't need to ask permission 
├── examples-from-tutorial
│   ├── html_batch_1    <-- not as nice as the final batch 
│   │   ├── src
│   │   ├── src_enhanced
│   │   └── themed_hybrid_all
│   ├── html_batch_2    <-- only final batch and SPEC-v3 is really great 
│   │   ├── src
│   │   └── src_infinite    <-- Presumably the batch in the video 
│   └── ui_screenshots
├── mock_data.txt    <-- Maybe you are able to see he mentioned this somewhere? I have not. 
├── README.md     <-- Most detailed overview of how to do the tutorial 
├── src_agent_1    <-- New directories for each subagent
├── src_agent_2
├── src_agent_3
├── src_agent_4
└── specs
    ├── invent_new_ui_v1.md
    ├── invent_new_ui_v2.md
    └── invent_new_ui_v3.md    <-- Presumably the best spec file used in the video 
```