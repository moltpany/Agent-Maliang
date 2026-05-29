# Agent-Maliang

> **The Magic Brush Agent** — 神笔马良，开源 AI 设计伙伴

一个 OpenClaw agent 框架，**接入多模态大模型**，具备生成图片、视频的能力。就像神话中的马良手持神笔，Maliang 能将你的创意构想变成视觉现实。

## What Is This?

Maliang 是一个**多模态 AI 设计 Agent** 框架。它像神话中的神笔马良一样，能将你的创意构想变成视觉现实：

- **生成图片** — 角色设计、场景构图、品牌视觉、概念插画
- **生成视频** — 动画短片、动态场景、视觉叙事
- **设计评审** — 对现有设计进行专业 critique（构图、色彩、排版、氛围）
- **资产归档** — 自动管理设计文件、版本迭代、素材库维护

**核心哲学：**
- **创意即咒语** — 好的提示词（prompt）是魔法咒语
- **迭代即修炼** — 每一版 revision 都是向完美更近一步
- **归档即珍藏** — 设计资产值得被妥善保管和追溯

## Why "Maliang"?

取自中国民间故事《神笔马良》。马良有一支神笔，画什么就变成什么。Maliang 就是数字时代的神笔 —— 接入多模态大模型，将你的描述变成图片和视频。

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

## Featured Work: Magic Mirror 🪞

> 一个儿童动画项目的角色与场景设计，展示了 Maliang 从概念到成品的全链路能力。

**项目内容：**
- 🎭 **角色设计** — 为儿童动画设计角色形象（肖像、全身像、表情），建立角色一致性档案
- 🏰 **场景设计** — 冰雪城堡等奇幻场景的概念设计与氛围渲染
- 🎨 **风格定稿** — 多轮迭代后确立统一视觉风格，归档至角色库和场景库

**Maliang 展示了：**
- 通过对话理解创意需求（角色性格、场景氛围）
- 使用多模态模型生成高质量视觉素材
- 建立角色/场景资产库，确保一致性
- 版本迭代与归档管理

（为保护隐私，具体角色细节已脱敏，仅展示工作流程和框架能力）

**📁 查看作品： [moltpany/magic-mirror](https://github.com/moltpany/magic-mirror)**

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

What remains is the **workflow pattern** — how a creative AI agent thinks, organizes, and delivers visual assets.

## License

MIT © moltpany
