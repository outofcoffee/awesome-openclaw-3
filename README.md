# Awesome OpenClaw [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A unified, beginner-to-advanced collection of the best OpenClaw resources, setup guides, use cases, security practices, integrations, and skill discovery paths — merged into **one clean README**.

> Last updated: **2026-02-22 (UTC)**

---

## Table of Contents

- [What is OpenClaw?](#what-is-openclaw)
- [Quick Start](#quick-start)
- [Beginner Commands](#beginner-commands)
- [How OpenClaw Works](#how-openclaw-works)
- [Official Resources](#official-resources)
- [Installation Guides](#installation-guides)
- [Skills & Plugins](#skills--plugins)
- [Best Beginner Skills](#best-beginner-skills)
- [Use Cases (Real-World)](#use-cases-real-world)
- [Integrations](#integrations)
- [MCP Support](#mcp-support)
- [Community Projects](#community-projects)
- [Alternatives & Comparisons](#alternatives--comparisons)
- [Security](#security)
- [Contributing](#contributing)
- [License](#license)

---

## What is OpenClaw?

OpenClaw (formerly Moltbot / Clawdbot) is an open-source AI agent platform that runs locally and combines:

- **Channels** (Telegram, WhatsApp, Discord, Slack, etc.)
- **Tools** (web, browser, filesystem, shell, messaging, devices)
- **Skills** (task-focused playbooks)
- **Memory** (`memory/*.md` + `MEMORY.md` style persistence)
- **Automation** (heartbeats, cron, sub-agents)

Think: **assistant + toolbelt + automation runtime**.

---

## Quick Start

```bash
# Install
npm install -g openclaw@latest
# or
pnpm add -g openclaw@latest

# Onboard
openclaw onboard --install-daemon
```

Then:
1. Choose AI provider
2. Connect messaging channel
3. Start with one small workflow
4. Add skills gradually

Dashboard (local):
- `http://localhost:18789/`

---

## Beginner Commands

### In chat
- `/new` or `/reset` — fresh session
- `/status` — runtime + model + usage snapshot
- `/doctor` — diagnostics / fix hints
- `/config` — configuration helpers

### In terminal
- `openclaw status`
- `openclaw gateway status`
- `openclaw gateway restart`
- `openclaw help`

---

## How OpenClaw Works

1. Trigger (chat/cron/heartbeat)
2. Context load (session + workspace)
3. Skill/tool selection
4. Action execution
5. Response + memory update
6. Optional background sub-agent orchestration

Docs:
- https://docs.openclaw.ai/concepts
- https://docs.openclaw.ai/tools
- https://docs.openclaw.ai/automation
- https://docs.openclaw.ai/security

---

## Official Resources

- OpenClaw website: https://openclaw.ai/
- OpenClaw GitHub: https://github.com/openclaw/openclaw
- Documentation: https://docs.openclaw.ai/
- Skills registry: https://clawhub.ai/
- Releases: https://github.com/openclaw/openclaw/releases
- AGENTS.md guide: https://github.com/openclaw/openclaw/blob/main/AGENTS.md
- Changelog: https://github.com/openclaw/openclaw/blob/main/CHANGELOG.md
- Showcase: https://openclaw.ai/showcase
- Community Discord: https://discord.com/invite/clawd

---

## Installation Guides

| Guide | Platform | Description |
|---|---|---|
| [Official Getting Started](https://docs.openclaw.ai/start/getting-started) | All | Official setup guide |
| [Codecademy Tutorial](https://www.codecademy.com/article/open-claw-tutorial-installation-to-first-chat-setup) | All | Installation to first chat |
| [Hostinger Guide](https://www.hostinger.com/tutorials/how-to-set-up-openclaw) | VPS | Private server setup |
| [DigitalOcean One-Click](https://www.digitalocean.com/community/tutorials/how-to-run-openclaw) | Cloud | One-click deployment |
| [LMStudio Setup](https://nwosunneoma.medium.com/how-to-setup-openclaw-with-lmstudio-1960a8046f6b) | Local | Local model setup |
| [Docker Setup](https://habr.com/en/articles/992720/) | Docker | Container deployment |

---

## Skills & Plugins

### Skill registries and sources
- ClawHub: https://clawhub.ai/
- Official skills repo: https://github.com/openclaw/skills
- Skill directory source: https://github.com/openclaw/clawhub
- Skills discovery mirror: https://skills.sh/openclaw/openclaw

### Skill installation
```bash
# ClawHub
openclaw skills install <skill-name>

# npm plugin
openclaw plugins install <npm-package>

# clawhub CLI
npx clawhub@latest install <skill-slug>
```

### Manual skill install
- Global: `~/.openclaw/skills/`
- Workspace: `<project>/skills/`
- Priority: **Workspace > Local > Bundled**

### Major skill categories (community index)

- Coding Agents & IDEs (133)
- Marketing & Sales (143)
- Communication (132)
- Git & GitHub (66)
- Productivity & Tasks (135)
- Speech & Transcription (65)
- AI & LLMs (287)
- Smart Home & IoT (56)
- Web & Frontend Development (202)
- Data & Analytics (46)
- DevOps & Cloud (212)
- Calendar & Scheduling (50)
- Browser & Automation (139)
- Media & Streaming (80)
- PDF & Documents (67)
- Image & Video Generation (60)
- Notes & PKM (100)
- Security & Passwords (64)
- Search & Research (253)
- CLI Utilities (129)
- and more

---

## Best Beginner Skills

Start here:

1. `github`
2. `gh-issues`
3. `calendar`
4. `Productivity`
5. `weather`
6. `healthcheck`
7. `tmux`
8. `skill-creator`
9. `clawhub`
10. `copywriter`

Then branch into your stack:
- Coding: code review, CI, release, PR automation
- Ops: monitoring, Docker, cloud deploy, security
- Second-brain: memory search, PKM, RAG

---

## Use Cases (Real-World)

## Social Media
- Daily Reddit Digest
- Daily YouTube Digest
- X Account Analysis
- Multi-Source Tech News Digest

## Creative & Building
- Goal-Driven Autonomous Tasks
- YouTube Content Pipeline
- Multi-Agent Content Factory

## Infrastructure & DevOps
- n8n Workflow Orchestration
- Self-Healing Home Server

## Productivity
- Autonomous Project Management
- Multi-Channel AI Customer Service
- Phone-Based Personal Assistant
- Inbox De-clutter
- Personal CRM
- Health & Symptom Tracker
- Multi-Channel Personal Assistant
- Project State Management
- Dynamic Dashboard
- Todoist Task Manager
- Family Calendar & Household Assistant
- Multi-Agent Specialized Team
- Custom Morning Brief
- Event Guest Confirmation

## Research & Learning
- AI Earnings Tracker
- Personal Knowledge Base (RAG)
- Market Research & Product Factory
- Semantic Memory Search

## Finance
- Polymarket Autopilot (paper trading)

## Second Brain blueprint
- Capture quickly (`memory/YYYY-MM-DD.md`)
- Distill weekly (`MEMORY.md`)
- Search before decisions
- Run review heartbeat
- Build semantic retrieval layer as needed

---

## Integrations

### Messaging platforms
- WhatsApp
- Telegram
- Discord
- Slack
- Signal
- iMessage
- Microsoft Teams
- Google Chat
- Matrix
- BlueBubbles
- Zalo
- WebChat

### Core external service patterns
- GitHub (issues/PR/CI)
- Gmail/email
- Calendar
- Browser automation
- File system + shell
- Cron scheduling

---

## MCP Support

OpenClaw supports MCP for tool expansion.

### MCP references
- MCP adapter plugin: https://github.com/androidStern-personal/openclaw-mcp-adapter
- Native MCP support issue: https://github.com/openclaw/openclaw/issues/4834
- PR #5121: https://github.com/openclaw/openclaw/pull/5121
- PR #1605: https://github.com/openclaw/openclaw/pull/1605

### Example MCP servers/use
- Creative design toolkit
- Security auditing
- Profanity detection
- AML/compliance flows
- Local RAG patterns

---

## Community Projects

### Clients / UI
- webclaw
- openclaw-web
- clawterm
- PinchChat

### Deployment
- moltworker
- OpenClawInstaller
- openclaw-docker
- claw-k8s
- lightweight edge/self-healing variants

### Memory / storage
- memU
- clawmem
- openclaw-redis
- encrypted artifact backups

### Monitoring / observability
- crabwalk
- clawmetrics
- openclaw-logs

### Regional integrations
- DingTalk / Feishu / WeChat / QQ / WeCom connectors

---

## Alternatives & Comparisons

| Agent | Type | Best For |
|---|---|---|
| OpenClaw | Open Source | Personal assistant + automation |
| Manus AI | Proprietary | General framework |
| OpenManus | Open Source | Manus-like workflows |
| Claude Code | Proprietary | Coding-focused assistance |
| Jan.ai | Open Source | Privacy/offline-first |

---

## Security

### Must-do baseline
- Do **not** expose OpenClaw on a public open port
- Use private networking (e.g., Tailscale)
- Scope and rotate API keys
- Review skill source before install
- Keep OpenClaw + skills updated
- Prefer sandboxed execution

### Practical hardening
- Limit filesystem scope
- Add guardrail/pre-action approval layers for sensitive tools
- Run periodic security checks
- Monitor logs and failed auth patterns

### Known risks
- Prompt injection from untrusted content
- Malicious/poisoned third-party skills
- Credential leakage from poor env handling
- Public instance takeover risk

---

## Contributing

PRs welcome.

Contribution checklist:
- Working link
- 1–2 line description
- Add to correct section
- Keep alphabetical order in lists
- Include prerequisites (API key, infra, paid service)
- Add/refresh last-verified date where possible

---

## License

CC0 1.0 (public domain): https://creativecommons.org/publicdomain/zero/1.0/
