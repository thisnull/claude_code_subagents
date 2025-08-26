# /init-docs Slash Command

## 功能描述
通过调用 `docs-manager` subagent 在任意项目中自动创建完整的文档目录结构，并建立文档管理和一致性保障机制。

## 命令格式
```
/init-docs
```

## 执行流程
```
当用户执行 /init-docs 命令时：
→ 自动触发 docs-manager subagent
→ subagent 直接创建完整的文档目录结构
→ 在每个目录中生成相应的README.md
→ 更新项目的CLAUDE.md添加文档管理约束
```

## 预期输出
- 完整的docs/目录结构（通过Claude Code Write工具创建）
- 每个目录的README.md索引文件
- 更新的CLAUDE.md（包含文档管理约束和提醒机制）

## 使用示例
```bash
/init-docs     # 在当前项目创建标准文档体系
```