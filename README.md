<div align="center">

# openspec-skills

**OpenSpec spec-driven development workflow skills**

[![GitHub](https://img.shields.io/badge/github-full--statck--skills%2Fopenspec-skills-green.svg)](https://github.com/full-statck-skills/openspec-skills)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Compatible-purple.svg)](https://agentskills.io)

English | [简体中文](./README.zh-CN.md)

[Introduction](#-introduction) ·
[Install](#-install) ·
[Skills](#-skills) ·
[Supported Agents](#-supported-agents) ·
[Ecosystem](#-ecosystem)

</div>

---

## 📖 Introduction

**OpenSpec Skills** is a curated collection of Agent Skills for AI coding agents, part of the [Full Stack Skills](https://github.com/partme-ai/full-stack-skills) ecosystem maintained by [PartMe.AI](https://github.com/partme-ai).

This package includes **15 skills**. Each skill is a self-contained `SKILL.md` file that AI agents load on-demand.

## 📦 Install

```bash
npx skills add full-statck-skills/openspec-skills
```

Or install specific skills:

```bash
npx skills add full-statck-skills/openspec-skills --skill <skill-name>
```

## 🎯 Skills (15)

| Skill | Description |
|-------|-------------|
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

## 🤖 Supported Agents

Works with [Claude Code](https://code.claude.com), [Codex](https://developers.openai.com/codex), [Cursor](https://cursor.com), [OpenCode](https://opencode.ai), [Gemini CLI](https://geminicli.com), [GitHub Copilot](https://github.com/features/copilot), [Windsurf](https://codeium.com/windsurf), and [70+ others](https://agentskills.io/clients).

### Claude Code Installation

**Option 1: npx skills CLI (Recommended)**

```bash
npx skills add full-statck-skills/openspec-skills
```

**Option 2: Manual Installation**

```bash
git clone https://github.com/full-statck-skills/openspec-skills.git
cp -r openspec-skills/skills/* .claude/skills/
```

For more details, see the [Claude Code Skills Guide](https://code.claude.com/docs/en/skills) and [Agent Skills Spec](https://agentskills.io/).

## 🌐 Ecosystem

| Resource | Link |
|----------|------|
| **Full Stack Skills** | [github.com/partme-ai/full-stack-skills](https://github.com/partme-ai/full-stack-skills) |
| **All Skill Groups** | [github.com/full-statck-skills](https://github.com/full-statck-skills) |
| **Agent Skills Spec** | [agentskills.io](https://agentskills.io) |
| **Skills CLI** | [github.com/vercel-labs/skills](https://github.com/vercel-labs/skills) |

## 📄 License

Apache 2.0 — see [LICENSE](LICENSE).
