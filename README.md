# skills

Agent skills by [iamhelitha](https://github.com/iamhelitha). Each skill is a folder under `skills/` with a `SKILL.md`, the open [Agent Skills](https://agentskills.io) format that many coding agents read.

## Skills

| Skill | What it does |
|---|---|
| [llm-prompt-injection-audit](skills/llm-prompt-injection-audit/SKILL.md) | Audits AI chatbots and agents for prompt injection, leakage and excessive agency (OWASP LLM Top 10 2025), then reports weaknesses, fixes and a safe test plan. |

## Install

### Claude Code

```text
/plugin marketplace add iamhelitha/skills
/plugin install llm-prompt-injection-audit@iamhelitha
```

### Other coding agents (Codex, Cursor, Gemini CLI, Copilot, OpenCode and more)

Use the [`skills` CLI](https://github.com/vercel-labs/skills), which installs into the right folder for each agent it detects:

```bash
npx skills add iamhelitha/skills
```

### Manual

Copy a skill folder into your agent's skills directory. Common locations:

| Agent | Project | Personal |
|---|---|---|
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |
| Codex, and agents that follow the shared convention | `.agents/skills/` | `~/.agents/skills/` |

```bash
git clone https://github.com/iamhelitha/skills.git
cp -r skills/skills/llm-prompt-injection-audit ~/.claude/skills/
```

Check your agent's docs for its exact path if it isn't listed.

### Claude.ai

Zip `skills/llm-prompt-injection-audit` and upload it under **Settings → Capabilities → Skills**.

## Layout

```text
.
├── .claude-plugin/     # Claude Code marketplace + plugin manifests
├── skills/
│   └── llm-prompt-injection-audit/SKILL.md
├── LICENSE
└── README.md
```

## License

[MIT](LICENSE)
