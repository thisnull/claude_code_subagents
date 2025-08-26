# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository is designed to implement and maintain **custom Claude Code Subagents and Slash Commands** to meet personal usage habits and development needs. The goal is to quickly define, extend, and debug a personal intelligent agent ecosystem to improve work efficiency and flexibility in Claude Code.

## Architecture

- **agents/**: Directory for custom subagent definitions and implementations
- **commands/**: Directory for custom slash command definitions and implementations

## Language Preference

This project documentation and code comments are primarily in Chinese (中文). Follow the existing language patterns when contributing to the codebase.

## Development Goals

- Customize commonly used commands and subagents according to personal habits
- Build modular, reusable Subagent templates
- Facilitate convenient debugging, iteration, and maintenance
- Support long-term expansion and team collaboration

## Project Status

This is a new repository with basic structure established. The main focus areas are:

1. **Personal Customization**: Tailoring Claude Code functionality to individual preferences
2. **Modularity**: Creating reusable templates and components
3. **Extensibility**: Building a foundation for future expansion
4. **Team Collaboration**: Enabling collaborative development of custom agents

## Available Custom Commands

### Document Management Commands
- **/init-docs**: Initialize complete documentation structure for projects
  - Automatically creates standardized docs/ directory with full hierarchy
  - Generates templates, README files, and documentation standards
  - Establishes document consistency and sync mechanisms

## Custom Subagents

### docs-manager
专业的文档架构管理专家，负责项目文档体系的初始化、维护和一致性保障。

**核心功能:**
- 标准文档目录结构创建和管理
- 文档模板库维护和应用
- 文档依赖关系追踪和一致性检查
- Claude Code集成约束和自动化提醒机制

**使用场景:**
- 新项目文档体系初始化
- 现有项目文档规范化改造  
- 文档质量和一致性维护
- 团队文档协作流程建立

## Document Management Integration

When working on projects that use the /init-docs command, Claude Code will:

### Automatic Documentation Awareness
- **Code Changes**: When modifying code, automatically remind about related documentation updates
- **API Changes**: When API interfaces change, prompt to update API docs, test cases, and user documentation
- **Architecture Changes**: When system architecture changes, remind to update architecture docs, deployment guides, and operational manuals

### Documentation-Driven Development
- **Feature Development**: Before implementing new features, remind to update design documents first
- **Testing**: Tests must be executed based on the latest test documentation
- **Deployment**: Deployment must reference the deployment documentation

### Consistency Checks
- **Cross-Document Consistency**: Regularly check consistency between PRD, API docs, and test cases
- **Version Synchronization**: Ensure version information consistency across all documentation
- **Terminology Alignment**: Maintain consistent terminology usage across all documents

### Quality Standards
- **Completeness**: Ensure all necessary documentation is created and maintained
- **Accuracy**: Keep documentation synchronized with actual code and product features  
- **Usability**: Maintain clear structure and easy navigation
- **Maintainability**: Establish sustainable long-term documentation maintenance processes

## Notes

- No build system or dependency management is currently configured
- The repository uses Python-style .gitignore, suggesting Python may be used for implementations
- This is a development framework project rather than an application with typical build/test/deploy cycles
- All documentation structure and templates are built into the docs-manager subagent