---
title: "Biting the AI Coding bullet"
date: 2026-03-14T11:34:15+05:30
draft: false
pinned: false
summary: "AI skeptic's guide to starting with AI assisted coding tools"
tags: ["Software Engineering"]
---

We're told every once in a while by Anthropic that almost all code will be written by AI in the next 6 months. Honestly how Dario Amodei has any credibility left is beyond me. Just because you have a power drill in place of a hammer doesn't mean that it's capable of building a cabinet by itself. The task of building the cabinet still requires a carpenter.

That said, familiarizing myself with the new brand of power tools seems obvious now that the models seem to have gotten to a level where they don't generate garbage all the time. It's like any other technology, either you move with time or you get left behind.

From my initial research getting up to speed on AI coding tools boils down to 3 things.

**Step 1:** Figuring out which model fits well for different tasks whether it's based on modality. The general wisdom on the Internet seems to be using a bunch of models in tandem depending on the task. For general purpose coding a cheaper model can be used whereas a more expensive reasoning model can be used for planning tasks and code review.

1. **Kimi K2.5** - Claude Sonnet for cheapskates like me. This could be my main workhorse as its the model that's actually affordable at API rates (approximately 3–5 times cheaper than comparable offerings from Anthropic & OpenAI )
3. **GPT 5.3 Codex** - Leading edge model by OpenAI for coding tasks. Quite expensive so I am going to use this for more complex coding tasks and planning.

**Step 2:** Selecting the harness that works best for me i.e. the actual tool  around the LLM that interacts with your IDE, OS, Filesystem, Git etc. Broadly there are two UX options here, the AI chat side panel integrated into your IDE and the Terminal based UI tools. I don't really find the side panel approach intuitive. Hence I decided to go for the terminal route.

1. **OpenCode** emerged as the obvious choice for personal usage primarily due to it being open source and compatible with almost all LLM providers therefore preventing vendor lock-in. It also comes with Plan/Build mode loop which I plan to use to delegate tasks between different models, support for custom skills, and MCP servers. Other good alternatives from leading companies are Claude Code from Anthropic, Codex from OpenAI and Gemini CLI from Google. 
2. **GitHub Copilot** because thats just what I have to use at work🤦‍♀

**Step 3**: Managing context efficiently via steering docs becomes essential for large codebases so some thought has to be given to [AGENTS.md](http://agents.md/). An interesting idea I came across is using Mermaid diagrams to encode complex app knowledge into your agent docs. Multiple markdown files organized by functional modules can be linked in the AGENTS.md file to allow for progressive disclosure of information to the agent and not overwhelm the agent's context window.

Another use case could be using [Agent Skills](https://agentskills.io/what-are-skills). These are collections of reusable prompts that assist the agent in domain-specific tasks. Optionally they may include bash / python scripts that the agent can execute to complete the task at hand. For all the hype MCP gets, Agent skills is a more efficient way to inject custom knowledge into coding agents. This is because Agent skills are loaded on demand by the agent whereas MCP loads all tools at the beginning itself filling up the context window unnecessarily.

Vercel hosts an open directory of skills developed in open source - https://skills.sh/ 

Resources I found to be extremely useful -

1. [AI Assisted Development Course by Anthony Alicea](https://dontimitate.dev/courses/ai-assisted-development/) 
2. [OpenCode Documentation](https://opencode.ai/docs)
3. [Steering Agents](https://dev.to/datadog-frontend-dev/steering-ai-agents-in-monorepos-with-agentsmd-13g0)
