---
name: openspec-explore
description: Think through ideas, investigate problems, and clarify requirements before committing to a change using `/opsx:explore`. Use when the user says "explore an idea", "think through this", "investigate options", or wants to brainstorm before creating a formal change.
---

# OpenSpec Explore Skill

Use **`/opsx:explore`** to think through ideas, investigate problems, compare options, and clarify requirements — all without creating any artifacts or committing to a structure. When insights crystallize, transition to **openspec-new** or **openspec-ff**.

## When to Use

- Requirements are unclear and the user needs to investigate first.
- Comparing multiple approaches before deciding on one.
- The user wants to explore the codebase for improvement opportunities.
- Brainstorming before a formal change proposal.

## Prerequisites

- **OpenSpec initialized** in the project (see **openspec-initial**).

## Workflow

1. **Start exploration**
   - Run `/opsx:explore` or `/opsx:explore [topic]`.
   - The agent opens an exploratory conversation with no structure required.

2. **Investigate**
   - Analyze the codebase, compare options, create diagrams, answer questions.
   - No artifacts are created during exploration — it is purely a thinking exercise.

3. **Transition when ready**
   - When the user has clarity, suggest `/opsx:new <change-name>` to start a formal change.
   - Or `/opsx:ff <change-name>` if they want to create all planning artifacts at once.

## Outputs

- No artifacts or files are created. The output is the conversation itself — insights, options, recommendations.

## Next Steps

- When ready to act: use **openspec-new** to start a change, or **openspec-ff** to fast-forward through planning.

## Troubleshooting

- **"Commands not recognized"**: Ensure OpenSpec is initialized (`openspec init`). See **openspec-initial**.

## References

- [OpenSpec Commands: /opsx:explore](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)

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
