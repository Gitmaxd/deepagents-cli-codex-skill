# Deep Agents CLI Skill

An OpenAI Codex Skill providing comprehensive reference documentation for the [LangChain Deep Agents CLI](https://docs.langchain.com/oss/python/deepagents/overview).

## What This Skill Does

Gives Codex structured, on-demand knowledge of the Deep Agents CLI — commands, flags, providers, skills, memory, sandboxes, streaming, SDK customization, and workflows.

Codex loads this skill automatically when relevant, or you can invoke it directly with `$deepagents-cli`.

## Skill Contents

| File | Topic |
|------|-------|
| `SKILL.md` | Entry point — overview, quick start, core concepts |
| `references/cli-reference.md` | Complete CLI commands, flags, keyboard shortcuts |
| `references/providers.md` | 20+ LLM providers, config.toml schema |
| `references/skills-system.md` | Skills creation, SKILL.md format |
| `references/memory-and-persistence.md` | Memory system, AGENTS.md |
| `references/sandboxes.md` | Modal, Runloop, Daytona, LangSmith |
| `references/sdk-customization.md` | create_deep_agent(), middleware, subagents |
| `references/streaming.md` | Streaming modes, frontend integration |
| `references/acp.md` | Agent Client Protocol, editor integrations |
| `references/workflows.md` | Automation, CI/CD patterns |

## Links

- **npm:** [deepagents-cli-codex-skill](https://www.npmjs.com/package/deepagents-cli-codex-skill)
- **GitHub:** [Gitmaxd/deepagents-cli-codex-skill](https://github.com/Gitmaxd/deepagents-cli-codex-skill)
- **Deep Agents Docs:** [docs.langchain.com](https://docs.langchain.com/oss/python/deepagents/overview)
- **Agent Skills Standard:** [agentskills.io](https://agentskills.io/)

## License

MIT
