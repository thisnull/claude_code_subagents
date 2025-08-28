---
name: prompt-enhancer
description: Launch development-cues enhancement for technical prompts. Uses Task tool to spawn development-cues-applier for project-methodology integration and concrete development practices enhancement. Outputs enhanced prompt document.
allowed-tools: Task, Write
argument-hint: "<technical_prompt>" (technical prompt that needs development methodology enhancement)
---

🚀 **Development Cues Enhancement Workshop**

Enhance your technical prompts with project-specific development methodology and concrete implementation practices.

## 🔧 Enhancement Workflow

This command uses the `development-cues-applier` agent for project methodology integration:

### Phase 1: Development Cues Application
**Agent**: `development-cues-applier`
- PROMPT_SCENARIOS.md analysis
- Project methodology integration
- Concrete practices enhancement
- Quality validation

### Phase 2: Final Output
**Orchestrator**: This slash command
- Save enhanced prompt to file
- Generate methodology-integrated document
- Ready-to-implement prompt delivery

## 🎯 Process

I will:
1. **Launch Enhancement Agent**: Use Task tool to spawn `development-cues-applier`
   - Provide technical prompt for enhancement
   - Agent will analyze project development practices
   - Apply concrete development methodology to prompt
2. **Generate Output**: 
   - Save development-cues-applier results to file
   - Create comprehensive enhanced prompt document
   - Deliver methodology-integrated prompt

## 🚀 Expected Outcome

You'll receive:
- **Project methodology analysis** from PROMPT_SCENARIOS.md
- **Development-enhanced prompt** with concrete practices
- **Ready-to-implement** prompt with project alignment

## 💡 Usage

Provide your technical prompt that needs development enhancement:

```
/prompt-enhancer "Implement user authentication system with JWT tokens"
```

## 📄 Output File

Each run creates an enhanced prompt document: `refined-prompt/enhanced-prompt-YYYY-MM-DD_HHMMSS.md`

```markdown
# 🎯 DEVELOPMENT-ENHANCED PROMPT

## 📋 Original Technical Requirements
[Preserved input prompt content]

## 🚀 Development Methodology Integration
[Project-specific development practices from development-cues-applier]

## ✅ Enhanced Implementation Framework
[Methodology-integrated prompt ready for implementation]
```

---

## 🤖 Agent Logic

I am the **development enhancement coordinator**. I will:

1. **Task Tool Spawn**: development-cues-applier
   - **Input**: Technical prompt requiring enhancement
   - **Process**: Analyze project practices and enhance prompt with methodology
   - **Completion**: Return enhanced prompt with integrated development cues

2. **Generate Final Document**
   - Save development-cues-applier output directly
   - Structure as methodology-enhanced prompt
   - Save as ready-to-implement file

Let's enhance your prompt with development methodology! 🚀