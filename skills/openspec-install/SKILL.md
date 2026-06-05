---
name: openspec-install
description: Install the OpenSpec CLI globally via npm, pnpm, yarn, bun, or nix. Use when the user says "install OpenSpec", "set up OpenSpec", or "openspec command not found".
---

# OpenSpec Install Skill

Install the [OpenSpec CLI](https://github.com/Fission-AI/OpenSpec) so that `openspec` is available globally. This skill covers only **installing the CLI**; it does not run `openspec init`. For project initialization after install, use **openspec-initial**.

## When to Use

- First-time OpenSpec setup ("install OpenSpec", "get started with OpenSpec").
- User reports "openspec: command not found".
- Upgrading to the latest version.
- CI or scripts that need the CLI pre-installed.

## Prerequisites

- **Node.js 20.19.0 or higher** — Check with `node --version`. If not installed, guide the user to install Node.js first (e.g. via nvm, fnm, or official installer).

## Workflow

1. **Check if already installed**
   - Run `openspec --version`. If it succeeds, the CLI is already installed; suggest **openspec-initial** for project setup or upgrading via `npm install -g @fission-ai/openspec@latest`.

2. **Choose package manager and install**
   - **npm** (most common): `npm install -g @fission-ai/openspec@latest`
   - **pnpm**: `pnpm add -g @fission-ai/openspec@latest`
   - **yarn**: `yarn global add @fission-ai/openspec@latest`
   - **bun**: `bun add -g @fission-ai/openspec@latest`
   - **nix** (one-time, no install): `nix run github:Fission-AI/OpenSpec -- init`
   - **nix** (persistent): `nix profile install github:Fission-AI/OpenSpec`

3. **Verify installation**
   - Run `openspec --version` to confirm.

4. **Upgrade existing installation**
   - Same command as install — e.g. `npm install -g @fission-ai/openspec@latest`.

## Outputs

- `openspec` command available globally in PATH.

## Next Steps

- Use **openspec-initial** to run `openspec init` in a project.
- Or use **openspec-onboard** for a guided tutorial.

## Different Environments

| Environment | Command |
|-------------|---------|
| **npm** | `npm install -g @fission-ai/openspec@latest` |
| **pnpm** | `pnpm add -g @fission-ai/openspec@latest` |
| **yarn** | `yarn global add @fission-ai/openspec@latest` |
| **bun** | `bun add -g @fission-ai/openspec@latest` |
| **nix (one-time)** | `nix run github:Fission-AI/OpenSpec -- init` |
| **nix (persistent)** | `nix profile install github:Fission-AI/OpenSpec` |
| **CI** | `npm install -g @fission-ai/openspec@latest` in a cacheable step |

## Troubleshooting

- **Node.js version too old**: OpenSpec requires Node.js 20.19.0+. Upgrade Node.js first.
- **Permission errors (npm)**: Use `npm install -g` without sudo if using nvm/fnm; otherwise consider using nvm.
- **Command not found after install**: Ensure the global bin directory is in PATH (check `npm bin -g`).
- **nix not available**: Install nix or use npm/pnpm/yarn/bun instead.

## References

- [OpenSpec Installation docs](https://github.com/Fission-AI/OpenSpec/blob/main/docs/installation.md)
- [OpenSpec GitHub](https://github.com/Fission-AI/OpenSpec)

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
