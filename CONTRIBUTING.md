# Contributing

Thank you for your interest in contributing to the Deep Agents CLI Skill for OpenAI Codex.

## How to Contribute

1. **Fork** the repository
2. **Create a branch** for your change (`git checkout -b my-change`)
3. **Make your changes** and commit (`git commit -m "description of change"`)
4. **Push** to your fork (`git push origin my-change`)
5. **Open a Pull Request** against `main`

## What to Contribute

- **Accuracy fixes** — corrections to CLI commands, flags, or behavior documented in the skill
- **Coverage gaps** — new reference material for undocumented Deep Agents CLI features
- **Installer improvements** — enhancements to the CLI installer or build pipeline

## Guidelines

- All skill content must be verifiable against the [official Deep Agents documentation](https://docs.langchain.com/oss/python/deepagents/overview)
- Keep `SKILL.md` under 500 lines per the [Agent Skills specification](https://agentskills.io/specification)
- Move detailed reference material to separate files in `references/`
- Run `pnpm run build && pnpm run typecheck` before submitting

## Reporting Issues

Open an issue on [GitHub](https://github.com/Gitmaxd/deepagents-cli-codex-skill/issues) with:

- A clear description of the problem
- Steps to reproduce (if applicable)
- Expected vs actual behavior

## License

By contributing, you agree that your contributions will be licensed under the [MIT License](LICENSE).
