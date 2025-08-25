# Claude Code 原生目录结构提醒机制

## 核心设计理念

通过 CLAUDE.md 文件的 `<system-reminder>` 标签和项目配置，让 Claude Code 在每次文件操作前自动感知并遵循目录结构约束，完全基于 Claude Code 内置机制。

## 实现策略

### 1. CLAUDE.md 嵌入式系统提醒

在项目的 CLAUDE.md 文件中嵌入以下结构化提醒：

```markdown
<system-reminder>
🏗️ **项目目录结构约束检查**

在创建任何文件或目录前，请严格遵循以下流程：

1. **强制验证步骤**：
   - 首先读取项目根目录的 .claude-structure.json 文件
   - 确认目标路径是否符合项目结构规范
   - 验证文件命名是否遵循约定（PascalCase/camelCase）
   
2. **必须调用 structure-manager subagent**：
   - 如果不确定操作是否符合规范，必须调用 structure-manager subagent
   - 传递操作详情给 subagent 进行验证
   - 等待 subagent 确认后再执行操作

3. **违规处理**：
   - 发现违规时立即停止操作
   - 调用 structure-manager subagent 获取修复建议
   - 向用户说明违规原因和正确做法

**当前项目约束**：
- 项目类型：{{PROJECT_TYPE}}
- 严格模式：已启用
- 源码文件只能放在 src/ 目录下
- 组件使用 PascalCase 命名
- 工具函数使用 camelCase 命名
</system-reminder>
```

### 2. 动态配置机制

通过 .claude-structure.json 文件提供项目特定的规范：

```json
{
  "claudeCodeBehavior": {
    "strictMode": true,
    "autoCallStructureManager": true,
    "operationValidation": {
      "beforeFileCreation": {
        "enabled": true,
        "action": "validate-path-and-name"
      },
      "beforeDirectoryCreation": {
        "enabled": true, 
        "action": "validate-structure"
      }
    }
  },
  "reminders": {
    "fileCreation": "⚠️ 确认文件路径和命名符合 {{PROJECT_TYPE}} 项目规范",
    "directoryCreation": "⚠️ 确认目录结构符合项目架构设计",
    "structureViolation": "❌ 操作违反项目结构规范，请调用 structure-manager 获取帮助"
  }
}
```

### 3. 智能触发机制

#### 文件操作拦截
```markdown
## 文件操作约束

**每次使用 Write、Edit 工具前**：
1. 检查操作是否涉及新文件创建
2. 如果是新文件，自动调用 structure-manager subagent
3. subagent 验证路径和命名合规性
4. 只有通过验证才能继续操作

**示例验证流程**：
用户要求："创建一个新组件 UserCard"
→ Claude Code 识别到这是文件创建操作
→ 自动调用 structure-manager subagent
→ subagent 确认：应创建 src/components/UserCard.jsx
→ 获得确认后执行创建操作
```

#### subagent 自动协作
```markdown
## Structure Manager Subagent 集成

**自动触发条件**：
- 任何文件/目录创建操作
- 检测到潜在的结构违规
- 用户明确要求结构验证

**Subagent 工作流**：
1. 接收操作请求和上下文
2. 读取 .claude-structure.json 配置  
3. 执行合规性验证
4. 返回验证结果和建议
5. 如需要，提供修复方案

**与主 Claude Code 实例协作**：
- 主实例负责接收用户指令
- 自动委托 structure-manager 进行验证
- 根据 subagent 反馈决定是否执行操作
- 确保所有操作都符合项目规范
```

## 优势特点

### 1. 完全原生集成
- 基于 Claude Code 的 system-reminder 机制
- 使用 subagent 系统进行专业化处理
- 无需任何外部脚本或工具

### 2. 智能感知
- 自动识别文件操作意图
- 上下文感知的规范检查
- 动态适应不同项目类型

### 3. 协作友好
- 其他开发者获得相同约束
- 项目规范统一维护
- 支持团队协作场景

### 4. 可维护性
- 配置集中在 .claude-structure.json
- 规范更新通过 /update-rules 命令
- 支持项目演进和规范调整

## 实际效果示例

```
用户：创建一个工具函数来格式化日期

Claude Code 内部流程：
1. 识别到要创建文件
2. 读取 CLAUDE.md 中的 system-reminder
3. 自动调用 structure-manager subagent
4. subagent 验证：应创建 src/utils/formatDate.js
5. 确认符合 camelCase 命名规范
6. 在正确路径创建文件

用户看到的结果：
文件创建在 src/utils/formatDate.js，完全符合项目规范
```