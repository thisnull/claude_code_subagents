# Personal Quality-First Minimalist Development Cues Knowledge Base

**Philosophy**: "Quality-first minimalist development: Simple solutions, rigorous testing, evidence-based validation. Build the simplest thing that works correctly, with quality assurance built into the process."

**AI Usage Instructions**: 
- Prioritize simple, direct solutions but never skip quality assurance steps
- Suggest minimal viable implementations with comprehensive testing
- Emphasize evidence-based validation over documentation assumptions
- Focus on documentation-driven development with test-first approach
- Recommend practical tools (SQLAlchemy, Alembic, Context7) to simplify quality development cues

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Building new features with documentation-driven, test-first approach
**Core Principles**:
- **Documentation first**: Update relevant documentation before coding, following project docs/README.md guidelines
- **Test-first development**: Write test cases and test plans in docs/40-quality before implementation
- **Simple implementation**: Choose the simplest approach that meets requirements
- **Evidence validation**: Verify everything works through real testing, not assumptions
**Best Practices**:
- **Step 0: Code Analysis** - Before any implementation, thoroughly read existing codebase to understand patterns and reusable components
- **Step 1: Documentation Update** - Review and update relevant documentation in docs/ following project README.md guidance
- **Step 2: Test Planning** - Create comprehensive test cases and test plan in docs/40-quality before coding
- **Step 3: Simple Implementation** - Write the minimum code needed with maximum reuse of existing code patterns
- **Step 4: Test Execution** - Execute test plan systematically, fix issues, re-test until all tests pass
- **Step 5: Evidence Verification** - For database changes: query real data; for APIs: make actual calls
- **Code Reuse Priority**: Always study existing code first to identify reusable functions, classes, and patterns
- Follow existing code conventions, naming patterns, and architectural decisions consistently
- Prefer extending or composing existing components over creating new ones from scratch
- When similar functionality exists, refactor existing code to be more generic rather than duplicating
- Add structured logging (not print statements) to enable effective debugging
- When using third-party APIs: actually call them to verify behavior, don't trust documentation alone
- Consult Context7 MCP documentation for best practices and established patterns
**Common Combinations**: Always combined with Testing, Documentation, Evidence Validation

## Bug Fixing
**When to Apply**: Resolving issues with systematic approach and quality validation
**Core Principles**:
- **Root cause analysis**: Understand the real problem through log analysis and data inspection
- **Documentation update**: Update relevant docs if bug reveals documentation gaps
- **Test-driven fixing**: Write test cases that reproduce the bug before fixing
- **Evidence validation**: Verify fixes work through real data inspection and testing
**Best Practices**:
- **Step 1: Problem Analysis** - Review logs carefully to understand root cause, don't guess
- **Step 2: Documentation Review** - Check if bug indicates documentation needs updates
- **Step 3: Test Case Creation** - Write failing test case in docs/40-quality that reproduces the bug
- **Step 4: Simple Fix** - Implement minimal fix with adequate logging
- **Step 5: Test Validation** - Run test plan, verify fix works, check real data if storage involved
- For database/cache issues: always inspect actual stored data, don't rely on application assumptions
- Add logging if not sufficient for debugging similar issues in future
- Use logs to analyze system behavior, not just application responses
**Common Combinations**: Often combined with Testing, Log Analysis, Data Validation

## Code Review
**When to Apply**: Quality validation focused on simplicity and correctness
**Core Principles**:
- **Simplicity check**: Is this the simplest way to solve the problem?
- **Quality validation**: Does code include proper logging, testing, and documentation?
- **Evidence verification**: Are assumptions validated through real testing?
- **Standards compliance**: Follows project patterns and best practices?
**Best Practices**:
- Verify that documentation was updated appropriately for changes
- Check that test cases exist in docs/40-quality and actually test the functionality
- **Code Reuse Validation**: Verify that existing code patterns and components were properly reused rather than duplicated
- Ensure adequate structured logging exists for debugging
- For database changes: verify Model-First approach and proper Alembic usage
- For API integrations: confirm actual API calls were made during development
- Review for proper error handling and edge case coverage
- Ensure changes are the simplest viable solution and follow existing code patterns
- Check that new code follows established naming conventions and architectural decisions
- Validate that similar existing functionality wasn't unnecessarily duplicated
**Common Combinations**: Often combined with Documentation Validation, Test Review

