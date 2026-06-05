---
name: openspec-ff
description: Fast-forward through artifact creation with `/opsx:ff`, generating all planning artifacts (proposal, specs, design, tasks) at once. Use when the user says "fast forward", "create all artifacts", "/opsx:ff", or has a clear picture of what to build.
---

# OpenSpec Fast-Forward Skill

Use **`/opsx:ff`** to fast-forward through all planning artifact creation at once. Creates all artifacts in dependency order (proposal -> specs -> design -> tasks) in a single pass.

## When to Use

- The user has a clear picture of what to build and does not need incremental review.
- The user says "fast forward", "create everything", "generate all planning docs".
- Small to medium features where step-by-step review is unnecessary.

## Prerequisites

- **An active change** exists (created via **openspec-new** or `/opsx:new`).
- Or use `/opsx:ff <change-name>` to create and fast-forward in one step.

## Workflow

1. **Run fast-forward**
   - `/opsx:ff` — fast-forward the current/inferred change.
   - `/opsx:ff <change-name>` — fast-forward a specific change.

2. **Artifacts are created in dependency order**
   - In the default `spec-driven` schema:
     1. `proposal.md` — why and what
     2. `specs/**/*.md` — delta specs (requirements and scenarios)
     3. `design.md` — technical approach
     4. `tasks.md` — implementation checklist
   - Each artifact reads its dependencies before being created.

3. **Review**
   - All planning artifacts are now available. The user can edit any of them before proceeding.

## Outputs

- All planning artifacts created in `openspec/changes/<name>/`:
  - `proposal.md`
  - `specs/**/*.md`
  - `design.md`
  - `tasks.md`

## Next Steps

- Review and edit artifacts if needed.
- Use **openspec-apply** to implement tasks.
- Or use **openspec-verify** after implementation to validate.

## Troubleshooting

- **"Change not found"**: Specify the name: `/opsx:ff add-dark-mode`.
- **Artifact quality issues**: Use `/opsx:continue` instead for more control; add project context in `openspec/config.yaml` (see **openspec-config**).

## References

- [OpenSpec Commands: /opsx:ff](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)

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
