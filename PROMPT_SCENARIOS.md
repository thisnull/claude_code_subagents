# Project Workflow Knowledge Base

**Purpose**: Provide comprehensive workflow knowledge for AI-powered prompt optimization. This knowledge base enables intelligent scenario detection and dynamic workflow requirement generation based on semantic understanding rather than keyword matching.

**AI Usage Instructions**: 
- Analyze the user's prompt to understand true intent and context
- Intelligently identify relevant scenarios and their relationships
- Dynamically generate customized workflow requirements
- Combine and prioritize multiple scenarios when appropriate
- Avoid mechanical matching and redundant suggestions

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Developing new functionality, adding capabilities, creating features
**Core Principles**:
- Requirements-driven development with clear specifications
- Design-first approach with architectural consideration
- Implementation following established coding standards
- Comprehensive testing and documentation
**Best Practices**:
- Update requirements documentation and design documents before development
- Follow project coding standards and architecture patterns during implementation
- Write unit tests, integration tests, and end-to-end tests after development completion
- Update API documentation when interface changes are involved
- Consider scalability and maintainability implications
**Common Combinations**: Often combined with API Changes, Database Changes, Testing, Documentation

## Bug Fixing
**When to Apply**: Resolving issues, fixing defects, addressing problems, debugging
**Core Principles**:
- Root cause analysis before implementing fixes
- Comprehensive testing to prevent regression
- Documentation of debugging process and solutions
- Systematic approach to identify similar issues
**Best Practices**:
- Conduct thorough testing verification after modifications are complete
- Document debugging process, root cause, and solution rationale
- Check for similar potential issues across the codebase
- Update relevant test cases to prevent regression
- Consider performance and security implications of the fix
**Common Combinations**: Often combined with Testing, Code Review, Performance Optimization

## Code Review
**When to Apply**: Reviewing code changes, refactoring, code quality improvements
**Core Principles**:
- Collaborative improvement and knowledge sharing
- Consistency with coding standards and best practices
- Security and performance consideration
- Maintainability and readability focus
**Best Practices**:
- Follow established code review checklist and guidelines
- Ensure coding standards and architectural best practices compliance
- Verify adequate test coverage for changed code
- Document architectural decisions and design rationale
- Check for security vulnerabilities and performance impacts
- Provide constructive feedback and learning opportunities
**Common Combinations**: Often combined with Bug Fixing, Testing, Security Audit

## Testing
**When to Apply**: Quality assurance, test development, validation, verification
**Core Principles**:
- Comprehensive coverage across different testing levels
- Automated testing for regression prevention
- Performance and reliability validation
- Documentation and maintainability of test suites
**Best Practices**:
- Ensure test coverage meets project standards and quality gates
- Run complete regression test suite before releases
- Update test documentation and testing strategy
- Verify functionality performance across different environments
- Implement appropriate testing pyramid (unit, integration, e2e)
**Common Combinations**: Often combined with Feature Development, Bug Fixing, Performance Optimization

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: System design, architectural planning, scalability considerations
**Core Principles**:
- Scalability and maintainability as primary concerns
- Technology stack alignment and trade-off analysis
- Documentation-driven architecture decisions
- Integration and data flow planning
**Best Practices**:
- Create comprehensive architecture documentation and diagrams
- Consider scalability, maintainability, and operational requirements
- Evaluate technology stack alignment and architectural trade-offs
- Plan for system integration, data flow, and service boundaries
- Document decision rationale and alternative considerations
- Consider non-functional requirements (security, performance, reliability)
**Common Combinations**: Often combined with API Changes, Database Changes, Performance Optimization

## API Changes
**When to Apply**: API development, interface modifications, service integration
**Core Principles**:
- Backward compatibility and versioning strategy
- Clear documentation and communication
- Contract testing and integration validation
- Consumer impact assessment
**Best Practices**:
- Update API documentation and interface specifications
- Consider API versioning strategy and backward compatibility requirements
- Conduct comprehensive API integration testing and contract testing
- Notify API consumers about changes with appropriate lead time
- Plan deprecation timeline and migration path for breaking changes
- Implement proper error handling and status codes
**Common Combinations**: Often combined with Feature Development, Database Changes, Testing, Documentation

## Database Changes
**When to Apply**: Schema modifications, data migrations, database optimizations
**Core Principles**:
- Data integrity and backward compatibility
- Safe migration procedures with rollback plans
- Performance and scalability considerations
- Documentation and change tracking
**Best Practices**:
- Create backward-compatible database migration scripts
- Validate migration scripts thoroughly in test environment
- Update data model documentation and ER diagrams
- Backup critical data before production migrations
- Plan detailed rollback procedures for failed migrations
- Consider performance impact of schema changes
**Common Combinations**: Often combined with Feature Development, API Changes, Data Migration

