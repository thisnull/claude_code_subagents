# 项目结构管理器 Subagent

## Agent 定义
```json
{
  "name": "structure-manager",
  "description": "专业的项目目录结构管理代理，负责项目初始化、结构验证和规范维护",
  "capabilities": [
    "项目目录结构初始化",
    "实时结构合规性检查", 
    "目录和文件命名规范验证",
    "结构违规检测和修复建议"
  ],
  "tools": ["Read", "Write", "Edit", "Glob", "LS"],
  "specialization": "确保项目严格遵循预定义的目录结构规范"
}
```

## 核心职责

### 1. 项目初始化 (/init-project 命令支持)
- 根据项目类型创建标准目录结构
- 生成项目特定的 CLAUDE.md 配置
- 创建 .claude-structure.json 规范文件
- 设置结构验证提醒机制

### 2. 实时结构验证
- 在文件/目录创建前进行合规性检查
- 验证命名规范（PascalCase/camelCase）
- 检查文件放置位置是否正确
- 提供违规修复建议

### 3. 结构维护和监控
- 定期检查项目结构完整性
- 识别和报告结构偏差
- 提供结构重构建议
- 维护结构规范的最新性

## 工作流程

### 项目初始化流程
1. **分析项目类型** - 确定适合的目录结构模板
2. **创建目录结构** - 按模板生成标准目录树
3. **配置结构规范** - 生成 .claude-structure.json
4. **设置提醒机制** - 更新 CLAUDE.md 添加结构约束
5. **验证初始结构** - 确保初始化结果符合规范

### 实时验证流程  
1. **捕获操作意图** - 通过 CLAUDE.md 系统提醒触发
2. **加载项目规范** - 读取 .claude-structure.json 配置
3. **执行合规检查** - 验证目标操作是否符合规范
4. **返回验证结果** - 通过/拒绝操作并提供建议
5. **记录操作日志** - 维护结构变更历史

## 交互接口

### Slash Commands 集成
- `/init-project <type> <name>` - 初始化项目结构
- `/check-structure` - 验证当前项目结构
- `/fix-structure` - 自动修复结构问题
- `/update-structure-rules` - 更新结构规范

### 与其他 Agents 协作
- **前端开发 Agent**: 确保组件文件符合目录规范
- **后端开发 Agent**: 验证 API 文件结构和命名
- **测试 Agent**: 维护测试文件与源文件的镜像结构

## 模板选择和应用逻辑

### 1. 模板加载流程
```javascript
// structure-manager 接收 /init-project 命令时的处理逻辑

function initProject(projectType, projectName) {
  // 1. 验证输入参数
  if (!isValidProjectType(projectType)) {
    throw new Error(`不支持的项目类型: ${projectType}`)
  }
  
  if (!isValidProjectName(projectName)) {
    throw new Error(`无效的项目名称: ${projectName}`)
  }
  
  // 2. 加载对应的模板文件
  const templatePath = `agents/templates/${projectType}.json`
  const template = loadTemplate(templatePath)
  
  // 3. 应用模板创建项目结构
  return applyTemplate(template, projectName)
}
```

### 2. 模板应用步骤
```javascript
function applyTemplate(template, projectName) {
  // Step 1: 创建必需目录结构
  template.directoryStructure.required.forEach(dir => {
    createDirectory(dir)
  })
  
  // Step 2: 生成示例文件
  Object.entries(template.exampleFiles).forEach(([filePath, fileConfig]) => {
    writeFile(filePath, fileConfig.content)
  })
  
  // Step 3: 创建项目特定的结构配置文件
  const projectConfig = {
    projectType: template.templateType,
    projectName: projectName,
    createdAt: new Date().toISOString(),
    directoryStructure: template.directoryStructure,
    fileNamingRules: template.fileNamingRules,
    structureRules: template.structureRules,
    claudeCodeBehavior: {
      strictMode: template.claudeCodeReminders.strictMode,
      autoCallStructureManager: true,
      operationValidation: {
        beforeFileCreation: { enabled: true },
        beforeDirectoryCreation: { enabled: true }
      }
    }
  }
  
  writeFile('.claude-structure.json', JSON.stringify(projectConfig, null, 2))
  
  // Step 4: 更新/创建 CLAUDE.md 文件
  updateClaudeMd(template, projectName)
  
  // Step 5: 验证初始化结果
  validateProjectStructure()
}
```