## Testing
**When to Apply**: Systematic testing with emphasis on real-world validation
**Core Principles**:
- **Test-first approach**: Tests are written before implementation, stored in docs/40-quality
- **Evidence-based validation**: Test with real data and actual system behavior
- **Log analysis**: Use logs to understand test results and identify issues
- **Iterative fixing**: Fix issues and re-test until all tests pass
**Best Practices**:
- Execute test plans from docs/40-quality systematically, don't skip steps
- Monitor logs during test execution to catch issues that might not surface in test results
- For database/cache functionality: query actual stored data to verify correct behavior
- For API functionality: make real API calls and verify actual responses
- When tests fail: analyze logs first before making assumptions about causes
- Add logging to tests themselves if needed for debugging test failures
- Continue testing cycles (test → fix → test) until all test cases pass
- Document any test plan updates needed based on testing experience
**Common Combinations**: Often combined with Log Analysis, Data Validation, API Validation

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: System design with focus on simplicity and maintainability
**Core Principles**:
- **Simple first**: Start with the simplest architecture that solves the problem
- **Documentation driven**: Architecture decisions documented before implementation
- **Tool utilization**: Use established tools (SQLAlchemy, Alembic) to reduce complexity
- **Evidence-based**: Validate architecture decisions through prototypes and real testing
**Best Practices**:
- Document architectural decisions in project docs before implementation
- Choose boring, proven technologies over new, complex solutions
- Use Context7 MCP documentation to understand best practices for chosen technologies
- For data layer: strictly follow Model-First approach with SQLAlchemy
- Plan for adequate logging and observability from the start
- Test architectural assumptions with simple prototypes before full implementation
- Design for debugging: ensure system behavior is observable through logs and data inspection
**Common Combinations**: Often combined with Documentation, Database Design, Tool Selection

## API Changes
**When to Apply**: API development and third-party integration with emphasis on real-world validation
**Core Principles**:
- **Simple patterns**: Use straightforward, proven API patterns for your own APIs
- **Evidence validation**: Actually call APIs during development, don't trust documentation alone
- **Third-party integration**: Reference Context7 MCP documentation when integrating external services
- **Test-driven approach**: Write API test cases before implementation
**Best Practices**:
- For your own APIs: focus on simple, consistent patterns that are easy to understand and maintain
- Write API test cases in docs/40-quality before implementation
- Implement with adequate logging for request/response debugging
- Actually call your own APIs during development to verify behavior
- **For third-party API integrations**: Consult Context7 MCP documentation for best practices and known patterns
- **For external services**: Make real calls to verify documentation accuracy, don't just trust vendor docs
- Test error conditions and edge cases with actual API calls, not mocked responses
- Document API behavior based on actual observed behavior, not intended behavior
**Common Combinations**: Often combined with Third-party Integration, Real API Testing, Documentation

## Database Changes
**When to Apply**: Database modifications using strict Model-First methodology with comprehensive validation
**Core Principles**:
- **Model-First approach**: All database structure changes start with SQLAlchemy model modifications
- **Alembic automation**: Use `uv run alembic revision --autogenerate` for all migrations
- **100% consistency**: Database structure must exactly match code models
- **Evidence validation**: Inspect actual database structure and data after changes
**Best Practices**:
- **Step 1: Model Modification** - Make changes to SQLAlchemy models first, never database directly
- **Step 2: Migration Status Check** - Run `uv run alembic current` to see current migration state
- **Step 3: Migration Generation** - Run `uv run alembic revision --autogenerate -m "descriptive message"` to create migration script
- **Step 4: Migration Review** - Review generated migration script for correctness and completeness:
  - Check upgrade() and downgrade() functions are properly generated
  - Verify all table/column changes are captured correctly
  - Ensure foreign key constraints and indexes are handled appropriately
- **Step 5: Migration Testing** - Test migration in development environment:
  - Run `uv run alembic upgrade head` to apply migration
  - Use `uv run alembic check` to verify no additional operations are detected
  - Test rollback with `uv run alembic downgrade -1` to ensure reversibility
