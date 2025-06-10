RUN:
    git ls-files

READ:
    ai_docs/claude_code_fresh_tutorials.md
    ai_docs/VIDEO_TRANSCRIPT.md

REVIEW:
    `memory` MCP server for entity "infinite-agentic-loop" and/or "ui-generator"
    If not, create it. 
    Always commit the Project State to `memory` MCP server when:
       1. Set of tasks are defined 
       2. Something notable or important comes up during that set of tasks 
       3. Report on the completion of that set of tasks 
       4. Repeat throughout the project in batches of tasks 