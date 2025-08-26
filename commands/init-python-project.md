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

# Intelligent initialization with markdown document analysis
/init-python-project requirements.md
/init-python-project PRD.md design-doc.md architecture.md
/init-python-project README.md project-spec.md api-design.md
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
- **Markdown Documents**: `.md` format only
- **Common Document Types**: Requirements docs, design specs, README files, API documentation
- **Project Plans**: Development roadmaps, feature specifications (in markdown)
- **Technical Specs**: Architecture docs, system design, database schemas (in markdown)

### Analysis Capabilities
- **Multi-Application Detection**: Identifies distinct application types within the same project
- **Application-Centric Architecture**: Each application type becomes an independent module with its own internal structure
- **Shared Infrastructure Planning**: Extracts common functionality to shared/ module
- **Inter-Application Interface Design**: Plans communication between different applications
- **Technology Stack Inference**: Database requirements, external integrations, frameworks

### Example Analysis Results

**Single Application Project:**
**Input**: `requirements.md` containing "REST API for user management with authentication endpoints"
**Result**: Web API application project:
```
src/user_management/
├── web_api/           # Single Web API application
│   ├── api/
│   │   └── v1/
│   │       ├── auth.py      # Authentication endpoints
│   │       └── users.py     # User management endpoints
│   ├── schemas/       # Request/response models
│   ├── services/      # Business logic
│   └── dependencies/  # FastAPI dependencies
├── shared/
│   ├── core/
│   ├── models/        # User data models
│   └── config/
└── __init__.py
```

**Multi-Application Project:**
**Input**: `project-spec.md` containing "LLM agent system with REST API endpoints and CLI interface for management"
**Detected Applications**: LLM Agents + Web API + CLI Application
**Result**: Multi-application architecture:
```
src/intelligent_system/
├── llm_agents/        # LLM应用 - 核心智能功能
│   ├── agents/        # Agent实现
│   ├── prompts/       # 提示管理
│   ├── tools/         # 工具集成
│   └── workflows/     # 工作流程
├── web_api/           # API应用 - 对外接口
│   ├── api/
│   │   └── v1/
│   │       ├── agents.py    # Agent管理API
│   │       └── chat.py      # 对话API
│   ├── schemas/       # API数据模型
│   └── services/      # API业务逻辑
├── cli_app/           # CLI应用 - 管理工具
│   ├── commands/
│   │   ├── agent.py   # Agent管理命令
│   │   └── config.py  # 配置命令
│   └── output/        # 输出格式化
├── shared/            # 共享基础设施
│   ├── core/          # 核心业务逻辑
│   ├── models/        # 共享数据模型
│   └── config/        # 统一配置管理
└── __init__.py
```

**Application Benefits:**
- **Clear Boundaries**: Each application has distinct responsibilities and can be developed independently
- **Scalable Architecture**: Applications can be deployed and scaled separately
- **Team Collaboration**: Different teams can work on different applications simultaneously  
- **Shared Infrastructure**: Common functionality is centralized and reusable across applications

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
│   └── docker-compose.yml      # Local development environmen
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

**Note**: The source code structure within `src/{project_name}/` follows application-centric architecture:

**Single Application Projects:**
- **Web APIs**: `web_api/` with internal api/, schemas/, services/, dependencies/
- **CLI Tools**: `cli_app/` with internal commands/, parsers/, output/, validators/  
- **Libraries**: `library/` with internal core/, utils/, exceptions/
- **Data Pipelines**: `data_pipeline/` with internal extractors/, transformers/, loaders/, orchestration/
- **LLM Agents**: `llm_agents/` with internal agents/, prompts/, tools/, workflows/

**Multi-Application Projects:**
- Each detected application type gets its own top-level module
- Applications follow their specific internal best practices
- Shared infrastructure extracted to `shared/` module
- Clear interfaces enable independent development and deployment

The initializer will detect application types from document analysis and create appropriate multi-application structure with proper separation of concerns.

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