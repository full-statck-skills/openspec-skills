---
name: openspec-continue
description: Create the next artifact in the dependency chain with `/opsx:continue`, building up a change incrementally. Use when the user says "continue the change", "create next artifact", "/opsx:continue", or wants step-by-step artifact creation.
---

# OpenSpec Continue Skill

Use **`/opsx:continue`** to create the next artifact in the dependency chain. This builds a change incrementally — one artifact at a time — giving the user control to review and edit before proceeding.

## When to Use

- The user wants incremental, step-by-step artifact creation.
- After creating a change with **openspec-new** and wanting to build artifacts one at a time.
- The user says "continue", "next artifact", "create specs", "create design".

## Prerequisites

- **An active change** exists (created via **openspec-new** or `/opsx:new`).

## Workflow

1. **Query the dependency graph**
   - The agent runs `openspec status --change <name> --json` to see which artifacts are done, ready, or blocked.

2. **Identify ready artifacts**
   - In the default `spec-driven` schema: `proposal` -> `specs` / `design` -> `tasks`.
   - Dependencies are enablers: once a dependency is done, its dependents become "ready".

3. **Create one artifact**
   - Read dependency files for context.
   - Create the first ready artifact (e.g. proposal, then specs, then design, then tasks).
   - Use `openspec instructions <artifact> --change <name> --json` to get enriched instructions and templates.

4. **Show what's unlocked**
   - After creating an artifact, show what becomes available next.

5. **Repeat**
   - User reviews, optionally edits, then runs `/opsx:continue` again for the next artifact.

## Artifact Dependency Graph (spec-driven schema)

```
proposal (root, no dependencies)
    |
    +---> specs (requires: proposal)
    |
    +---> design (requires: proposal)
            |
            +---> tasks (requires: specs + design)
```

## Outputs

- One artifact file created per invocation (e.g. `proposal.md`, `specs/**/*.md`, `design.md`, `tasks.md`).

## Next Steps

- Run `/opsx:continue` again for the next artifact.
- When all planning artifacts are done: use **openspec-apply** to implement tasks.
- Or use **openspec-ff** to fast-forward remaining artifacts.

## Troubleshooting

- **"No artifacts ready"**: All artifacts are either complete or blocked. Check `openspec status --change <name>`.
- **"Change not found"**: Specify the change name explicitly: `/opsx:continue add-dark-mode`.

## References

- [OpenSpec Commands: /opsx:continue](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)
- [OpenSpec Concepts: Artifacts](https://github.com/Fission-AI/OpenSpec/blob/main/docs/concepts.md)

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