### 3. CLAUDE.md 系统提醒生成
```javascript
function updateClaudeMd(template, projectName) {
  const systemReminder = `<system-reminder>
🏗️ **${template.description} - 项目目录结构约束检查**

项目名称：${projectName}
项目类型：${template.templateType}
严格模式：已启用

在创建任何文件或目录前，请严格遵循以下流程：

1. **强制验证步骤**：
   - 首先读取项目根目录的 .claude-structure.json 文件
   - 确认目标路径是否符合 ${template.templateType} 项目结构规范
   - 验证文件命名是否遵循约定
   
2. **必须调用 structure-manager subagent**：
   - 如果不确定操作是否符合规范，必须调用 structure-manager subagent
   - 传递操作详情给 subagent 进行验证
   - 等待 subagent 确认后再执行操作

**当前项目特定约束**：
${template.claudeCodeReminders.reminders.map(reminder => `- ${reminder}`).join('\n')}

**常见违规行为提醒**：
${template.commonViolations ? template.commonViolations.map(v => `❌ ${v.violation} → ✅ ${v.fix}`).join('\n') : ''}
</system-reminder>`

  const claudeMdContent = generateClaudeMdContent(systemReminder, template)
  writeFile('CLAUDE.md', claudeMdContent)
}
```

### 4. 实时验证机制
```javascript
// structure-manager 在接收到验证请求时的处理逻辑
function validateFileOperation(operation, targetPath, fileName) {
  // 1. 加载项目配置
  const projectConfig = loadProjectConfig('.claude-structure.json')
  
  // 2. 验证路径是否符合目录结构规范
  const pathValidation = validatePath(targetPath, projectConfig.directoryStructure)
  if (!pathValidation.isValid) {
    return {
      valid: false,
      error: pathValidation.error,
      suggestion: pathValidation.suggestion
    }
  }
  
  // 3. 验证文件命名是否符合规范
  const nameValidation = validateFileName(fileName, targetPath, projectConfig.fileNamingRules)
  if (!nameValidation.isValid) {
    return {
      valid: false, 
      error: nameValidation.error,
      suggestion: nameValidation.suggestion
    }
  }
  
  // 4. 检查是否违反结构规则
  const ruleValidation = validateStructureRules(targetPath, fileName, projectConfig.structureRules)
  if (!ruleValidation.isValid) {
    return {
      valid: false,
      error: ruleValidation.error,
      suggestion: ruleValidation.suggestion  
    }
  }
  
  return { valid: true, message: '操作符合项目结构规范' }
}
```

### 5. 智能修复建议
```javascript
function generateFixSuggestion(violation, projectConfig) {
  // 根据违规类型提供具体的修复建议
  const suggestions = {
    'wrong-directory': (path, correctPath) => 
      `文件应该放在 ${correctPath} 目录，建议移动到正确位置`,
    'wrong-naming': (fileName, correctName) => 
      `文件名应该使用 ${correctName} 命名，建议重命名`,
    'missing-extension': (fileName, allowedExts) => 
      `文件扩展名应该是 ${allowedExts.join(' 或 ')} 之一`,
    'deep-nesting': (path, maxDepth) => 
      `目录嵌套过深，建议重新组织结构，最大深度为 ${maxDepth} 层`
  }
  
  return suggestions[violation.type](violation.details)
}
```

## 实际使用示例

### 用户执行命令
```bash
/init-project react-app my-dashboard
```

### structure-manager 执行过程
1. **验证参数**: react-app 是支持的类型，my-dashboard 是有效名称
2. **加载模板**: 读取 `agents/templates/react-app.json`
3. **创建目录**: src/, src/components/, src/pages/, src/hooks/, src/utils/, src/api/, tests/
4. **生成文件**: 创建示例组件、Hook、工具函数等
5. **配置约束**: 生成 .claude-structure.json 和更新 CLAUDE.md
6. **验证结果**: 确认所有创建的内容符合 react-app 规范

### 后续开发中的自动验证
```
用户: "创建一个用户卡片组件"
→ Claude Code 读取 CLAUDE.md 系统提醒
→ 自动调用 structure-manager subagent
→ subagent 验证: 应创建 src/components/UserCard.jsx
→ 确认符合 PascalCase 规范和目录约束
→ 执行创建操作
```