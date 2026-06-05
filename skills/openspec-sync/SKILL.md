---
name: openspec-sync
description: Sync delta specs from a change into main specs using `/opsx:sync`, without archiving the change. Use when the user says "sync specs", "merge specs to main", "/opsx:sync", or needs to update main specs mid-change.
---

# OpenSpec Sync Skill

Use **`/opsx:sync`** to merge delta specs from a change into the main `openspec/specs/` directory without archiving the change. The change remains active after sync. This is optional — **openspec-archive** handles syncing automatically when archiving.

## When to Use

- Long-running change where the user wants specs in main before archiving.
- Multiple parallel changes need updated base specs.
- The user wants to review/preview the merge separately before archiving.

## Prerequisites

- **An active change** with delta specs in `specs/`.

## Workflow

1. **Run sync**
   - `/opsx:sync` — sync the current/inferred change.
   - `/opsx:sync <change-name>` — sync a specific change.

2. **What happens**
   - Reads delta specs from the change folder.
   - Parses ADDED / MODIFIED / REMOVED sections.
   - Merges changes into `openspec/specs/`.
   - Preserves existing content not mentioned in the delta.
   - The change remains active (not archived).

3. **Verify**
   - Review the updated specs in `openspec/specs/`.

## Outputs

- Updated `openspec/specs/` with delta changes merged.
- Change remains active in `openspec/changes/<name>/`.

## Next Steps

- Continue working on the change, or use **openspec-archive** when done.

## Troubleshooting

- **"No delta specs"**: The change has no `specs/` directory; create specs via **openspec-continue** or **openspec-ff** first.
- **Conflicts with other changes**: Sync handles merging at the requirement level; if two changes modify the same requirement, the latest sync wins.

## References

- [OpenSpec Commands: /opsx:sync](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)
- [OpenSpec Concepts: Delta Specs](https://github.com/Fission-AI/OpenSpec/blob/main/docs/concepts.md)

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
