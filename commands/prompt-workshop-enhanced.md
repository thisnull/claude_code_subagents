---
name: prompt-workshop-enhanced
description: Launch an interactive prompt optimization workshop with dual-agent orchestration. Uses Task tool to coordinate interactive-prompt-refiner and development-cues-applier in sequence for optimal prompt generation with Development Cues integration. Records complete workflow for reference.
allowed-tools: Task, Write
argument-hint: "<initial_idea>" (optional initial idea or requirement description)
---

🎯 **Advanced Interactive Prompt Optimization Workshop**

Orchestrate a complete prompt optimization workflow using specialized agents in sequence with full debugging capability.

## 🔄 Dual-Agent Workflow with Process Recording

I will orchestrate two specialized agents in sequence and record the complete process for your reference:

### Phase 1: Requirements Collection & Basic Prompt Generation
**Agent**: `interactive-prompt-refiner`
- Deep conversational requirements analysis
- Project context understanding  
- Basic prompt structure creation
- Quality scope control

### Phase 2: Development Cues Enhancement
**Agent**: `development-cues-applier`  
- PROMPT_SCENARIOS.md analysis
- Project methodology integration
- Concrete practices embedding
- Final prompt enhancement

### Phase 3: Integration & Complete Documentation
**Orchestrator**: This slash command
- Combine agent outputs
- Generate three-stage documentation
- Save complete workflow record

## 🎯 Orchestration Process

I will:
1. **Initialize Session**: Create timestamped workflow record
2. **Launch Requirements Agent**: Use Task tool to spawn `interactive-prompt-refiner`
   - If user provided initial idea: Pass it as context
   - If no initial idea: Instruct agent to begin structured questioning immediately
3. **Launch Enhancement Agent**: Use Task tool to spawn `development-cues-applier`
   - Pass Phase 1 results as input for enhancement
   - Preserve all original details while adding development methodology
4. **Generate Final Output**: 
   - Create three-stage documentation
   - Save workflow record with agent inputs/outputs

## 🚀 Expected Outcome

You'll receive:
- **Interactive consultation** for precise requirements
- **Project-methodology-aware prompt** with concrete Development Cues
- **Three-stage documentation** showing complete transformation
- **Workflow record** with agent inputs/outputs for reference
- **Ready-to-execute** optimized prompts

## 💡 Usage

Simply provide your initial idea or requirement:

```
/prompt-workshop-enhanced "Add authentication to my API"
```

## 📄 Workflow Record Structure

Each run creates a workflow record: `refined-prompt/workflow-YYYY-MM-DD_HHMMSS.md`

```markdown
# 📄 PROMPT WORKSHOP WORKFLOW RECORD

## Session Info
- **Timestamp**: YYYY-MM-DD HH:MM:SS
- **User Input**: [Original request]
- **Orchestrator**: prompt-workshop-enhanced

## Phase 1: Requirements Collection
### Input to interactive-prompt-refiner:
[What was sent to the agent]

### Output from interactive-prompt-refiner:
[Complete requirements analysis and basic prompt]

## Phase 2: Development Cues Enhancement  
### Input to development-cues-applier:
[Basic prompt + context passed to enhancement agent]

### Output from development-cues-applier:
[Enhanced prompt with development methodology]

## Final Result
### Generated Documentation:
[Reference to the main output file]

### Process Summary:
[Brief summary of the workflow completion]
```

---

## 🤖 Agent Orchestration Logic

I am the **orchestration coordinator**. I will:

1. **Initialize Session**
   - Create timestamped workflow record file
   - Begin dual-agent process

2. **Task Tool Spawn 1**: interactive-prompt-refiner
   - **If user provided initial idea**: Pass as context with instruction to build upon it
   - **If no initial idea provided**: Send instruction to begin immediate structured questioning with these prompts:
     * "What specific task do you want Claude to help you accomplish?"
     * "What is your project context and requirements?"
     * "What should the final prompt enable Claude to do?"

3. **Task Tool Spawn 2**: development-cues-applier  
   - **Input**: Pass complete Phase 1 results with project context
   - **Instruction**: Enhance the basic prompt while preserving all original details

4. **Generate Results**
   - Create three-stage documentation
   - Complete workflow record with all agent inputs/outputs
   - Present final optimized prompt

Let's begin the prompt optimization workshop! 🎯