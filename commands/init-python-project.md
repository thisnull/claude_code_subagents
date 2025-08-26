---
name: init-python-project
description: Initialize a Python project following your preferred structure and best practices using uv package manager, clean directory structure, and development tools setup. Automatically invokes python-project-initializer subagent. Supports intelligent project analysis from requirement documents.
allowed-tools: Task, Bash, Write, Read, Edit
argument-hint: [file1] [file2] [file3] ... (optional requirement/design documents)
---

Initialize a high-quality Python project following your established preferences by invoking the specialized `python-project-initializer` subagent with intelligent document analysis capabilities.

## Command Usage

```bash
# Basic initialization (interactive project type selection)
/init-python-project

# Intelligent initialization with document analysis
/init-python-project requirements.md
/init-python-project PRD.md design-doc.pdf architecture.txt
/init-python-project README.md project-spec.docx api-design.yaml
```

## Execution Flow

```
When user executes /init-python-project [documents...]:
→ Automatically invokes python-project-initializer subagent
→ If documents provided: Analyzes documents to determine project type and architecture
→ If no documents: Interactive prompts for project type and requirements
→ Creates complete directory structure following your preferences
→ Generates project-specific module organization based on analysis
→ Sets up development environment with uv package manager
→ Updates CLAUDE.md with Python project preferences for future reference
```

## Intelligent Document Analysis

The command can analyze various document types to understand your project:

### Supported Document Types
- **Requirements Documents**: `.md`, `.txt`, `.docx`, `.pdf`
- **Design Documents**: Architecture specs, system design, API documentation
- **Project Plans**: Development roadmaps, feature specifications
- **Existing Code**: Sample files, prototypes, legacy code references
- **Configuration Files**: API schemas (`.yaml`, `.json`), database schemas

### Analysis Capabilities
- **Project Type Detection**: Web API, CLI tool, data pipeline, microservice, library, etc.
- **Architecture Pattern Recognition**: REST API, GraphQL, event-driven, batch processing
- **Technology Stack Inference**: Database requirements, external integrations, frameworks
- **Module Structure Planning**: Domain boundaries, service layers, data models
- **Integration Requirements**: Third-party APIs, message queues, storage systems

### Example Analysis Results

**Input**: `requirements.md` containing "user authentication, product catalog, shopping cart, payment processing"
**Result**: E-commerce web API project with modules:
```
src/myproject/
├── auth/          # User authentication & authorization
├── catalog/       # Product catalog management
├── cart/          # Shopping cart functionality
├── payments/      # Payment processing
├── orders/        # Order management
├── api/           # REST API endpoints
└── models/        # Shared data models
```

**Input**: `data-pipeline-spec.pdf` describing ETL workflows
**Result**: Data pipeline project with modules:
```
src/myproject/
├── extractors/    # Data extraction components
├── transformers/  # Data transformation logic
├── loaders/       # Data loading mechanisms
├── pipeline/      # Workflow orchestration
├── storage/       # Storage adapters
└── monitoring/    # Pipeline monitoring
```

## Your Established Preferences

This command implements your specific habits and preferences:

### Package Management
- **uv**: Modern, fast Python packaging tool
- **pyproject.toml**: Modern Python project configuration
- **Development dependencies**: Integrated quality tools

### Directory Structure
- **src/ layout**: Avoids top-level import conflicts
- **Adaptive organization**: Module structure adapts to project type and domain
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
│   └── {project_name}/        # Main package (structure adapts to project type)
│       ├── __init__.py
│       ├── config.py          # Configuration management
│       └── logging.py         # Structured logging configuration (structlog/loguru)
├── tests/                     # Comprehensive test suite
│   ├── conftest.py           # pytest configuration & fixtures
│   ├── unit/                 # Unit tests
│   └── integration/          # Integration tests
└── scripts/                  # Operational & maintenance scripts
    ├── setup.sh              # Project setup automation
    ├── deploy.sh             # Deployment script
    └── migrate.py            # Data migration template
```

**Note**: The source code structure within `src/{project_name}/` adapts to your project type:
- **Web APIs**: api/, models/, services/, core/
- **CLI Tools**: cli/, commands/, core/, utils/  
- **Libraries**: core/, utils/, exceptions/
- **Data Pipelines**: pipeline/, processors/, transformers/
- **Microservices**: handlers/, domain/, infrastructure/

The initializer will detect or prompt for project type and create appropriate module structure.

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