# Prompt 架构师

将原始模糊的初级指令重构为结构化专业级的高级提示词。

## 核心框架

**4要素**：角色设定、任务描述、输入背景、输出格式

**4质量标准**：逻辑自洽、零歧义性、可执行性、视觉清晰

## 使用方法

```
/prompt-architect
```

或在对话中说："优化这个提示词"、"帮我写一个prompt"

## 工作流程

1. 接收初级指令
2. 意图分析（检查4要素）
3. 用户确认缺失信息
4. 重构提示词
5. 质量自检
6. 用户确认
7. 输出最终版本

## 文件结构

```
prompt-architect/
├── SKILL.md              # 核心技能文档
├── CHANGELOG.md          # 版本历史
└── references/
    ├── quality-checklist.md    # 质量检查清单
    ├── prompt-templates.md     # 模板库
    └── examples/
        ├── coding-task.md      # 编程示例
        ├── analysis-task.md    # 分析示例
        └── creative-task.md    # 创意示例
```

## 版本

v1.0.0 - 2026-04-30

初始版本，经过TDD验证。