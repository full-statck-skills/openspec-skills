---
name: openspec-archive
description: Archive a completed change with `/opsx:archive`, merging delta specs into main specs and preserving the change for history. Use when the user says "archive the change", "finish up", "/opsx:archive", or "mark this change as done".
---

# OpenSpec Archive Skill

Use **`/opsx:archive`** to finalize a completed change. Archives by merging delta specs into the main `openspec/specs/` directory and moving the change folder to `openspec/changes/archive/`.

## When to Use

- Implementation is complete and verified.
- The user says "archive", "finish", "done with this change", "wrap up".
- After running **openspec-verify** (optional but recommended).

## Prerequisites

- **Change exists** with artifacts and (ideally) completed tasks.

## Workflow

1. **Run archive**
   - `/opsx:archive` — archive the current/inferred change.
   - `/opsx:archive <change-name>` — archive a specific change.

2. **What happens**
   1. Checks artifact completion status and task completion (warns if incomplete).
   2. Offers to sync delta specs if not already synced (see **openspec-sync**).
   3. Merges delta specs into `openspec/specs/` (ADDED / MODIFIED / REMOVED sections).
   4. Moves the change folder to `openspec/changes/archive/YYYY-MM-DD-<name>/`.

3. **All artifacts preserved**
   - The full change context (proposal, design, tasks, specs) is preserved in the archive for audit trail.

## Delta Spec Merge Rules

| Section | What happens |
|---------|--------------|
| `## ADDED Requirements` | Appended to main spec |
| `## MODIFIED Requirements` | Replaces existing requirement in main spec |
| `## REMOVED Requirements` | Deleted from main spec |

## Outputs

- Delta specs merged into `openspec/specs/`.
- Change moved to `openspec/changes/archive/YYYY-MM-DD-<name>/`.

## Next Steps

- Start a new change with **openspec-new**.
- The main specs now reflect the changes — future changes build on the updated source of truth.

## Troubleshooting

- **"Incomplete tasks"**: Archive warns but does not block. Decide whether to complete tasks first or archive as-is.
- **"Delta specs not synced"**: Archive will prompt to sync; or run **openspec-sync** beforehand.
- **Multiple changes to archive**: Use **openspec-bulk-archive** instead.

## References

- [OpenSpec Commands: /opsx:archive](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)
- [OpenSpec Concepts: Archive](https://github.com/Fission-AI/OpenSpec/blob/main/docs/concepts.md)

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
