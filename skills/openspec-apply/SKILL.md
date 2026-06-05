---
name: openspec-apply
description: Implement tasks from the change using `/opsx:apply`, working through the task list and checking off items. Use when the user says "implement", "apply the change", "/opsx:apply", or "start coding from tasks".
---

# OpenSpec Apply Skill

Use **`/opsx:apply`** to implement tasks from a change. The agent reads `tasks.md`, works through tasks one by one, writes code, creates files, runs tests as needed, and checks off completed items with `[x]`.

## When to Use

- All planning artifacts are complete and the user wants to implement.
- The user says "implement", "apply", "start coding", "execute tasks".
- Resuming implementation after an interruption.

## Prerequisites

- **Planning artifacts complete** — at minimum `tasks.md` exists (created via **openspec-ff** or **openspec-continue**).

## Workflow

1. **Start implementation**
   - `/opsx:apply` — apply the current/inferred change.
   - `/opsx:apply <change-name>` — apply a specific change.

2. **Read tasks**
   - The agent reads `tasks.md` and identifies incomplete tasks (unchecked `[ ]` items).

3. **Work through tasks**
   - For each task: read relevant specs, design, and existing code; write code; create/modify files; run tests.
   - Mark each task complete with `[x]` in `tasks.md`.

4. **Handle issues**
   - If a task reveals that the design was wrong, edit the artifact (e.g. `design.md`) and continue.
   - OpenSpec is fluid — updating artifacts during implementation is expected and encouraged.

5. **Resume if interrupted**
   - Run `/opsx:apply` again; it picks up where it left off based on checkbox state.

## Outputs

- Code changes (new files, modified files) implementing the tasks.
- `tasks.md` updated with `[x]` for completed tasks.

## Next Steps

- Use **openspec-verify** to validate implementation matches artifacts.
- Use **openspec-archive** to archive the completed change.

## Troubleshooting

- **"Change not found"**: Specify the change name: `/opsx:apply add-dark-mode`.
- **Tasks seem wrong**: Edit `tasks.md` (or use `/opsx:continue` to regenerate) before applying.
- **Implementation diverges from design**: Edit `design.md` or `specs/` as needed; OpenSpec is iterative.

## References

- [OpenSpec Commands: /opsx:apply](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)
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
