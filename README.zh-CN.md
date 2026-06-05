<div align="center">

# openspec-skills

**OpenSpec spec-driven development workflow skills**

[![GitHub](https://img.shields.io/badge/github-full--statck--skills%2Fopenspec-skills-green.svg)](https://github.com/full-statck-skills/openspec-skills)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-兼容-purple.svg)](https://agentskills.io)

[English](./README.md) | 简体中文

[简介](#-简介) ·
[安装](#-安装) ·
[技能列表](#-技能列表) ·
[支持的智能体](#-支持的智能体) ·
[生态](#-生态)

</div>

---

## 📖 简介

**OpenSpec 技能** 是一组 AI 编码智能体技能，属于 [Full Stack Skills](https://github.com/partme-ai/full-stack-skills) 生态，由 [PartMe.AI](https://github.com/partme-ai) 维护。

本包包含 **15 个技能**。每个技能是一个独立的 `SKILL.md` 文件，AI 智能体按需加载。

## 📦 安装

```bash
npx skills add full-statck-skills/openspec-skills
```

或按需安装特定技能：

```bash
npx skills add full-statck-skills/openspec-skills --skill <skill-name>
```

## 🎯 技能列表 (15)

| 技能 | 描述 |
|------|------|
| `openspec-apply` | Implement tasks from the change using `/opsx:apply`, working through the task list and checking off items. Use when t... |
| `openspec-archive` | Archive a completed change with `/opsx:archive`, merging delta specs into main specs and preserving the change for hi... |
| `openspec-bulk-archive` | Archive multiple completed changes at once with `/opsx:bulk-archive`, handling spec conflicts between changes. Use wh... |
| `openspec-config` | Configure OpenSpec project settings and global CLI configuration using `openspec/config.yaml` and `openspec config` c... |
| `openspec-continue` | Create the next artifact in the dependency chain with `/opsx:continue`, building up a change incrementally. Use when ... |
| `openspec-explore` | Think through ideas, investigate problems, and clarify requirements before committing to a change using `/opsx:explor... |
| `openspec-ff` | Fast-forward through artifact creation with `/opsx:ff`, generating all planning artifacts (proposal, specs, design, t... |
| `openspec-initial` | Run `openspec init` to initialize OpenSpec in a project directory, creating the openspec/ folder structure and config... |
| `openspec-install` | Install the OpenSpec CLI globally via npm, pnpm, yarn, bun, or nix. Use when the user says "install OpenSpec", "set u... |
| `openspec-new` | Start a new OpenSpec change with `/opsx:new`, creating a change folder with metadata and scaffolding. Use when the us... |
| `openspec-onboard` | Guided onboarding through the complete OpenSpec workflow using `/opsx:onboard`, walking the user through a real chang... |
| `openspec-schema` | Create and manage custom workflow schemas using `openspec schema init/fork/validate/which`. Use when the user says "c... |
| `openspec-sync` | Sync delta specs from a change into main specs using `/opsx:sync`, without archiving the change. Use when the user sa... |
| `openspec-update` | Run `openspec update` to regenerate AI tool instruction files after upgrading the OpenSpec CLI. Use when the user say... |
| `openspec-verify` | Validate that implementation matches change artifacts using `/opsx:verify`, checking completeness, correctness, and c... |

## 🤖 支持的智能体

适用于 [Claude Code](https://code.claude.com)、[Codex](https://developers.openai.com/codex)、[Cursor](https://cursor.com)、[OpenCode](https://opencode.ai)、[Gemini CLI](https://geminicli.com)、[GitHub Copilot](https://github.com/features/copilot)、[Windsurf](https://codeium.com/windsurf) 及 [70+ 其他智能体](https://agentskills.io/clients)。

### Claude Code 安装

**方式一：npx skills CLI（推荐）**

```bash
npx skills add full-statck-skills/openspec-skills
```

**方式二：手动安装**

```bash
git clone https://github.com/full-statck-skills/openspec-skills.git
cp -r openspec-skills/skills/* .claude/skills/
```

更多详情请参阅 [Claude Code 技能指南](https://code.claude.com/docs/en/skills) 和 [Agent Skills 规范](https://agentskills.io/)。

## 🌐 生态

| 资源 | 链接 |
|------|------|
| **Full Stack Skills** | [github.com/partme-ai/full-stack-skills](https://github.com/partme-ai/full-stack-skills) |
| **全部技能组** | [github.com/full-statck-skills](https://github.com/full-statck-skills) |
| **Agent Skills 规范** | [agentskills.io](https://agentskills.io) |
| **Skills CLI** | [github.com/vercel-labs/skills](https://github.com/vercel-labs/skills) |

## 📄 许可证

Apache 2.0 — 详见 [LICENSE](LICENSE)。
