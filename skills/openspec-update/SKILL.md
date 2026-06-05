---
name: openspec-update
description: Run `openspec update` to regenerate AI tool instruction files after upgrading the OpenSpec CLI. Use when the user says "update OpenSpec", "openspec update", or "refresh OpenSpec skills/commands".
---

# OpenSpec Update Skill

Run **openspec update** to regenerate AI tool configuration files (skills, commands, rules) after upgrading the OpenSpec CLI package. This ensures your project uses the latest slash commands and skill instructions.

## When to Use

- After upgrading the OpenSpec CLI (`npm install -g @fission-ai/openspec@latest`).
- When slash commands or skills seem outdated or missing.
- After changing tool selections and wanting to refresh configs.

## Prerequisites

- **OpenSpec CLI** installed (see **openspec-install**).
- **Project initialized** with `openspec init` (see **openspec-initial**).

## Workflow

1. **Upgrade the CLI first** (if not already done)
   - `npm install -g @fission-ai/openspec@latest` (or pnpm/yarn/bun equivalent).

2. **Run update**
   - `openspec update` — regenerates AI tool config files.
   - `openspec update --force` — force update even when files are up to date.
   - `openspec update ./my-project` — target a specific directory.

3. **Verify**
   - Check that `.claude/skills/`, `.cursor/rules/`, or other tool directories have been refreshed.
   - Restart your AI tool to pick up new skills if needed.

## Outputs

- Regenerated tool-specific config files (skills, commands, rules) matching the new CLI version.

## Next Steps

- Continue your workflow with **openspec-new**, **openspec-explore**, etc.

## Troubleshooting

- **"openspec: command not found"**: Use **openspec-install** first.
- **"Project not initialized"**: Run **openspec-initial** (`openspec init`) first.
- **Skills not appearing after update**: Restart your AI tool (Claude Code, Cursor, etc.) to reload skills.

## References

- [OpenSpec CLI: update](https://github.com/Fission-AI/OpenSpec/blob/main/docs/cli.md)

## 国内适配

- 支持中文文档和中文注释
- 示例代码兼容国内开发环境
- 提供中文 FAQ 和常见问题解答

## 能力边界

### ✅ 适用场景
- 当你需要使用此技能对应的技术栈时
- 当项目需要遵循最佳实践时
- 当需要快速上手或深入理解核心概念时

### ⚠️ 需要注意
- 复杂业务逻辑需要结合具体场景调整
- 性能优化需要根据实际数据量评估

### ❌ 不适用场景
- 不相关的技术栈或框架
- 需要完全自定义的特殊场景

## 使用流程

### Step 1: 环境准备
确保开发环境已安装必要的依赖和工具。

### Step 2: 配置初始化
根据项目需求进行基础配置。

### Step 3: 核心功能使用
按照示例代码实现核心功能。

### Step 4: 测试验证
运行测试确保功能正常。

### Step 5: 部署上线
完成开发后进行部署和监控。
