# /check-structure Slash Command

## 功能描述
通过调用 `structure-manager` subagent 验证当前项目的目录结构是否符合规范

## 命令格式
```
/check-structure [--fix]
```

## 参数说明
- `--fix`: 可选参数，自动修复发现的结构问题

## 执行流程

### 1. 自动调用 structure-manager subagent
```
当用户执行 /check-structure 命令时：
→ 触发 structure-manager subagent
→ 传递检查模式参数
→ subagent 执行结构验证流程
```

### 2. structure-manager 检查步骤
1. **加载项目配置** - 读取 .claude-structure.json 规范
2. **扫描项目结构** - 使用 Glob 和 LS 工具遍历项目
3. **验证目录结构** - 检查必需目录是否存在
4. **验证文件命名** - 检查文件命名是否符合规范
5. **检查文件位置** - 验证文件是否放在正确目录
6. **生成检查报告** - 输出详细的验证结果

### 3. 检查报告格式
```
🔍 项目结构检查报告
项目类型: react-app
项目名称: dashboard
检查时间: 2024-01-20 10:30:00

✅ 通过的检查:
  • 必需目录结构完整
  • 组件文件命名规范正确
  • 测试文件结构与源文件匹配

⚠️ 警告:
  • src/utils/helper.js 建议使用camelCase命名
  
❌ 错误:
  • Component.jsx 应该放在 src/components/ 目录
  • InvalidName.vue 命名不符合PascalCase规范

📝 修复建议:
  • 移动 Component.jsx 到 src/components/
  • 重命名 InvalidName.vue 为 InvalidName.vue (已符合规范)
```

## 使用示例
```bash
/check-structure                    # 仅检查，不修复
/check-structure --fix             # 检查并自动修复
```

---

# /fix-structure Slash Command

## 功能描述
通过调用 `structure-manager` subagent 自动修复项目结构问题

## 命令格式
```
/fix-structure [--interactive]
```

## 参数说明
- `--interactive`: 交互式修复，每个修复操作前询问用户确认

## 执行流程

### 1. 修复操作类型
- **文件移动** - 将错放的文件移动到正确目录
- **重命名文件** - 修复不符合规范的文件名
- **创建缺失目录** - 创建项目必需的目录结构
- **删除违规文件** - 移除不应存在的文件（需用户确认）

### 2. 安全机制
- **备份机制** - 修复前创建当前结构快照
- **确认机制** - 危险操作前要求用户确认
- **撤销机制** - 提供修复操作的撤销功能
- **日志记录** - 记录所有修复操作的详细日志

## 使用示例
```bash
/fix-structure                     # 自动修复所有问题
/fix-structure --interactive       # 交互式修复
```

---

# /update-rules Slash Command

## 功能描述
更新当前项目的目录结构规范配置

## 命令格式
```
/update-rules [配置类型]
```

## 配置类型选项
- `naming`: 更新文件命名规范
- `structure`: 更新目录结构规则
- `project-type`: 更改项目类型
- `custom`: 自定义规则配置

## 使用示例
```bash
/update-rules naming              # 更新命名规范
/update-rules structure           # 更新目录结构
/update-rules project-type        # 更改项目类型
```