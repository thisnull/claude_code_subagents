---
name: prompt-workshop-enhanced
description: Launch an interactive prompt optimization workshop with dual-agent orchestration. Uses Task tool to coordinate interactive-prompt-refiner and development-cues-applier in sequence for optimal prompt generation with Development Cues integration. Maintains complete debugging logs.
allowed-tools: Task, Write
argument-hint: "<initial_idea>" (optional initial idea or requirement description)
---

🎯 **Advanced Interactive Prompt Optimization Workshop**

Orchestrate a complete prompt optimization workflow using specialized agents in sequence with full debugging capability.

## 🔄 Dual-Agent Workflow with Debug Logging

I will orchestrate two specialized agents in sequence and maintain complete logs for debugging:

### Phase 1: Requirements Collection & Basic Prompt Generation
**Agent**: `interactive-prompt-refiner`
- Deep conversational requirements analysis
- Project context understanding  
- Basic prompt structure creation
- Quality scope control
- **Debug**: Log all inputs and outputs

### Phase 2: Development Cues Enhancement
**Agent**: `development-cues-applier`  
- PROMPT_SCENARIOS.md analysis
- Project methodology integration
- Concrete practices embedding
- Final prompt enhancement
- **Debug**: Log transformation process

### Phase 3: Integration & Complete Documentation
**Orchestrator**: This slash command
- Combine agent outputs
- Generate three-stage documentation
- Save complete debugging log
- **Debug**: Full workflow trace

## 🎯 Orchestration Process with Debugging

I will:
1. **Create Debug Session**: Initialize timestamped debug file
2. **Launch Requirements Agent**: Use Task tool to spawn `interactive-prompt-refiner`
   - Log input parameters
   - Monitor and log output
3. **Launch Enhancement Agent**: Use Task tool to spawn `development-cues-applier`
   - Log input (basic prompt + context)
   - Monitor and log enhanced output
4. **Integration & Documentation**: 
   - Log integration process
   - Create three-stage documentation
   - Save complete debug trace

## 🚀 Expected Outcome

You'll receive:
- **Interactive consultation** for precise requirements
- **Project-methodology-aware prompt** with concrete Development Cues
- **Three-stage documentation** showing complete transformation
- **Complete debug log** with all inputs/outputs for troubleshooting
- **Ready-to-execute** optimized prompts

## 💡 Usage

Simply provide your initial idea or requirement:

```
/prompt-workshop-enhanced "Add authentication to my API"
```

## 🐛 Debug File Structure

Each run creates a debug file: `refined-prompt/debug-YYYY-MM-DD_HHMMSS.md`

```markdown
# 🐛 PROMPT WORKSHOP DEBUG LOG

## Session Info
- **Timestamp**: YYYY-MM-DD HH:MM:SS
- **User Input**: [Original request]
- **Orchestrator**: prompt-workshop-enhanced

## Phase 1: Interactive Prompt Refiner
### Input to Agent:
[Logged input parameters]

### Agent Output:
[Complete output from interactive-prompt-refiner]

### Notes:
[Any issues or observations]

## Phase 2: Development Cues Applier  
### Input to Agent:
[Basic prompt + context passed to development-cues-applier]

### Agent Output:
[Complete enhanced prompt output]

### Notes:
[Transformation observations]

## Phase 3: Integration
### Integration Process:
[How outputs were combined]

### Final Three-Stage Document:
[Reference to the main output file]

### Session Summary:
[Overall success/failure, timing, issues]
```

---

## 🤖 Agent Orchestration Logic

I am the **orchestration coordinator with full debugging**. I will:

1. **Initialize Debug Session**
   - Create timestamped debug file
   - Log initial user input

2. **Task Tool Spawn 1**: interactive-prompt-refiner
   - Log: Input parameters sent to agent
   - Monitor: Conversation progress  
   - Log: Complete output received
   - Note: Any issues or observations

3. **Task Tool Spawn 2**: development-cues-applier  
   - Log: Basic prompt + context sent to agent
   - Monitor: Development Cues integration process
   - Log: Enhanced prompt received
   - Note: Transformation quality and issues

4. **Result Integration with Logging**
   - Log: Integration process steps
   - Create: Three-stage documentation
   - Save: Both main output and debug log
   - Summary: Complete workflow trace

Let's begin the orchestrated workflow with full debugging! 🎯