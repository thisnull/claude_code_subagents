# /init-project Slash Command

## 功能描述
通过调用 `structure-manager` subagent 初始化项目目录结构并建立 Claude Code 原生的结构约束机制

## 命令格式
```
/init-project [项目类型] [项目名称]
```

## 支持的项目类型
- `react-app`: React前端项目  
- `vue-app`: Vue前端项目
- `fullstack-web`: 全栈Web项目
- `api-service`: 后端API服务项目
- `mobile-app`: 移动应用项目
- `library`: 组件库/工具库项目

## Claude Code 原生执行流程

### 1. 自动调用 structure-manager subagent
```
当用户执行 /init-project 命令时：
→ 自动触发 structure-manager subagent
→ 传递项目类型和名称参数
→ subagent 执行完整的项目初始化流程
```

### 2. structure-manager 执行步骤
1. **验证输入参数** - 检查项目类型和名称的有效性
2. **创建项目目录结构** - 使用 Write 和 LS 工具创建标准目录
3. **生成结构配置文件** - 创建 .claude-structure.json
4. **更新 CLAUDE.md** - 添加项目特定的结构约束提醒
5. **创建示例文件** - 生成符合规范的示例代码文件
6. **验证初始结构** - 确保所有创建的内容符合规范

### 3. 纯 Claude Code 机制优势
- **无外部依赖**: 完全基于 Claude Code 内置工具
- **实时验证**: 通过 CLAUDE.md 系统提醒实现持续约束
- **智能适应**: subagent 可以根据项目特点调整行为
- **协作友好**: 其他开发者也能获得相同的结构约束

## 使用示例
```bash
/init-project react-app dashboard
/init-project api-service user-service  
/init-project fullstack-web ecommerce
```

## 预期输出
- 完整的项目目录结构（通过 Claude Code Write 工具创建）
- 配置好的 CLAUDE.md（包含系统提醒机制）
- .claude-structure.json 规范文件
- 项目类型特定的示例文件和文档

## 与其他 Slash Commands 集成
- `/check-structure` - 验证当前项目结构
- `/fix-structure` - 自动修复结构问题
- `/update-rules` - 更新项目结构规范