# Claude Code overview

> Learn about Claude Code, an agentic coding tool made by Anthropic.

Claude Code is an agentic coding tool that lives in your terminal, understands your codebase, and helps you code faster through natural language commands. By integrating directly with your development environment, Claude Code streamlines your workflow without requiring additional servers or complex setup.

```bash
npm install -g @anthropic-ai/claude-code
```

Claude Code's key capabilities include:

* Editing files and fixing bugs across your codebase
* Answering questions about your code's architecture and logic
* Executing and fixing tests, linting, and other commands
* Searching through git history, resolving merge conflicts, and creating commits and PRs
* Browsing documentation and resources from the internet using web search
* Works with [Amazon Bedrock and Google Vertex AI](/en/docs/claude-code/bedrock-vertex-proxies) for enterprise deployments

## Why Claude Code?

Claude Code operates directly in your terminal, understanding your project context and taking real actions. No need to manually add files to context - Claude will explore your codebase as needed.

### Security and privacy by design

Your code's security is paramount. Claude Code's architecture ensures:

* **Direct API connection**: Your queries go straight to Anthropic's API without intermediate servers
* **Works where you work**: Operates directly in your terminal
* **Understands context**: Maintains awareness of your entire project structure
* **Takes action**: Performs real operations like editing files and creating commits

## Quick tour

Here's what you can accomplish with Claude Code:

### From questions to solutions in seconds

```bash
# Ask questions about your codebase
claude
> how does our authentication system work?

# Create a commit with one command
claude commit

# Fix issues across multiple files
claude "fix the type errors in the auth module"
```

### Understand unfamiliar code

```
> what does the payment processing system do?
> find where user permissions are checked
> explain how the caching layer works
```

### Automate Git operations

```
> commit my changes
> create a pr
> which commit added tests for markdown back in December?
> rebase on main and resolve any merge conflicts
```

# Getting started with Claude Code

> Learn how to install, authenticate, and start using Claude Code.

## Check system requirements

* **Operating Systems**: macOS 10.15+, Ubuntu 20.04+/Debian 10+, or Windows via WSL
* **Hardware**: 4GB RAM minimum
* **Software**:
  * Node.js 18+
  * [git](https://git-scm.com/downloads) 2.23+ (optional)
  * [GitHub](https://cli.github.com/) or [GitLab](https://gitlab.com/gitlab-org/cli) CLI for PR workflows (optional)
  * [ripgrep](https://github.com/BurntSushi/ripgrep?tab=readme-ov-file#installation) (rg) for enhanced file search (optional)
* **Network**: Internet connection required for authentication and AI processing
* **Location**: Available only in [supported countries](https://www.anthropic.com/supported-countries)

<Note>
  **Troubleshooting WSL installation**

  Currently, Claude Code does not run directly in Windows, and instead requires WSL. If you encounter issues in WSL:

  1. **OS/platform detection issues**: If you receive an error during installation, WSL may be using Windows `npm`. Try:

     * Run `npm config set os linux` before installation
     * Install with `npm install -g @anthropic-ai/claude-code --force --no-os-check` (Do NOT use `sudo`)

  2. **Node not found errors**: If you see `exec: node: not found` when running `claude`, your WSL environment may be using a Windows installation of Node.js. You can confirm this with `which npm` and `which node`, which should point to Linux paths starting with `/usr/` rather than `/mnt/c/`. To fix this, try installing Node via your Linux distribution's package manager or via [`nvm`](https://github.com/nvm-sh/nvm).
</Note>

## Install and authenticate

<Steps>
  <Step title="Install Claude Code">
    Install [NodeJS 18+](https://nodejs.org/en/download), then run:

    ```sh
    npm install -g @anthropic-ai/claude-code
    ```

    <Warning>
      Do NOT use `sudo npm install -g` as this can lead to permission issues and
      security risks. If you encounter permission errors, see [configure Claude
      Code](/en/docs/claude-code/troubleshooting#linux-permission-issues) for recommended solutions.
    </Warning>
  </Step>

  <Step title="Navigate to your project">
    ```bash
    cd your-project-directory 
    ```
  </Step>

  <Step title="Start Claude Code">
    ```bash
    claude
    ```
  </Step>

  <Step title="Complete authentication">
    Claude Code offers multiple authentication options:

    1. **Anthropic Console**: The default option. Connect through the Anthropic Console and
       complete the OAuth process. Requires active billing at [console.anthropic.com](https://console.anthropic.com).
    2. **Claude App (with Pro or Max plan)**: Subscribe to Claude's [Pro or Max plan](https://www.anthropic.com/pricing) for a unified subscription that includes both Claude Code and the web interface. Get more value at the same price point while managing your account in one place. Log in with your Claude.ai account. During launch, choose the option that matches your subscription type.
    3. **Enterprise platforms**: Configure Claude Code to use
       [Amazon Bedrock or Google Vertex AI](/en/docs/claude-code/bedrock-vertex-proxies)
       for enterprise deployments with your existing cloud infrastructure.
  </Step>
</Steps>

## Initialize your project

For first-time users, we recommend:

<Steps>
  <Step title="Start Claude Code">
    ```bash
    claude
    ```
  </Step>

  <Step title="Run a simple command">
    ```bash
    summarize this project
    ```
  </Step>

  <Step title="Generate a CLAUDE.md project guide">
    ```bash
    /init 
    ```
  </Step>

  <Step title="Commit the generated CLAUDE.md file">
    Ask Claude to commit the generated CLAUDE.md file to your repository.
  </Step>
</Steps>

# Core tasks and workflows

> Explore Claude Code's powerful features for editing, searching, testing, and automating your development workflow.

Claude Code operates directly in your terminal, understanding your project
context and taking real actions. No need to manually add files to context -
Claude will explore your codebase as needed.

## Understand unfamiliar code

```
> what does the payment processing system do?
> find where user permissions are checked
> explain how the caching layer works
```

## Automate Git operations

```
> commit my changes
> create a pr
> which commit added tests for markdown back in December?
> rebase on main and resolve any merge conflicts
```

## Edit code intelligently

```
> add input validation to the signup form
> refactor the logger to use the new API
> fix the race condition in the worker queue
```

## Test and debug your code

```
> run tests for the auth module and fix failures
> find and fix security vulnerabilities
> explain why this test is failing
```

## Encourage deeper thinking

For complex problems, explicitly ask Claude to think more deeply:

```
> think about how we should architect the new payment service
> think hard about the edge cases in our authentication flow
```

Claude Code will show when the model is using extended thinking. You can
proactively prompt Claude to "think" or "think deeply" for more
planning-intensive tasks. We suggest that you first tell Claude about your task
and let it gather context from your project. Then, ask it to "think" to create a
plan.

<Tip>
  Claude will think more based on the words you use. For example, "think hard" will trigger more extended thinking than saying "think" alone.

  For more tips, see
  [Extended thinking tips](/en/docs/build-with-claude/prompt-engineering/extended-thinking-tips).
</Tip>

## Automate CI and infra workflows

Claude Code comes with a non-interactive mode for headless execution. This is
especially useful for running Claude Code in non-interactive contexts like
scripts, pipelines, and Github Actions.

Use `--print` (`-p`) to run Claude in non-interactive mode. In this mode, you
can set the `ANTHROPIC_API_KEY` environment variable to provide a custom API
key.

Non-interactive mode is especially useful when you pre-configure the set of
commands Claude is allowed to use:

```sh
export ANTHROPIC_API_KEY=sk_...
claude -p "update the README with the latest changes" --allowedTools "Bash(git diff:*)" "Bash(git log:*)" Write --disallowedTools ...
```
