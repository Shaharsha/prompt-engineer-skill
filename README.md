# prompt-engineer-skill

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent_Skills-compatible-green.svg)](https://agentskills.io)
[![Claude Code](https://img.shields.io/badge/Claude_Code-skill-blueviolet.svg)](https://claude.com/claude-code)

Expert prompt engineering skill for [Claude Code](https://claude.com/claude-code) and any agent supporting the [Agent Skills](https://agentskills.io) standard.

Covers system prompts, tool descriptions, tool response design, context engineering, agentic system design, and cross-provider compatibility across **Claude**, **GPT**, and **Gemini** APIs.

## What's Inside

The skill provides actionable, research-backed guidance for building AI agents:

- **System Prompt Structure** -- role setting, XML tags, few-shot examples, output format
- **Tool Descriptions** -- the 6-element checklist, production patterns from Claude Code, provider-specific guidance
- **Tool Response Design** -- high-signal returns, semantic values, pagination, truncation, actionable errors
- **Context Engineering** -- progressive discovery, semantic identifiers, compaction, grounding
- **Agentic Systems** -- subagent design, state management, autonomy calibration, delegation discipline
- **Provider Differences** -- comparison tables for Claude 4.6, GPT-5, and Gemini 3 (prompting style, reasoning, caching, unique features)
- **Budget Models** -- what changes for Haiku, GPT-5 Mini, Flash
- **Cross-Provider Compatibility** -- safe patterns, must-abstract concerns, non-English output
- **Anti-Patterns** -- 10 common mistakes with explanations
- **Quality Checklist & Testing** -- before-you-ship verification steps
- **Templates** -- contract-style system prompt and structured tool description templates

## Install

### Via Claude Code Plugin Marketplace

```bash
# Add the marketplace (one-time)
claude plugin marketplace add Shaharsha/prompt-engineer-skill

# Install the skill
claude plugin install prompt-engineer@prompt-engineer-marketplace
```

### Manual Install (Personal)

```bash
mkdir -p ~/.claude/skills/prompt-engineer
cp -r skills/prompt-engineer/* ~/.claude/skills/prompt-engineer/
```

### Manual Install (Project)

```bash
mkdir -p .claude/skills/prompt-engineer
cp -r skills/prompt-engineer/* .claude/skills/prompt-engineer/
```

## Usage

The skill activates automatically when you:

- Write or edit system prompts, tool descriptions, or agent instructions
- Discuss prompt quality, tool-use accuracy, or cross-provider compatibility
- Design tool response schemas or agentic workflows

You can also invoke it directly:

```
/prompt-engineer
```

### Example Triggers

- "Improve the system prompt"
- "Write a tool description for search_projects"
- "The agent keeps calling the wrong tool"
- "Make this work on Gemini too"
- "The tool returns too much data"
- "Design the agent context flow"

## File Structure

```
skills/prompt-engineer/
  SKILL.md                              # Main skill (~330 lines)
  templates/
    system-prompt-template.md           # Contract-style system prompt structure
    tool-description-template.md        # Structured tool description format
```

## Research Sources

This skill synthesizes guidance from official provider documentation and production systems:

- [Anthropic: Writing Tools for Agents](https://www.anthropic.com/engineering/writing-tools-for-agents)
- [Anthropic: Effective Context Engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
- [Claude Prompting Best Practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)
- [Anthropic: Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents)
- [Anthropic: Advanced Tool Use](https://www.anthropic.com/engineering/advanced-tool-use)
- [OpenAI: GPT-5 Prompting Guide](https://developers.openai.com/cookbook/examples/gpt-5/gpt-5_prompting_guide)
- [Google: Gemini Prompting Strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies)
- [Claude Code system prompts](https://github.com/Piebald-AI/claude-code-system-prompts) -- tool description patterns, safety architecture, subagent design

## Compatibility

| Platform | Supported |
|----------|-----------|
| Claude Code | Yes |
| Cursor | Yes |
| Gemini CLI | Yes |
| OpenCode | Yes |
| Any Agent Skills-compatible tool | Yes |

## License

[MIT](LICENSE)