- **Step 6: Data Validation** - After migration, inspect actual database structure and data:
  - Query database directly to verify schema changes applied correctly
  - Check data integrity and relationships are maintained
  - Validate that application code works with new database structure
- **Step 7: Production Readiness** - Before production deployment:
  - Test migration on copy of production data
  - Document any data migration or transformation requirements
  - Plan rollback procedures and test them thoroughly
- Never manually modify database structure - always go through model → migration process
- Use descriptive migration messages: `uv run alembic revision --autogenerate -m "add user email column"`
- For complex changes, consider breaking into multiple smaller migrations
- Add logging to track database operations during migration and testing
- Check real data in database to ensure migrations worked correctly, don't just trust return codes
- Use `uv run alembic history` to view migration timeline and dependencies
**Common Combinations**: Always combined with Model Validation, Migration Testing, Data Inspection

---

# 📊 DATA & ANALYTICS

## Data Analysis
**When to Apply**: Simple analysis with focus on actionable insights
**Core Principles**:
- **Real data validation**: Always work with actual data, verify data quality first
- **Simple tools**: Use straightforward analysis approaches before complex solutions
- **Evidence-based**: Validate analysis results through multiple approaches
- **Actionable focus**: Analysis should lead to concrete, implementable decisions
**Best Practices**:
- Inspect actual data quality and completeness before analysis
- Use simple statistical approaches before complex modeling
- Validate analysis results by checking against actual data records
- Add logging to analysis processes to track data processing steps
- Document analysis methodology and assumptions clearly
- Verify analysis results make business sense through manual spot-checks of data
**Common Combinations**: Often combined with Data Validation, Evidence Checking

## Performance Optimization
**When to Apply**: Performance improvements based on actual measurement and evidence
**Core Principles**:
- **Measure first**: Use logs and real performance data to identify bottlenecks
- **Evidence-based**: Optimize based on actual measured problems, not assumptions
- **Simple solutions**: Choose straightforward optimizations before complex ones
- **Real validation**: Verify improvements through actual performance measurements
**Best Practices**:
- Add performance logging before optimization to establish baseline
- Identify bottlenecks through log analysis and actual performance measurement
- For database performance: inspect actual query execution and data access patterns
- Implement simple optimizations first (indexing, caching, query optimization)
- Measure performance improvements with real data and actual usage patterns
- Use logs to verify optimizations work as expected under real conditions
**Common Combinations**: Often combined with Log Analysis, Database Inspection, Measurement Validation

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Security validation with focus on real-world testing
**Core Principles**:
- **Evidence-based security**: Test security measures with actual attempts, not theoretical analysis
- **Simple security**: Use proven security libraries and patterns
- **Log-based monitoring**: Implement logging to detect and analyze security events
- **Real validation**: Verify security controls work through actual testing
**Best Practices**:
- Use established security libraries instead of implementing custom security
- Add comprehensive security logging for monitoring and analysis
- Test security controls with actual attack simulations, not just code review
- For API security: make actual unauthorized calls to verify access controls
- For data security: attempt actual data access to verify protection mechanisms
- Review logs for security events and suspicious patterns regularly
- Keep security tools and dependencies updated, verify updates work correctly
**Common Combinations**: Often combined with Real Security Testing, Log Monitoring

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: User interface development with real user validation
**Core Principles**:
- **User validation**: Test interfaces with real users, not assumptions
- **Simple interfaces**: Create intuitive, straightforward user experiences
- **Evidence-based design**: Make design decisions based on actual user behavior
- **Iterative improvement**: Improve interfaces based on real usage data and feedback
**Best Practices**:
- Test interfaces with actual users early and often
- Use simple, familiar interface patterns that users already understand
- Add logging to track actual user behavior and interface usage
- Make interface improvements based on real usage data, not assumptions
- Keep interface designs simple and focused on core user needs
- Validate interface changes through actual user testing before deployment
**Common Combinations**: Often combined with User Testing, Usage Analytics, Real Validation

---

# 🛠️ DEVOPS & OPERATIONS

