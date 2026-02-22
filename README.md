<div align="center">

# deepagents-cli-codex-skill

**An OpenAI Codex Skill for the LangChain Deep Agents CLI**

[![npm version](https://img.shields.io/npm/v/deepagents-cli-codex-skill.svg)](https://www.npmjs.com/package/deepagents-cli-codex-skill)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-%3E%3D18-green.svg)](https://nodejs.org/)
[![npm downloads](https://img.shields.io/npm/dm/deepagents-cli-codex-skill.svg)](https://www.npmjs.com/package/deepagents-cli-codex-skill)

Scaffold a production-grade Codex Skill that gives OpenAI Codex comprehensive, structured knowledge of the Deep Agents CLI — commands, providers, memory, sandboxes, streaming, and SDK customization.

[Installation](#installation) · [What Gets Installed](#what-gets-installed) · [Skill Resources](#skill-resources) · [Official Documentation](#official-documentation)

</div>

---

## Overview

The Deep Agents CLI is LangChain's terminal coding agent — a LangGraph-powered assistant with persistent memory, 20+ LLM provider integrations, sandboxed code execution, and a composable skills system. Its surface area spans interactive and non-interactive modes, a rich slash-command REPL, programmatic SDK customization, streaming output, and the Agent Client Protocol for editor integration.

This package scaffolds an [OpenAI Codex Skill](https://developers.openai.com/codex/skills) that encodes that entire surface area as structured, on-demand knowledge. When the skill is active, Codex can accurately assist with any Deep Agents CLI task — from launching a first session to building production subagent pipelines — without requiring repeated context or pasted documentation.

The skill follows the [Agent Skills open standard](https://agentskills.io/) and loads automatically when relevant. It can also be invoked directly with `$deepagents-cli`.

---

## Installation

### Workspace (recommended)

Installs the skill into the current project's `.agents/skills/` directory. Check it into version control to share it with your team.

```bash
npx deepagents-cli-codex-skill init
```

### Personal

Installs the skill to `~/.agents/skills/` so it is available across all projects on your machine.

```bash
npx deepagents-cli-codex-skill init --personal
```

### Alternative: `$skill-installer`

If you prefer to install from within Codex, you can use the built-in skill installer after placing the skill files in a known location:

```
$skill-installer install deepagents-cli
```

### Options

| Flag | Description | Default |
|------|-------------|---------|
| `--personal` | Install to `~/.agents/skills/` (personal scope) | `false` |
| `--path <dir>` | Target directory for workspace installation | Current directory |
| `--force` | Skip confirmation when skill directory already exists | `false` |
| `--help` | Show usage information | — |
| `--version` | Show installed version | — |

### Updating

To update the skill after a new release, re-run the init command. Existing files are never overwritten; only files added in the new release will be created.

---

## What Gets Installed

```
.agents/skills/deepagents-cli/
├── SKILL.md                        Main skill definition and quick-start reference
└── references/
    ├── cli-reference.md            Complete CLI commands, flags, and keyboard shortcuts
    ├── providers.md                LLM provider configuration and config.toml schema
    ├── skills-system.md            Skills creation, SKILL.md format, progressive disclosure
    ├── memory-and-persistence.md   Memory system, AGENTS.md, SDK long-term memory
    ├── sandboxes.md                Sandbox providers: Modal, Runloop, Daytona, LangSmith
    ├── sdk-customization.md        create_deep_agent(), middleware, subagents, backends, HITL
    ├── streaming.md                Streaming modes, subgraph streaming, frontend integration
    ├── acp.md                      Agent Client Protocol and editor integrations
    └── workflows.md                Automation patterns, CI/CD, troubleshooting
```

The skill follows the [Agent Skills progressive disclosure model](https://agentskills.io/specification#progressive-disclosure): `SKILL.md` is the primary context loaded by Codex, and the reference files are surfaced on-demand as the task requires them. This keeps the token footprint minimal while making the full surface area available.

---

## Skill Resources

Each reference file is a structured knowledge document scoped to a specific area of the Deep Agents CLI. All content is sourced from the [official LangChain Deep Agents documentation](https://docs.langchain.com/oss/python/deepagents/overview) and aligned with the documented API.

### SKILL.md

**Purpose:** Entry point for the skill. Contains a concise overview, quick-start examples, core concept summaries, and links to all reference files.

**Value:** Codex reads this file first when the skill is activated. It provides enough context to handle the most common tasks immediately and directs Codex to the appropriate reference file for deeper questions, keeping initial token usage minimal.

---

### CLI Reference

**File:** `references/cli-reference.md`
**Source:** [CLI Overview](https://docs.langchain.com/oss/python/deepagents/cli/overview)

Complete reference for every command, flag, slash command, and keyboard shortcut in the Deep Agents CLI.

---

### Providers and Models

**File:** `references/providers.md`
**Source:** [Model Providers](https://docs.langchain.com/oss/python/deepagents/cli/providers)

Configuration reference for all 20+ supported LLM providers.

---

### Skills System

**File:** `references/skills-system.md`
**Source:** [Skills](https://docs.langchain.com/oss/python/deepagents/skills)

Detailed guide to the Deep Agents skills system.

---

### Memory and Persistence

**File:** `references/memory-and-persistence.md`
**Source:** [Long-term Memory](https://docs.langchain.com/oss/python/deepagents/long-term-memory)

Covers both layers of the Deep Agents memory system.

---

### Sandboxes

**File:** `references/sandboxes.md`
**Source:** [Sandboxes](https://docs.langchain.com/oss/python/deepagents/sandboxes)

Setup and configuration guide for all four supported sandbox providers.

---

### SDK Customization

**File:** `references/sdk-customization.md`
**Sources:** [Customization](https://docs.langchain.com/oss/python/deepagents/customization), [Subagents](https://docs.langchain.com/oss/python/deepagents/subagents), [Backends](https://docs.langchain.com/oss/python/deepagents/backends), [Human-in-the-Loop](https://docs.langchain.com/oss/python/deepagents/human-in-the-loop), [Middleware](https://docs.langchain.com/oss/python/deepagents/middleware)

Programmatic usage of the Deep Agents SDK via `create_deep_agent()`.

---

### Streaming

**File:** `references/streaming.md`
**Sources:** [Streaming Overview](https://docs.langchain.com/oss/python/deepagents/streaming/overview), [Streaming Frontend](https://docs.langchain.com/oss/python/deepagents/streaming/frontend)

Streaming output reference for both CLI and SDK usage.

---

### Agent Client Protocol

**File:** `references/acp.md`
**Source:** [Agent Client Protocol](https://docs.langchain.com/oss/python/deepagents/acp)

Reference for the Agent Client Protocol (ACP).

---

### Workflows and Patterns

**File:** `references/workflows.md`

Practical reference for automation and scripted usage.

---

## Agent Skills Compliance

This skill is built to the [Agent Skills open standard](https://agentskills.io/specification) and the [Codex Skills specification](https://developers.openai.com/codex/skills):

| Requirement | Implementation |
|-------------|----------------|
| `SKILL.md` with YAML frontmatter | `name`, `description`, and `compatibility` fields present; description written for accurate auto-invocation matching |
| Narrow, outcome-focused scope | Skill scoped entirely to Deep Agents CLI knowledge; single domain, single responsibility |
| Co-located supporting files | `references/` directory co-located with `SKILL.md` inside the skill directory |
| Progressive disclosure | `SKILL.md` is the primary context under 500 lines; reference files are loaded on-demand by topic |
| Flexible invocation | Codex loads the skill automatically when relevant; user can also invoke with `$deepagents-cli` |
| Personal and workspace scopes | `--personal` targets `~/.agents/skills/`; default targets `<project>/.agents/skills/` |
| Never overwrites existing files | The installer skips any file that already exists at the target path |

---

## Official Documentation

All technical content in this skill is sourced from and cross-referenced against the official LangChain Deep Agents documentation:

| Topic | URL |
|-------|-----|
| Deep Agents Overview | https://docs.langchain.com/oss/python/deepagents/overview |
| Quickstart | https://docs.langchain.com/oss/python/deepagents/quickstart |
| CLI Overview | https://docs.langchain.com/oss/python/deepagents/cli/overview |
| Model Providers | https://docs.langchain.com/oss/python/deepagents/cli/providers |
| Customization | https://docs.langchain.com/oss/python/deepagents/customization |
| Harness Capabilities | https://docs.langchain.com/oss/python/deepagents/harness |
| Backends | https://docs.langchain.com/oss/python/deepagents/backends |
| Subagents | https://docs.langchain.com/oss/python/deepagents/subagents |
| Human-in-the-Loop | https://docs.langchain.com/oss/python/deepagents/human-in-the-loop |
| Long-term Memory | https://docs.langchain.com/oss/python/deepagents/long-term-memory |
| Skills | https://docs.langchain.com/oss/python/deepagents/skills |
| Sandboxes | https://docs.langchain.com/oss/python/deepagents/sandboxes |
| Streaming Overview | https://docs.langchain.com/oss/python/deepagents/streaming/overview |
| Streaming Frontend | https://docs.langchain.com/oss/python/deepagents/streaming/frontend |
| Agent Client Protocol | https://docs.langchain.com/oss/python/deepagents/acp |
| Middleware | https://docs.langchain.com/oss/python/deepagents/middleware |

Codex Skills specification: https://developers.openai.com/codex/skills
Agent Skills open standard: https://agentskills.io/specification

---

## Requirements

- Node.js >= 18
- [OpenAI Codex](https://developers.openai.com/codex)

---

## License

MIT — see [LICENSE](LICENSE) for details.

---

## Author

[GitMaxd](https://github.com/Gitmaxd) · [@gitmaxd](https://x.com/gitmaxd)

---

<div align="center">
  <a href="https://github.com/Gitmaxd/deepagents-cli-codex-skill">GitHub</a>
  &nbsp;·&nbsp;
  <a href="https://www.npmjs.com/package/deepagents-cli-codex-skill">npm</a>
  &nbsp;·&nbsp;
  <a href="https://developers.openai.com/codex/skills">Codex Skills Docs</a>
  &nbsp;·&nbsp;
  <a href="https://docs.langchain.com/oss/python/deepagents/overview">Deep Agents Docs</a>
</div>
