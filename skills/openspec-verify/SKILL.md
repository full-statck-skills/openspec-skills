---
name: openspec-verify
description: Validate that implementation matches change artifacts using `/opsx:verify`, checking completeness, correctness, and coherence. Use when the user says "verify implementation", "check my work", "/opsx:verify", or wants quality validation before archiving.
---

# OpenSpec Verify Skill

Use **`/opsx:verify`** to validate that the implementation matches the change artifacts. Checks three dimensions — completeness, correctness, and coherence — and reports issues categorized as CRITICAL, WARNING, or SUGGESTION.

## When to Use

- After implementing tasks with **openspec-apply**, before archiving.
- The user says "verify", "check my work", "validate implementation".
- Quality gate before archiving a change.

## Prerequisites

- **Tasks implemented** (via **openspec-apply** or manual coding).

## Workflow

1. **Run verification**
   - `/opsx:verify` — verify the current/inferred change.
   - `/opsx:verify <change-name>` — verify a specific change.

2. **Three verification dimensions**

   | Dimension | What it validates |
   |-----------|-------------------|
   | **Completeness** | All tasks done, all requirements implemented, scenarios covered |
   | **Correctness** | Implementation matches spec intent, edge cases handled |
   | **Coherence** | Design decisions reflected in code, patterns consistent |

3. **Review the report**
   - **CRITICAL**: Must fix before archiving.
   - **WARNING**: Should address; does not block archive.
   - **SUGGESTION**: Optional improvements.

4. **Fix issues if needed**
   - Address critical issues, optionally fix warnings.
   - Run `/opsx:verify` again to confirm.

## Outputs

- Verification report with categorized issues (CRITICAL / WARNING / SUGGESTION).
- Summary: ready to archive or not.

## Next Steps

- If ready: use **openspec-archive** to archive the change.
- If issues found: fix code or update artifacts, then re-verify.

## Troubleshooting

- **Many false positives**: Add project context in `openspec/config.yaml` to help the agent understand conventions. See **openspec-config**.

## References

- [OpenSpec Commands: /opsx:verify](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)

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
