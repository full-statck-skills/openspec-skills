---
name: openspec-onboard
description: Guided onboarding through the complete OpenSpec workflow using `/opsx:onboard`, walking the user through a real change in their codebase. Use when the user says "onboard me", "tutorial", "/opsx:onboard", "how does OpenSpec work", or is new to OpenSpec.
---

# OpenSpec Onboard Skill

Use **`/opsx:onboard`** for a guided, interactive tutorial through the complete OpenSpec workflow. The tutorial uses the user's actual codebase — finding real improvement opportunities, creating a real change, implementing it, and archiving it.

## When to Use

- First-time OpenSpec users who want a hands-on walkthrough.
- The user says "onboard", "tutorial", "show me how OpenSpec works".
- Learning the workflow before using it on real work.

## Prerequisites

- **OpenSpec initialized** in the project (see **openspec-initial**).

## Workflow

1. **Start onboarding**
   - Run `/opsx:onboard`.

2. **Tutorial phases**
   1. Welcome and codebase analysis.
   2. Finding an improvement opportunity (small, safe changes).
   3. Creating a change (`/opsx:new`).
   4. Writing the proposal.
   5. Creating specs.
   6. Writing the design.
   7. Creating tasks.
   8. Implementing tasks (`/opsx:apply`).
   9. Verifying implementation.
   10. Archiving the change.
   11. Summary and next steps.

3. **Interactive**
   - The agent explains each step as it happens.
   - The user chooses which improvement to work on.
   - The change created is real and can be kept or discarded.

## Outputs

- A complete change cycle (from proposal to archive) using the user's actual codebase.
- The user has first-hand experience with every OPSX command.

## Next Steps

- Start real work with **openspec-new** or **openspec-explore**.

## Troubleshooting

- **"Commands not recognized"**: Ensure OpenSpec is initialized (`openspec init`). See **openspec-initial**.
- **Takes too long**: The tutorial covers the full workflow; expect 15-30 minutes.

## References

- [OpenSpec Commands: /opsx:onboard](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)

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
