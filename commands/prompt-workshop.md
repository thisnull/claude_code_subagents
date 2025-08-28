---
name: prompt-workshop
description: Launch interactive prompt optimization workshop. Uses Task tool to spawn interactive-prompt-refiner for comprehensive requirements analysis and prompt generation. Outputs optimized prompt document.
allowed-tools: Task, Write
argument-hint: "<initial_idea>" (optional initial idea or requirement description)
---

🎯 **Interactive Prompt Optimization Workshop**

Refine and optimize your prompts through professional interactive requirements analysis and customized prompt generation.

## 🤝 Interactive Workflow

This command uses the `interactive-prompt-refiner` agent for comprehensive prompt optimization:

### Phase 1: Requirements Collection & Prompt Generation
**Agent**: `interactive-prompt-refiner`
- Interactive requirements elicitation
- Project context analysis  
- Complete prompt generation
- Quality optimization

### Phase 2: Final Output
**Orchestrator**: This slash command
- Save optimized prompt to file
- Generate comprehensive prompt document
- Ready-to-use prompt delivery

## 🎯 Process

I will:
1. **Launch Interactive Agent**: Use Task tool to spawn `interactive-prompt-refiner`
   - Instruct agent to conduct multi-round interactive session with user
   - Agent will ask questions and wait for user responses before proceeding
   - Complete full requirements gathering and prompt generation process
2. **Generate Output**: 
   - Save interactive-prompt-refiner results to file
   - Create comprehensive optimized prompt document
   - Deliver ready-to-use prompt

## 🚀 Expected Outcome

You'll receive:
- **Interactive requirements session** for precise requirements
- **Complete optimized prompt** from interactive analysis
- **Ready-to-use** prompt document for immediate application

## 💡 Usage

Simply provide your initial idea or requirement:

```
/prompt-workshop "Add authentication to my API"
```

## 📄 Output File

Each run creates an optimized prompt document: `refined-prompt/optimized-prompt-YYYY-MM-DD_HHMMSS.md`

```markdown
# 🎯 OPTIMIZED PROMPT

## 📋 Interactive Requirements Analysis
[Complete output from interactive-prompt-refiner agent]

## ✅ Ready-to-Execute Instructions
[Final optimized prompt ready for immediate use]
```

---

## 🤖 Agent Logic

I am the **prompt optimization coordinator**. I will:

1. **Task Tool Spawn**: interactive-prompt-refiner
   - **Instruction**: Conduct complete multi-round interactive session with user
   - **Process**: Ask questions, wait for responses, refine understanding iteratively  
   - **Completion**: Only finish when comprehensive requirements have been gathered through dialogue

2. **Generate Final Document**
   - Save interactive-prompt-refiner output directly
   - Structure as comprehensive optimized prompt
   - Save as ready-to-use file

Let's create your optimized prompt! 🎯