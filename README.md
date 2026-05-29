# Agent-DesignDirector

An OpenClaw agent framework for **visual design, brand identity, and creative direction**. Think of it as a design studio lead that can handle logo design, character design, scene composition, and brand systems — all through conversational workflow.

## What Is This?

This is a distilled, reusable agent framework for anyone who needs a **design partner** inside OpenClaw. It carries the workflow patterns and aesthetic sensibilities of a design director, without any personal data tied to a specific user or project.

**Core philosophy:**
- **Taste over tools** — A good designer knows *why*, not just *how*
- **Iterate with intent** — Every revision should have a rationale
- **Archive with structure** — Design assets live in organized workspaces

## Core Workflows

| Trigger | What It Does |
|---------|--------------|
| "Design a logo for..." | Runs brand analysis → mood board → concept sketches → final deliverable |
| "Create a character..." | Builds character sheets (body, portrait, expressions) with consistent style |
| "Design a scene..." | Composes environments with lighting, mood, and focal points |
| "Review my design" | Critiques with constructive feedback (composition, color, typography, hierarchy) |
| "Build a brand system" | Generates logo, color palette, typography rules, usage guidelines |

## Repository Layout

```
Agent-DesignDirector/          ← This repo (the framework)
├── README.md
├── LICENSE
├── .gitignore
├── references/                ← Template files (copy to your workspace)
│   ├── IDENTITY.md.template
│   ├── SOUL.md.template
│   ├── AGENTS.md.template
│   ├── TOOLS.md.template
│   ├── USER.md.template
│   └── HEARTBEAT.md.template
└── skills/                    ← Core skills (install from ClawHub)
    └── (see Required Skills below)
```

**After setup, your workspace looks like:**

```
/workspace-design-director/
├── IDENTITY.md          ← Who you are (fill in)
├── SOUL.md              ← Your personality & vibe (fill in)
├── AGENTS.md            ← Workspace rules (copy template)
├── TOOLS.md             ← Your tool notes (fill in)
├── USER.md              ← Who you serve (fill in)
├── HEARTBEAT.md         ← Periodic checks (optional)
├── skills/
│   ├── logo-design/     ← Install from ClawHub
│   └── graphic-design/  ← Install from ClawHub
└── memory/
    └── YYYY-MM-DD.md    ← Daily logs (auto-created)
```

## Quick Start

1. **Clone or copy** this repo into a new workspace:
   ```bash
   mkdir -p /workspace-design-director
   cp references/*.md.template /workspace-design-director/
   # Remove .template suffix
   for f in /workspace-design-director/*.template; do mv "$f" "${f%.template}"; done
   ```

2. **Install required skills** from ClawHub:
   ```bash
   clawhub install logo-design
   clawhub install graphic-design
   ```
   *(If `clawhub` CLI is not available, download skills from [clawhub.ai](https://clawhub.ai) and unzip to `skills/`.)*

3. **Fill in your identity**:
   - Edit `IDENTITY.md` — pick a name, emoji, vibe
   - Edit `SOUL.md` — customize the design philosophy section
   - Edit `USER.md` — who is your human? What do they care about?

4. **Register in OpenClaw**:
   - Add to `agents.list` in your `openclaw.json`
   - Assign a channel (e.g., Feishu) if you want messaging
   - Restart gateway

5. **Start designing** — Say "Design a logo for my coffee shop" and go.

## Required Skills

This agent framework is designed to work with these skills (install separately):

- **`logo-design`** — Brand identity pipeline: analysis → mood board → concepts → final
- **`graphic-design`** — General visual design workflows, composition, color theory

Both are available on [ClawHub](https://clawhub.ai). The agent will check `SKILL.md` before executing any design task.

## What Gets Generalized

When this framework was distilled from a real agent, the following were **stripped** to protect privacy:

- Real family members, personal projects, and private photos
- App credentials (App ID, App Secret, tokens)
- Memory logs containing specific project details
- Runtime data (`.openclaw/`, logs, state files)

What remains is the **workflow pattern** — how a design director thinks, organizes, and delivers.

## License

MIT © moltpany