## Legacy System Modernization
**When to Apply**: System upgrades, technology migration, modernization projects
**Core Principles**:
- Risk mitigation through phased approach
- Data integrity throughout transition
- Minimal business disruption
- Comprehensive documentation and knowledge transfer
**Best Practices**:
- Assess current system dependencies, constraints, and business rules
- Plan phased migration strategy with minimal downtime
- Ensure data integrity and business continuity throughout transition
- Maintain backward compatibility during transition period
- Document migration procedures, rollback plans, and lessons learned
**Common Combinations**: Often combined with Architecture Design, Data Migration, Testing

---

# 📊 DATA & ANALYTICS

## Data Analysis
**When to Apply**: Data exploration, statistical analysis, reporting, insights generation
**Core Principles**:
- Data quality and accuracy as foundation
- Appropriate statistical methods and tools
- Clear visualization and actionable insights
- Reproducible analysis methodology
**Best Practices**:
- Verify data source accuracy, completeness, and representativeness
- Select appropriate statistical methods and analytical tools
- Design clear, meaningful, and accessible visualizations
- Provide actionable insights and concrete recommendations
- Document analysis methodology, assumptions, and limitations
**Common Combinations**: Often combined with Machine Learning, Documentation, Performance Optimization

## Machine Learning
**When to Apply**: Predictive modeling, AI/ML implementation, algorithmic solutions
**Core Principles**:
- Data quality and ethical considerations
- Proper model validation and evaluation
- Monitoring and maintenance planning
- Bias detection and mitigation
**Best Practices**:
- Validate training data quality, representativeness, and ethical implications
- Implement proper model evaluation, validation, and cross-validation
- Document model architecture, hyperparameters, and performance metrics
- Plan for model monitoring, retraining, and performance degradation detection
- Consider ethical implications, bias mitigation, and fairness measures
**Common Combinations**: Often combined with Data Analysis, Performance Optimization, Security Audit

## Data Migration
**When to Apply**: Data transfer, system integration, ETL processes
**Core Principles**:
- Data integrity and accuracy validation
- Minimal downtime and business disruption
- Comprehensive mapping and transformation
- Robust error handling and recovery
**Best Practices**:
- Create comprehensive data mapping and transformation documentation
- Implement thorough data validation and integrity checks
- Plan for incremental migration with minimal business downtime
- Establish detailed rollback procedures for failed migrations
- Test migration process extensively in staging environment
**Common Combinations**: Often combined with Database Changes, Legacy System Modernization, Testing

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Security assessments, vulnerability analysis, security enhancements
**Core Principles**:
- Comprehensive threat assessment
- Defense in depth strategy
- Compliance with security standards
- Continuous monitoring and improvement
**Best Practices**:
- Conduct comprehensive security vulnerability assessment and penetration testing
- Review authentication, authorization, and access control mechanisms
- Validate data encryption, secure communication, and key management
- Document security findings, risk assessment, and remediation plans
- Ensure compliance with relevant security standards and regulations
**Common Combinations**: Often combined with Code Review, Compliance, API Changes

## Compliance
**When to Apply**: Regulatory compliance, policy adherence, legal requirements
**Core Principles**:
- Thorough understanding of applicable regulations
- Systematic gap analysis and remediation
- Ongoing monitoring and maintenance
- Cross-functional collaboration
**Best Practices**:
- Review relevant regulatory requirements, standards, and organizational policies
- Assess current system compliance gaps and risk exposure
- Document compliance measures, controls, and evidence
- Plan for ongoing compliance monitoring and audit preparation
- Coordinate with legal, compliance, and business stakeholders
**Common Combinations**: Often combined with Security Audit, Documentation, Architecture Design

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: User interface development, user experience improvements, design system work
**Core Principles**:
- User-centered design methodology
- Accessibility and inclusivity
- Consistency with design systems
- Iterative design and validation
**Best Practices**:
- Conduct user research, persona development, and requirements gathering
- Create wireframes, mockups, and interactive prototypes
- Follow design system guidelines and maintain visual consistency
- Plan for responsive design across different devices and platforms
- Conduct usability testing, user feedback sessions, and design validation
**Common Combinations**: Often combined with Accessibility, Performance Optimization, Testing

## Performance Optimization
**When to Apply**: Performance improvements, optimization tasks, scalability enhancements
**Core Principles**:
- Baseline measurement and target setting
- Systematic bottleneck identification
- Measurable improvement validation
- Continuous monitoring and maintenance
**Best Practices**:
- Establish performance baseline metrics and realistic target goals
- Identify performance bottlenecks through profiling and monitoring
- Implement optimization strategies with measurable improvements
- Conduct comprehensive load testing and stress testing
- Monitor performance metrics continuously in production environment
**Common Combinations**: Often combined with Architecture Design, Database Changes, Monitoring

