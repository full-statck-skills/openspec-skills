---
name: openspec-new
description: Start a new OpenSpec change with `/opsx:new`, creating a change folder with metadata and scaffolding. Use when the user says "start a new change", "new feature", "/opsx:new", or "create an OpenSpec change".
---

# OpenSpec New Skill

Use **`/opsx:new`** to start a new change. This creates the change folder structure under `openspec/changes/<name>/` with metadata (`.openspec.yaml`) and prepares the first artifact for creation.

## When to Use

- Starting work on a new feature, bug fix, or refactor.
- The user says "start a change", "new feature", "new OpenSpec change".
- After exploring ideas with **openspec-explore** and deciding what to build.

## Prerequisites

- **OpenSpec initialized** in the project (see **openspec-initial**).

## Workflow

1. **Start the change**
   - `/opsx:new <change-name>` — e.g. `/opsx:new add-dark-mode`.
   - `/opsx:new <change-name> --schema <schema>` — use a specific workflow schema (default: `spec-driven`).
   - If no name is provided, the agent will prompt for one.

2. **What gets created**
   - `openspec/changes/<name>/` directory.
   - `openspec/changes/<name>/.openspec.yaml` — change metadata (schema, created date).

3. **Next action**
   - The agent shows the first artifact ready for creation (typically `proposal`).
   - Use **openspec-continue** to create one artifact at a time, or **openspec-ff** to create all planning artifacts at once.

## Naming Conventions

- Use descriptive names: `add-dark-mode`, `fix-login-bug`, `refactor-auth`.
- Avoid generic names: `update`, `changes`, `wip`.
- Use kebab-case.

## Outputs

- `openspec/changes/<name>/` directory with `.openspec.yaml`.

## Next Steps

- Use **openspec-continue** to create the next artifact incrementally.
- Or **openspec-ff** to fast-forward through all planning artifacts at once.

## Troubleshooting

- **"Change not found"**: Check the change name matches; run `openspec list` to see active changes.
- **"Schema not found"**: List available schemas with `openspec schemas`; see **openspec-schema** for custom schemas.

## References

- [OpenSpec Commands: /opsx:new](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)

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