## Deployment
**When to Apply**: Simple, reliable deployment with comprehensive validation
**Core Principles**:
- **Simple deployment**: Use straightforward deployment methods with proven reliability
- **Evidence validation**: Verify deployments work through real testing and monitoring
- **Rollback readiness**: Always have tested rollback procedures available
- **Log-based validation**: Use logs to verify deployment success and system health
**Best Practices**:
- Use simple, proven deployment platforms and methods
- Add comprehensive logging to deployment processes for debugging
- Test deployments in staging environments that mirror production
- After deployment: inspect actual system behavior through logs and real testing
- Verify all functionality works correctly after deployment through actual usage testing
- Monitor logs closely after deployment to catch any issues early
- Have rollback procedures tested and ready before any deployment
**Common Combinations**: Often combined with Log Monitoring, Real Testing, System Validation

## Monitoring
**When to Apply**: System monitoring focused on actionable insights and evidence
**Core Principles**:
- **Log-centric monitoring**: Use comprehensive logging as foundation for monitoring
- **Evidence-based alerts**: Alert on actual problems, not theoretical issues
- **Simple monitoring**: Use straightforward monitoring approaches that are easy to maintain
- **Actionable information**: Monitor things that require and enable specific responses
**Best Practices**:
- Implement comprehensive structured logging throughout applications
- Monitor logs for patterns that indicate real problems or performance issues
- Set up alerts for conditions that require immediate action
- For database monitoring: track actual query performance and data access patterns
- For API monitoring: track actual request/response patterns and error rates
- Review logs regularly to understand system behavior and identify trends
- Use monitoring data to make evidence-based decisions about system improvements
**Common Combinations**: Always combined with Log Analysis, System Inspection, Evidence Validation

## Documentation
**When to Apply**: Essential documentation that supports development workflow and quality
**Core Principles**:
- **Development workflow support**: Documentation that actively supports the development process
- **Evidence-based documentation**: Document actual system behavior, not intended behavior
- **Quality integration**: Documentation is part of quality assurance, not separate from it
- **Practical focus**: Focus on documentation that developers actually need and use
**Best Practices**:
- Follow project docs/README.md guidelines for documentation structure and content
- Update documentation as part of feature development process, not as afterthought
- Include test cases and test plans in docs/40-quality as living documentation
- Document actual system behavior based on real testing and usage
- Include troubleshooting information based on actual issues encountered
- Keep documentation current by updating it as part of every development cycle
- Document debugging and deployment procedures based on real experience
**Common Combinations**: Always combined with all development scenarios

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Simple Solutions First**: Always suggest the simplest approach that meets requirements, but include quality steps
2. **Quality Integration**: Include documentation update, test planning, and evidence validation as standard steps
3. **Code Reuse Priority**: Emphasize studying existing codebase first and maximizing reuse of existing patterns and components
4. **Tool Utilization**: Recommend using SQLAlchemy, Alembic, Context7, and other established tools to simplify development cues
5. **Evidence Emphasis**: Stress real testing, actual API calls, and data inspection over assumptions
6. **Structured Process**: Follow the code analysis → documentation → test planning → implementation → validation cycle

### For Interactive Workshop (`/prompt-workshop`)
1. **Development Cues Clarification**: Help establish the documentation-first, test-first approach for specific tasks
2. **Evidence Planning**: Plan how to validate assumptions through real testing and data inspection
3. **Quality Checkpoints**: Identify specific points where quality validation should occur
4. **Tool Integration**: Suggest how to effectively use project tools (SQLAlchemy, Alembic, Context7) for the task

### Example AI Decision Process
**User Input**: "Add user authentication to the API"

**Personal Quality-First AI Analysis**:
- Primary Context: Feature Development + API Changes (documentation-driven, test-first approach)
- Code Analysis Step: First study existing authentication patterns and user management code in the project
- Documentation Step: Update API docs and authentication section following docs/README.md
- Test Planning: Create authentication test cases in docs/40-quality before coding
- Implementation: Reuse existing authentication patterns, extend current user models if available
- Evidence Validation: Actually test authentication calls, don't just check code logic
- Database Integration: Use SQLAlchemy Model-First, extend existing user tables if they exist
- Real Testing: Make actual authenticated and unauthenticated API calls to verify behavior