---
name: init-python-project
description: Initialize a Python project following your preferred structure and best practices using uv package manager, clean directory structure, and development tools setup. Automatically invokes python-project-initializer subagent.
allowed-tools: Task, Bash, Write, Read, Edit
---

Initialize a high-quality Python project following your established preferences by invoking the specialized `python-project-initializer` subagent.

## Execution Flow

```
When user executes /init-python-project:
→ Automatically invokes python-project-initializer subagent
→ Subagent analyzes current directory and project context
→ Creates complete directory structure following your preferences
→ Generates all configuration files with proper tool integration
→ Sets up development environment with uv package manager
→ Updates CLAUDE.md with Python project preferences for future reference
```

## Your Established Preferences

This command implements your specific habits and preferences:

### Package Management
- **uv**: Modern, fast Python packaging tool
- **pyproject.toml**: Modern Python project configuration
- **Development dependencies**: Integrated quality tools

### Directory Structure
- **src/ layout**: Avoids top-level import conflicts
- **Clear separation**: core/, models/, services/, api/, utils/
- **Comprehensive testing**: unit/ and integration/ directories
- **Documentation**: Integrated docs/ structure
- **Operational scripts**: scripts/ for maintenance tasks

### Development Experience
- **Code Quality**: ruff, black, mypy integration
- **Testing**: pytest framework with proper fixture management
- **Logging**: structlog or loguru (modern structured logging)
- **Containerization**: Docker with multi-stage builds (organized in docker/ directory)
- **Configuration**: Centralized config.py management

## Created Project Structure

```
{project-name}/
├── pyproject.toml              # uv dependency management & modern config
├── README.md                   # Comprehensive project documentation
├── .gitignore                  # Python-specific git ignores
├── docker/                     # Container deployment configuration
│   ├── Dockerfile              # Multi-stage container deployment
│   └── docker-compose.yml      # Local development environment
├── docs/                       # Project documentation
│   ├── README.md              # Documentation overview
│   ├── architecture.md        # System architecture
│   ├── api/                   # API documentation
│   └── development.md         # Development guide
├── src/                       # Source code (avoids import conflicts)
│   └── {project_name}/
│       ├── __init__.py
│       ├── core/              # Core business logic
│       ├── models/            # Data models & schemas
│       ├── services/          # Business services layer
│       ├── api/               # API endpoints
│       ├── utils/             # Utility functions
│       ├── logging.py         # Structured logging configuration (structlog/loguru)
│       └── config.py          # Configuration management
├── tests/                     # Comprehensive test suite
│   ├── conftest.py           # pytest configuration & fixtures
│   ├── unit/                 # Unit tests
│   └── integration/          # Integration tests
└── scripts/                  # Operational & maintenance scripts
    ├── setup.sh              # Project setup automation
    ├── deploy.sh             # Deployment script
    └── migrate.py            # Data migration template
```

## Usage Example

```bash
# Initialize Python project
/init-python-project

# After initialization, typical workflow:
uv sync                       # Install all dependencies
uv run pytest               # Run test suite (pytest framework)
uv run ruff check src/      # Run linting
uv run black src/           # Format code
uv run mypy src/            # Type checking

# Docker operations (from docker/ directory)
cd docker && docker-compose up -d  # Start development environment
docker build -f docker/Dockerfile .  # Build production image
```

## Integration Benefits

After running this command:

1. **Preference Memory**: Your Python project preferences are stored in CLAUDE.md
2. **Consistent Structure**: Future Python work follows your established patterns
3. **Modern Tooling**: Latest Python development practices integrated
4. **Quality Automation**: Code quality tools integrated in development workflow
5. **Development Efficiency**: All tools configured and ready to use

## Generated Configuration Features

- **pyproject.toml**: uv-compatible with modern Python packaging standards
- **Development tools**: ruff (linting), black (formatting), mypy (type checking)
- **Testing**: pytest framework with plugins and proper test organization
- **Logging**: structlog or loguru integration for structured logging
- **Docker**: Production-ready containerization organized in docker/ directory
- **Documentation**: Structured docs/ with architectural guidance
- **Scripts**: Operational automation for common tasks

This command establishes your Python project foundation and teaches Claude Code your preferred development patterns for consistent future assistance.