---
name: openspec-schema
description: Create and manage custom workflow schemas using `openspec schema init/fork/validate/which`. Use when the user says "create a custom workflow", "custom schema", "fork a schema", or wants to define their own artifact types and dependencies.
---

# OpenSpec Schema Skill

Use **openspec schema** subcommands to create and manage custom workflow schemas. Schemas define what artifacts exist and their dependencies. The default `spec-driven` schema provides proposal -> specs -> design -> tasks, but custom schemas allow different workflows.

## When to Use

- The user wants a custom workflow (e.g. research-first, rapid iteration).
- The user says "create a schema", "custom workflow", "fork the spec-driven schema".
- Debugging schema resolution (`openspec schema which`).
- Validating a custom schema's structure.

## Prerequisites

- **OpenSpec CLI** installed (see **openspec-install**).

## Workflow

### Create a new schema from scratch

```bash
openspec schema init my-workflow
# Interactive: prompts for description, artifacts, default
# Non-interactive:
openspec schema init rapid --description "Rapid iteration" --artifacts "proposal,tasks" --default
```

Creates `openspec/schemas/my-workflow/` with `schema.yaml` and `templates/`.

### Fork an existing schema

```bash
openspec schema fork spec-driven my-workflow
```

Copies the `spec-driven` schema for customization.

### Validate a schema

```bash
openspec schema validate my-workflow
# Or validate all:
openspec schema validate
```

### Check schema resolution

```bash
openspec schema which spec-driven
# Shows: package, project, or user source
openspec schema which --all
```

## Schema Structure

```
openspec/schemas/<name>/
├── schema.yaml       # Artifact definitions and dependencies
└── templates/
    ├── proposal.md   # Template for each artifact
    ├── specs.md
    ├── design.md
    └── tasks.md
```

### Example schema.yaml

```yaml
name: research-first
artifacts:
  - id: research
    generates: research.md
    requires: []
  - id: proposal
    generates: proposal.md
    requires: [research]
  - id: tasks
    generates: tasks.md
    requires: [proposal]
```

## Schema Precedence

1. **Project**: `openspec/schemas/<name>/` (local, version controlled)
2. **User**: `~/.local/share/openspec/schemas/<name>/` (global)
3. **Package**: Built-in schemas (e.g. `spec-driven`)

## Outputs

- Custom schema in `openspec/schemas/<name>/` with `schema.yaml` and templates.

## Next Steps

- Use the schema with **openspec-new**: `/opsx:new my-change --schema my-workflow`.
- Or set as default in **openspec-config** (`openspec/config.yaml`).

## Troubleshooting

- **"Schema not found"**: Check `openspec schemas` for available schemas; check `openspec schema which <name>` for resolution.
- **Validation errors**: Run `openspec schema validate <name> --verbose` for details.
- **Unknown artifact IDs in rules**: Check `openspec schemas --json` for artifact IDs per schema.

## References

- [OpenSpec CLI: schema commands](https://github.com/Fission-AI/OpenSpec/blob/main/docs/cli.md)
- [OpenSpec Concepts: Schemas](https://github.com/Fission-AI/OpenSpec/blob/main/docs/concepts.md)
- [OpenSpec Customization](https://github.com/Fission-AI/OpenSpec/blob/main/docs/customization.md)

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
