---
name: openspec-bulk-archive
description: Archive multiple completed changes at once with `/opsx:bulk-archive`, handling spec conflicts between changes. Use when the user says "archive all changes", "bulk archive", "/opsx:bulk-archive", or has multiple completed changes.
---

# OpenSpec Bulk Archive Skill

Use **`/opsx:bulk-archive`** to archive multiple completed changes at once. Validates each change, detects spec conflicts across changes, and resolves them by checking what is actually implemented.

## When to Use

- Multiple changes are completed and ready to archive.
- The user says "archive all", "bulk archive", "clean up finished changes".
- After a sprint or batch of parallel work.

## Prerequisites

- **Multiple active changes** with completed tasks.

## Workflow

1. **Run bulk archive**
   - `/opsx:bulk-archive` — lists all completed changes and prompts to select.
   - `/opsx:bulk-archive <name1> <name2> ...` — archive specific changes.

2. **What happens**
   - Lists all completed changes.
   - Validates each change before archiving.
   - Detects spec conflicts across changes (e.g. two changes touch the same spec file).
   - Resolves conflicts by checking what is actually implemented in the codebase.
   - Archives in chronological order (by creation date).

3. **Confirm**
   - The agent shows the list and conflict resolution plan; the user confirms.

## Outputs

- All selected changes archived to `openspec/changes/archive/`.
- Delta specs merged into `openspec/specs/` in chronological order.

## Next Steps

- Start new changes with **openspec-new**.

## Troubleshooting

- **Spec conflicts**: The agent inspects the codebase to resolve; review the resolution before confirming.
- **Incomplete changes**: Bulk archive warns about incomplete tasks but does not block.

## References

- [OpenSpec Commands: /opsx:bulk-archive](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)

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