## Accessibility
**When to Apply**: Accessibility improvements, inclusive design, compliance with accessibility standards
**Core Principles**:
- Universal design and inclusive access
- Standards compliance (WCAG, ADA)
- Assistive technology compatibility
- User testing with diverse abilities
**Best Practices**:
- Follow WCAG guidelines and accessibility standards (A, AA, AAA)
- Test with assistive technologies, screen readers, and keyboard navigation
- Ensure proper keyboard navigation, focus management, and tab order
- Provide alternative text, semantic markup, and proper heading structure
- Conduct accessibility audits and user testing with diverse user groups
**Common Combinations**: Often combined with UI/UX Design, Testing, Compliance

---

# 🛠️ DEVOPS & OPERATIONS

## CI/CD Pipeline
**When to Apply**: Automation setup, deployment pipeline development, workflow optimization
**Core Principles**:
- Automation and repeatability
- Quality gates and validation
- Environment consistency
- Monitoring and alerting
**Best Practices**:
- Design automated build, test, and deployment pipeline
- Implement comprehensive testing and quality gates at each stage
- Configure environment-specific deployment strategies and approval processes
- Establish monitoring, alerting, and notification for pipeline failures
- Document pipeline configuration, troubleshooting, and maintenance procedures
**Common Combinations**: Often combined with Testing, Monitoring, Deployment

## Deployment
**When to Apply**: Release management, production deployments, environment management
**Core Principles**:
- Risk mitigation and rollback readiness
- Environment validation and configuration management
- Stakeholder communication and coordination
- Post-deployment monitoring
**Best Practices**:
- Check comprehensive deployment checklist and release notes
- Verify all environment configurations and dependency requirements
- Prepare detailed rollback plans and disaster recovery procedures
- Monitor system status, performance, and error rates after deployment
- Coordinate with stakeholders for release communication and support
**Common Combinations**: Often combined with CI/CD Pipeline, Monitoring, Testing

## Monitoring
**When to Apply**: Observability setup, alerting configuration, system monitoring
**Core Principles**:
- Proactive monitoring and alerting
- Comprehensive observability (metrics, logs, traces)
- Actionable alerts and escalation
- Continuous improvement and optimization
**Best Practices**:
- Define key performance indicators, SLIs, SLOs, and success metrics
- Configure comprehensive logging, metrics, and alerting systems
- Create operational dashboards for system visibility and health monitoring
- Establish incident response procedures, escalation paths, and on-call rotations
- Plan for capacity planning, resource optimization, and cost management
**Common Combinations**: Often combined with Performance Optimization, Deployment, Architecture Design

## Documentation
**When to Apply**: Technical documentation, knowledge management, process documentation
**Core Principles**:
- Accuracy and clarity for target audience
- Maintainability and version control
- Comprehensive coverage with practical examples
- Feedback incorporation and continuous improvement
**Best Practices**:
- Follow established documentation standards, templates, and style guides
- Ensure technical accuracy, clarity, and appropriate detail level for target audience
- Include practical code examples, screenshots, and step-by-step procedures
- Plan for documentation maintenance, version control, and regular updates
- Gather feedback from users and stakeholders for continuous improvement
**Common Combinations**: Often combined with Feature Development, API Changes, Architecture Design

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Semantic Analysis**: Understand the true intent behind the user's prompt
2. **Intelligent Matching**: Identify 1-3 most relevant scenarios based on context
3. **Dynamic Generation**: Create customized workflow requirements, not template filling
4. **Smart Combination**: When multiple scenarios apply, intelligently merge requirements
5. **Contextual Filtering**: Exclude irrelevant suggestions based on prompt context

### For Interactive Workshop (`/prompt-workshop`)
1. **Scenario Discussion**: Present identified scenarios and ask for confirmation
2. **Requirement Customization**: Adapt workflow requirements to specific project needs
3. **Priority Guidance**: Help users prioritize workflow requirements based on their context
4. **Best Practice Recommendations**: Suggest additional considerations based on scenario combinations

### Example AI Decision Process
**User Input**: "Fix the authentication API performance issue"

**AI Analysis**:
- Primary Context: Bug fixing (fixing a problem)
- Secondary Contexts: API changes (authentication API), Performance optimization (performance issue)
- Scenario Priority: Bug Fixing > Performance Optimization > API Changes
- Generated Focus: Fix-first approach with performance and API considerations
- Excluded: Not feature development, not new architecture design