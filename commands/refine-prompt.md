---
name: refine-prompt
description: Simple and fast prompt refinement tool that transforms brief user inputs into detailed, actionable instructions. Optionally adds project-specific workflow requirements from PROMPT_SCENARIOS.md when --with-scenarios flag is used.
allowed-tools: Read
argument-hint: "<brief_prompt>" [--with-scenarios] (add --with-scenarios to include project workflow requirements)
---

Transform your brief prompts into clear, detailed instructions and optionally add project workflow requirements.

**IMPORTANT: This command generates and displays refined prompts for you to copy and use - it does NOT execute the prompts.**

## Command Usage

```bash
# Basic prompt refinement (Step 1 only)
/refine-prompt "Add user authentication"
# → Returns detailed technical requirements only

# Enhanced with project scenarios (Step 1 + Step 2)
/refine-prompt "Add user authentication" --with-scenarios
# → Returns technical requirements + project workflow reminders

# Bug fixing with workflows
/refine-prompt "Fix login issue" --with-scenarios
# → Returns debugging steps + testing and documentation requirements
```

## Two-Step Enhancement Process

### Step 1: Prompt Refinement (Always)
- **Analyze** your brief input for intent and scope
- **Expand** with specific technical details and actionable steps  
- **Clarify** requirements, constraints, and expected outcomes
- **Format** as detailed, actionable instructions

### Step 2: Scenario Enhancement (Optional with --with-scenarios)
- **Read** PROMPT_SCENARIOS.md for project-specific workflows
- **Detect** matching scenarios based on keywords in refined prompt
- **Append** relevant workflow requirements as additional sections
- **Integrate** seamlessly with technical requirements

## Output Formats

### Basic Output (without --with-scenarios)
```markdown
# 🔄 Refined Prompt (Ready to Copy)

[Detailed technical requirements and implementation steps]

---
## 📋 How to Use  
1. Review the refined prompt above
2. Copy it if it meets your needs
3. Paste it into a new Claude Code session
4. Modify as needed for your specific requirements
```

### Enhanced Output (with --with-scenarios)
```markdown
# 🚀 Enhanced Prompt (Ready to Copy)

## 📋 Technical Requirements
[Detailed technical requirements and implementation steps from Step 1]

## ⚠️ Project Workflow Requirements
Based on detected scenarios: [Scenario Names]

### 🎯 Feature Development
- 开发前更新需求文档和设计文档
- 开发完成后编写单元测试和集成测试

### 🎯 API Changes
- 更新API文档和接口规范
- 进行API集成测试和契约测试

---
## 📋 How to Use
1. Review both technical and workflow requirements
2. Copy the entire enhanced prompt if it looks good
3. Use it in your next Claude Code session  
4. Modify any parts that don't fit your needs
```

## Scenario Detection (when --with-scenarios is used)

The system automatically detects relevant scenarios by matching keywords:

**Example Keywords:**
- **Feature Development**: implement, add, create, build, develop, new, feature
- **Bug Fixing**: fix, bug, issue, problem, error, debug
- **API Changes**: api, endpoint, route, rest, interface  
- **Database Changes**: database, schema, migration, table, column
- **Testing**: test, testing, unit, integration, e2e

## PROMPT_SCENARIOS.md Integration

When using `--with-scenarios`:

**If PROMPT_SCENARIOS.md exists:**
- Reads your custom project scenarios and requirements
- Matches scenarios based on your defined trigger keywords
- Adds your specific workflow requirements

**If PROMPT_SCENARIOS.md doesn't exist:**
- Uses built-in basic scenarios
- Still provides common workflow reminders
- Suggests creating PROMPT_SCENARIOS.md for customization

## Benefits

### Basic Mode (Step 1 only)
- **Fast Generation**: Lightweight, proven prompt refinement
- **Clear Output**: Immediate technical details ready to copy
- **No Dependencies**: Works without any configuration files
- **Focused Purpose**: Pure technical prompt enhancement

### Enhanced Mode (Step 1 + Step 2)  
- **Complete Workflow**: Technical details + project requirements
- **Never Forget**: Automatic workflow reminders
- **Project Aware**: Customizable scenarios via PROMPT_SCENARIOS.md
- **Team Consistency**: Standardized workflow enforcement

This progressive enhancement approach lets you choose the level of detail you need: basic technical refinement or complete project-aware enhancement.