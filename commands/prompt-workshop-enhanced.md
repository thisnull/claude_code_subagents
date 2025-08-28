---
name: prompt-workshop-enhanced
description: Launch an interactive prompt optimization workshop with dual-agent orchestration. Uses Task tool to coordinate interactive-prompt-refiner and development-cues-applier in sequence for optimal prompt generation with Development Cues integration. Outputs single optimized prompt document.
allowed-tools: Task, Write
argument-hint: "<initial_idea>" (optional initial idea or requirement description)
---

🎯 **Interactive Prompt Optimization Workshop**

Refine and optimize your prompts through dual-agent collaboration with interactive requirements analysis and project methodology enhancement.

## 🔄 Dual-Agent Workflow

I will orchestrate two specialized agents in sequence to create your optimized prompt:

### Phase 1: Requirements Collection & Basic Prompt Generation
**Agent**: `interactive-prompt-refiner`
- Interactive requirements elicitation
- Project context analysis  
- Initial prompt structuring
- Quality scope control

### Phase 2: Development Cues Enhancement
**Agent**: `development-cues-applier`  
- PROMPT_SCENARIOS.md analysis
- Project methodology integration
- Concrete practices integration
- Final prompt enhancement

### Phase 3: Final Integration
**Orchestrator**: This slash command
- Combine both agent outputs into single document
- Generate final optimized prompt
- Save as ready-to-use file

## 🎯 Orchestration Process

I will:
1. **Launch Requirements Agent**: Use Task tool to spawn `interactive-prompt-refiner`
   - Instruct agent to conduct multi-round interactive session with user
   - Agent will ask questions and wait for user responses before proceeding
   - Only move to Phase 2 after interactive requirements gathering is complete
2. **Launch Enhancement Agent**: Use Task tool to spawn `development-cues-applier`
   - Pass Phase 1 results as input for enhancement
   - Preserve all original details while adding development methodology
3. **Generate Final Output**: 
   - Create single comprehensive prompt document
   - Include both requirements analysis and development methodology
   - Save as ready-to-execute prompt

## 🚀 Expected Outcome

You'll receive:
- **Interactive requirements session** for precise requirements
- **Comprehensive enhanced prompt** integrating requirements analysis and development methodology
- **Ready-to-execute** comprehensive prompt document

## 💡 Usage

Simply provide your initial idea or requirement:

```
/prompt-workshop-enhanced "Add authentication to my API"
```

## 📄 Output File

Each run creates a single optimized prompt: `refined-prompt/optimized-prompt-YYYY-MM-DD_HHMMSS.md`

```markdown
# 🎯 OPTIMIZED PROMPT

## 📋 Requirements Analysis
[Complete analysis from interactive-prompt-refiner]

## 🚀 Development-Enhanced Implementation Guide
[Enhanced implementation with project methodology from development-cues-applier]

## ✅ Ready-to-Execute Instructions
[Final consolidated prompt ready for immediate use]
```

---

## 🤖 Agent Orchestration Logic

I am the **orchestration coordinator**. I will:

1. **Task Tool Spawn 1**: interactive-prompt-refiner
   - **Instruction**: Conduct complete multi-round interactive session with user
   - **Process**: Ask questions, wait for responses, refine understanding iteratively  
   - **Completion**: Only finish when comprehensive requirements have been gathered through dialogue

2. **Task Tool Spawn 2**: development-cues-applier  
   - **Input**: Pass complete Phase 1 results with project context
   - **Instruction**: Enhance the basic prompt while preserving all original details

3. **Generate Final Document**
   - Combine both agent outputs into comprehensive prompt
   - Structure as requirements + enhanced implementation
   - Save as single ready-to-use file

Let's create your optimized prompt! 🎯