---
name: init-docs
description: Initialize complete documentation structure for projects by invoking the docs-manager subagent to create standardized directory hierarchy and establish documentation management mechanisms.
---

Automatically create a comprehensive documentation structure for any project by invoking the `docs-manager` subagent.

## Command Format
```
/init-docs
```

## Execution Flow
```
When user executes /init-docs command:
→ Automatically triggers docs-manager subagent
→ Subagent creates complete documentation directory structure
→ Generates corresponding README.md files in each directory
→ Updates project CLAUDE.md with documentation management constraints
```

## Expected Output
- Complete docs/ directory structure (created via Claude Code Write tool)
- README.md index files for each directory
- Updated CLAUDE.md (including documentation management constraints and reminder mechanisms)
- Established documentation consistency and sync mechanisms
- Quality standards and maintenance guidelines

## Documentation Architecture Created
The command creates a standardized documentation structure including:
- Meta-documents and management (00-meta/)
- Product and requirement documents (10-product/)
- Architecture and design documents (20-architecture/)
- Integration architecture (25-integration/)
- Engineering and development practices (30-engineering/)
- Testing and quality assurance (40-quality/)
- CI/CD and delivery (50-delivery/)
- Operations and SRE (60-operations/)
- Data and analytics (70-data-analytics/)
- Project management (80-project/)
- User-facing documentation (90-user-docs/)
- Legal and compliance (95-legal/)
- Research documents (96-research/)
- Deployment documentation (97-deployment/)
- Archived documents (98-archive/)
- Development logs (99-development-log/)

## Usage Examples
```bash
/init-docs     # Create standard documentation system in current project
```

## Integration Features
After initialization, Claude Code will:
- Automatically remind about documentation updates when code/API/architecture changes
- Enforce documentation-driven development practices
- Maintain cross-document consistency checks
- Ensure version synchronization across all documentation
- Maintain terminology alignment standards
- Monitor completeness, accuracy, and maintainability quality standards

This command establishes a professional documentation foundation that enhances project maintainability and team collaboration.