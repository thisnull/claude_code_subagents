# 项目类型模板管理机制

## 模板存储结构

所有项目类型的目录结构规范都定义在 `agents/templates/` 目录中：

```
agents/templates/
├── react-app.json         # React 单页应用模板
├── vue-app.json           # Vue.js 应用模板  
├── api-service.json       # 后端 API 服务模板
├── fullstack-web.json     # 全栈 Web 项目模板
├── mobile-app.json        # 移动应用模板
├── library.json           # 组件库/工具库模板
└── template-schema.json   # 模板规范定义
```

## 模板文件结构

每个模板文件包含以下核心部分：

### 1. 基本信息
```json
{
  "templateType": "react-app",
  "description": "React 单页应用项目结构模板", 
  "version": "1.0.0"
}
```

### 2. 目录结构定义
```json
{
  "directoryStructure": {
    "required": ["src/", "src/components/", "tests/"],
    "optional": ["docs/", "src/types/"],
    "forbidden": ["component/", "src/util/"]
  }
}
```

### 3. 文件命名规范
```json
{
  "fileNamingRules": {
    "components": {
      "pattern": "PascalCase",
      "extensions": [".jsx", ".tsx"],
      "examples": ["UserCard.jsx"]
    }
  }
}
```

### 4. 结构规则约束
```json
{
  "structureRules": [
    {
      "rule": "components-in-src",
      "description": "组件必须放在 src/components/ 目录",
      "violation": "在其他位置创建组件",
      "correct": "src/components/ComponentName.jsx"
    }
  ]
}
```

### 5. 示例文件内容
```json
{
  "exampleFiles": {
    "src/components/Example.jsx": {
      "content": "React 组件的实际代码内容",
      "description": "示例组件说明"
    }
  }
}
```

### 6. Claude Code 提醒配置
```json
{
  "claudeCodeReminders": {
    "strictMode": true,
    "reminders": [
      "React 组件必须使用 PascalCase 命名",
      "组件文件放在 src/components/ 目录"
    ]
  }
}
```

## structure-manager Subagent 使用模板的流程

### 1. 模板加载
```javascript
// structure-manager 收到 /init-project react-app myapp 命令时
1. 读取 agents/templates/react-app.json 文件
2. 解析模板配置信息
3. 验证模板完整性和有效性
```

### 2. 目录创建
```javascript
// 根据模板的 directoryStructure.required 创建目录
foreach (directory in template.directoryStructure.required) {
  createDirectory(projectRoot + directory)
}
```

### 3. 示例文件生成
```javascript
// 根据模板的 exampleFiles 创建示例代码
foreach (file, config in template.exampleFiles) {
  writeFile(projectRoot + file, config.content)
}
```

### 4. 配置文件生成
```javascript
// 生成项目特定的 .claude-structure.json
const projectConfig = {
  projectType: template.templateType,
  projectName: userInputName,
  ...template.directoryStructure,
  ...template.fileNamingRules,
  ...template.structureRules,
  ...template.claudeCodeReminders
}
writeFile('.claude-structure.json', projectConfig)
```

### 5. CLAUDE.md 更新
```javascript
// 将模板的提醒信息嵌入到项目的 CLAUDE.md
const systemReminder = generateSystemReminder(template.claudeCodeReminders)
updateClaudeMd(systemReminder)
```

## 模板扩展和定制

### 1. 添加新项目类型
1. 在 `agents/templates/` 目录创建新的 JSON 模板文件
2. 按照 template-schema.json 规范定义结构
3. 更新 `/init-project` 命令的支持列表

### 2. 修改现有模板
1. 直接编辑对应的 JSON 模板文件
2. 使用 `/update-rules` 命令应用到现有项目

### 3. 项目特定定制
1. 修改项目根目录的 `.claude-structure.json` 文件
2. 通过 `/update-rules` 命令交互式修改规范

## 模板版本管理

每个模板包含版本信息，支持：
- 模板升级和兼容性检查
- 项目迁移到新版本模板
- 模板变更历史追踪