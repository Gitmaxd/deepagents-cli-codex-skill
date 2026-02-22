# Security Policy

## Supported Versions

| Version | Supported |
|---------|-----------|
| 0.1.x   | Yes       |

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please report it responsibly.

**Do not open a public issue.**

Instead, email **131803031+Gitmaxd@users.noreply.github.com** with:

- A description of the vulnerability
- Steps to reproduce
- Potential impact

You can expect an initial response within 72 hours. We will work with you to understand the issue and coordinate a fix before any public disclosure.

## Scope

This project is a documentation skill — it contains markdown reference files and a CLI installer. It does not execute user code, make network requests, or handle credentials. The primary security considerations are:

- **Supply chain** — the npm package and its dependencies
- **Installer behavior** — the CLI copies files to the filesystem without overwriting existing files
- **Skill content** — instructions that Codex follows when the skill is active
