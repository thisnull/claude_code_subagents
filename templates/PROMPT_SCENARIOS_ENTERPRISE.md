# Enterprise Development Cues Knowledge Base

**Philosophy**: "Systematic, compliant, and maintainable development with comprehensive governance, risk management, and stakeholder alignment."

**AI Usage Instructions**: 
- Prioritize compliance, security, and risk mitigation in all recommendations
- Suggest comprehensive documentation and approval processes
- Emphasize cross-team collaboration and stakeholder alignment
- Focus on long-term maintainability and operational excellence
- Recommend established enterprise patterns and proven practices

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Developing enterprise features with full governance
**Core Principles**:
- **Requirements-driven**: All development must be traceable to business requirements
- **Stakeholder alignment**: Ensure all parties are informed and aligned
- **Compliance-first**: Consider regulatory and policy requirements from day one
- **Enterprise architecture**: Align with existing systems and standards
**Best Practices**:
- Create detailed requirements documents with business stakeholder approval
- Conduct architecture review board (ARB) sessions for significant changes
- Follow enterprise coding standards and security guidelines
- Implement comprehensive test coverage (unit, integration, system, UAT)
- Update all documentation including API docs, runbooks, and user guides
- Obtain security and compliance team approval before production deployment
**Common Combinations**: Always combined with Architecture Design, Security Audit, Documentation

## Bug Fixing
**When to Apply**: Resolving issues with full impact assessment and governance
**Core Principles**:
- **Root cause analysis**: Comprehensive investigation of underlying causes
- **Impact assessment**: Evaluate business, security, and operational implications
- **Change control**: Follow established change management processes
- **Risk mitigation**: Implement safeguards to prevent similar issues
**Best Practices**:
- Document detailed root cause analysis with timeline and contributing factors
- Assess impact on all stakeholders and dependent systems
- Follow change advisory board (CAB) process for production fixes
- Implement comprehensive regression testing to prevent similar issues
- Update monitoring and alerting to detect similar problems proactively
- Conduct post-incident review with lessons learned documentation
**Common Combinations**: Often combined with Security Audit, Code Review, Testing, Documentation

## Code Review
**When to Apply**: Comprehensive peer review with enterprise standards focus
**Core Principles**:
- **Multiple reviewers**: Senior developers and architects review significant changes
- **Standards compliance**: Ensure adherence to enterprise coding and security standards
- **Knowledge transfer**: Share expertise across team members
- **Quality assurance**: Comprehensive review of functionality, performance, and maintainability
**Best Practices**:
- Require approval from at least two senior developers for production changes
- Use automated tools to check coding standards, security vulnerabilities, and code quality
- Review for compliance with enterprise architecture patterns and principles
- Verify adequate test coverage and documentation updates
- Check for proper error handling, logging, and monitoring integration
- Ensure changes align with data governance and privacy requirements
**Common Combinations**: Always combined with Security Audit, Testing, Documentation

## Testing
**When to Apply**: Comprehensive testing strategy across all environments
**Core Principles**:
- **Comprehensive coverage**: Multiple levels of testing with defined quality gates
- **Automated regression**: Extensive automated test suites for continuous validation
- **Environment parity**: Testing in production-like environments
- **Performance validation**: Ensure scalability and performance requirements are met
**Best Practices**:
- Implement comprehensive test pyramid (unit, integration, system, acceptance)
- Maintain automated regression test suites with minimum coverage thresholds
- Conduct performance testing with realistic load scenarios
- Execute security testing including penetration testing for critical systems
- Perform user acceptance testing (UAT) with business stakeholders
- Validate disaster recovery and business continuity procedures
**Common Combinations**: Always combined with all other scenarios

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: Enterprise system design with comprehensive governance
**Core Principles**:
- **Enterprise alignment**: Ensure consistency with enterprise architecture standards
- **Scalability planning**: Design for current and projected enterprise scale
- **Integration strategy**: Plan for seamless integration with existing enterprise systems
- **Governance compliance**: Adhere to architectural governance processes
**Best Practices**:
- Conduct formal architecture review with enterprise architecture team
- Create comprehensive architecture documentation with multiple viewpoints
- Perform technology stack alignment assessment with enterprise standards
- Plan for system integration patterns, data flow, and service boundaries
- Document architectural decisions with rationale and alternatives considered
- Consider non-functional requirements (security, performance, reliability, compliance)
- Plan for operational requirements (monitoring, logging, maintenance, support)
**Common Combinations**: Always combined with Security Audit, Compliance, Performance Optimization

## API Changes
**When to Apply**: Enterprise API development with governance and lifecycle management
**Core Principles**:
- **Enterprise API strategy**: Align with enterprise API management and governance
- **Comprehensive documentation**: Detailed API specifications and consumer guidance
- **Lifecycle management**: Proper versioning, deprecation, and migration strategies
- **Consumer impact management**: Proactive communication and support for API consumers
**Best Practices**:
- Follow enterprise API design standards and governance processes
- Create comprehensive OpenAPI specifications with detailed documentation
- Implement proper API versioning strategy with backward compatibility planning
- Conduct thorough API security review including authentication and authorization
- Perform comprehensive integration testing with consumer systems
- Establish API monitoring, analytics, and SLA management
- Plan deprecation timeline with migration support for breaking changes
- Coordinate with API governance team for approval and lifecycle management
**Common Combinations**: Always combined with Architecture Design, Security Audit, Documentation

## Database Changes
**When to Apply**: Enterprise database management with comprehensive governance
**Core Principles**:
- **Data governance**: Ensure compliance with enterprise data management policies
- **Change control**: Follow rigorous database change management processes
- **Performance impact**: Comprehensive assessment of performance implications
- **Disaster recovery**: Maintain enterprise backup and recovery capabilities
**Best Practices**:
- Follow enterprise database change control and approval processes
- Create comprehensive database migration scripts with rollback procedures
- Conduct thorough testing in production-equivalent environments
- Update enterprise data model documentation and data dictionaries
- Implement proper backup procedures before production migrations
- Plan detailed rollback procedures with tested recovery processes
- Consider performance impact analysis for large-scale changes
- Coordinate with database administration team for deployment approval
**Common Combinations**: Always combined with Architecture Design, Security Audit, Data Migration

## Legacy System Modernization
**When to Apply**: Enterprise system transformation with minimal business disruption
**Core Principles**:
- **Business continuity**: Ensure minimal disruption to business operations
- **Risk management**: Comprehensive risk assessment and mitigation strategies
- **Phased approach**: Systematic migration with controlled rollback points
- **Stakeholder management**: Extensive communication and change management
**Best Practices**:
- Conduct comprehensive current state assessment with dependency mapping
- Develop detailed migration strategy with multiple phases and rollback points
- Ensure data integrity and business continuity throughout transformation
- Maintain backward compatibility and parallel operations during transition
- Document comprehensive migration procedures and lessons learned
- Coordinate with business stakeholders for change management and training
- Implement comprehensive monitoring and validation during migration phases
**Common Combinations**: Always combined with Architecture Design, Data Migration, Testing, Documentation

---

# 📊 DATA & ANALYTICS

## Data Analysis
**When to Apply**: Enterprise analytics with governance and compliance focus
**Core Principles**:
- **Data governance**: Ensure compliance with enterprise data policies and privacy regulations
- **Quality assurance**: Comprehensive data quality validation and lineage tracking
- **Stakeholder alignment**: Align analysis objectives with business strategy and KPIs
- **Methodological rigor**: Apply statistical best practices and peer review processes
**Best Practices**:
- Verify data source accuracy, completeness, and compliance with data governance policies
- Select appropriate statistical methods with peer review and validation
- Create clear, accessible visualizations following enterprise design standards
- Provide actionable insights with confidence intervals and statistical significance
- Document comprehensive methodology, assumptions, limitations, and data lineage
- Ensure compliance with privacy regulations and data usage policies
**Common Combinations**: Often combined with Compliance, Documentation, Machine Learning

## Machine Learning
**When to Apply**: Enterprise ML with comprehensive governance and ethical considerations
**Core Principles**:
- **Ethical AI**: Comprehensive bias detection, fairness assessment, and ethical review
- **Model governance**: Established MLOps practices with model lifecycle management
- **Regulatory compliance**: Ensure compliance with AI/ML regulatory requirements
- **Enterprise integration**: Seamless integration with existing enterprise systems
**Best Practices**:
- Validate training data quality with comprehensive bias and fairness assessment
- Implement rigorous model evaluation with cross-validation and business metrics
- Document comprehensive model architecture, hyperparameters, and performance metrics
- Establish model monitoring, retraining, and performance degradation detection
- Conduct ethical review including bias mitigation and explainability requirements
- Implement enterprise MLOps practices with version control and deployment automation
- Ensure compliance with AI/ML regulatory requirements and enterprise policies
**Common Combinations**: Always combined with Data Analysis, Security Audit, Compliance

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Comprehensive enterprise security assessment and validation
**Core Principles**:
- **Defense in depth**: Multi-layered security strategy with comprehensive threat modeling
- **Compliance alignment**: Ensure adherence to enterprise security standards and regulations
- **Continuous monitoring**: Ongoing security validation and threat detection
- **Risk management**: Systematic risk assessment with mitigation strategies
**Best Practices**:
- Conduct comprehensive security vulnerability assessment with penetration testing
- Review authentication, authorization, and access control against enterprise standards
- Validate data encryption, secure communication, and key management practices
- Document detailed security findings with risk assessment and remediation plans
- Ensure compliance with enterprise security standards and regulatory requirements
- Implement security monitoring and incident response procedures
- Coordinate with enterprise security team for approval and ongoing monitoring
**Common Combinations**: Always combined with all enterprise scenarios

## Compliance
**When to Apply**: Comprehensive regulatory and policy compliance validation
**Core Principles**:
- **Regulatory expertise**: Deep understanding of applicable regulations and standards
- **Systematic approach**: Comprehensive gap analysis with remediation planning
- **Ongoing monitoring**: Continuous compliance validation and audit preparation
- **Cross-functional collaboration**: Coordination with legal, risk, and business teams
**Best Practices**:
- Conduct comprehensive review of applicable regulatory requirements and enterprise policies
- Perform systematic compliance gap analysis with risk exposure assessment
- Document detailed compliance measures, controls, and audit evidence
- Implement ongoing compliance monitoring with automated validation where possible
- Coordinate with legal, compliance, and risk management teams for approval
- Prepare comprehensive audit documentation and evidence packages
- Establish compliance reporting and governance processes
**Common Combinations**: Always combined with Security Audit, Documentation, Architecture Design

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: Enterprise user experience with accessibility and brand compliance
**Core Principles**:
- **Enterprise design system**: Consistent user experience across all enterprise applications
- **Accessibility compliance**: Full compliance with accessibility standards (WCAG, Section 508)
- **User-centered design**: Comprehensive user research and validation with enterprise users
- **Brand alignment**: Consistent brand experience and corporate design standards
**Best Practices**:
- Conduct comprehensive user research with enterprise user personas and journey mapping
- Create detailed wireframes, prototypes, and design specifications
- Follow enterprise design system guidelines and brand standards
- Ensure comprehensive accessibility compliance with assistive technology testing
- Conduct extensive usability testing with representative enterprise users
- Coordinate with brand, marketing, and accessibility teams for approval
**Common Combinations**: Often combined with Accessibility, Testing, Documentation

---

# 🛠️ DEVOPS & OPERATIONS

## CI/CD Pipeline
**When to Apply**: Enterprise automation with comprehensive quality gates and governance
**Core Principles**:
- **Enterprise integration**: Integration with enterprise development and deployment infrastructure
- **Quality assurance**: Comprehensive automated testing and quality validation
- **Security integration**: Automated security scanning and compliance validation
- **Audit trail**: Complete deployment tracking and compliance reporting
**Best Practices**:
- Design automated pipeline following enterprise DevOps standards and tools
- Implement comprehensive quality gates including automated testing, security scanning, and compliance checks
- Configure environment-specific deployment strategies with approval development cues
- Establish comprehensive monitoring, logging, and alerting for pipeline operations
- Document detailed pipeline configuration with troubleshooting and maintenance procedures
- Coordinate with enterprise DevOps and security teams for infrastructure approval
**Common Combinations**: Always combined with Testing, Security Audit, Monitoring

## Deployment
**When to Apply**: Enterprise deployment with comprehensive risk management and coordination
**Core Principles**:
- **Change control**: Rigorous change management with stakeholder approval
- **Risk mitigation**: Comprehensive risk assessment with detailed rollback procedures
- **Business coordination**: Extensive stakeholder communication and coordination
- **Operational excellence**: Comprehensive monitoring and support procedures
**Best Practices**:
- Follow enterprise change control and deployment approval processes
- Verify comprehensive environment configurations and dependency validation
- Prepare detailed rollback plans with tested disaster recovery procedures
- Implement comprehensive monitoring for system performance, security, and business metrics
- Coordinate extensively with business stakeholders for release communication and training
- Establish 24/7 support procedures with escalation processes
**Common Combinations**: Always combined with CI/CD Pipeline, Monitoring, Documentation

## Monitoring
**When to Apply**: Enterprise observability with comprehensive operational intelligence
**Core Principles**:
- **Enterprise visibility**: Comprehensive system and business metrics aligned with enterprise KPIs
- **Proactive operations**: Advanced monitoring with predictive analytics and automated response
- **Compliance monitoring**: Continuous validation of security, performance, and compliance requirements
- **Business alignment**: Monitoring aligned with business objectives and SLA requirements
**Best Practices**:
- Define comprehensive KPIs, SLIs, SLOs aligned with business objectives and enterprise standards
- Implement enterprise monitoring infrastructure with centralized logging and metrics
- Create comprehensive operational dashboards with business and technical metrics
- Establish detailed incident response procedures with enterprise escalation processes
- Plan for capacity management, resource optimization, and cost control
- Coordinate with enterprise operations and business teams for SLA management
**Common Combinations**: Always combined with all enterprise scenarios

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Governance First**: Always include appropriate approval processes and stakeholder alignment
2. **Comprehensive Documentation**: Recommend thorough documentation for all enterprise changes
3. **Risk Assessment**: Consider security, compliance, and operational risks in all recommendations
4. **Enterprise Integration**: Ensure alignment with existing enterprise systems and standards
5. **Long-term Perspective**: Focus on maintainability, scalability, and operational excellence

### For Interactive Workshop (`/prompt-workshop`)
1. **Stakeholder Identification**: Help identify all relevant stakeholders and approval processes
2. **Risk Planning**: Guide through comprehensive risk assessment and mitigation planning
3. **Compliance Validation**: Ensure consideration of all relevant regulatory and policy requirements
4. **Enterprise Standards**: Align recommendations with enterprise architecture and standards

### Example AI Decision Process
**User Input**: "Implement new customer data processing system"

**Enterprise AI Analysis**:
- Primary Context: Architecture Design + Data Analysis + Security Audit + Compliance
- Enterprise Considerations: Data privacy regulations, enterprise architecture alignment, stakeholder approval
- Required Processes: Architecture review board, security assessment, compliance validation, change control
- Documentation Needs: Business requirements, technical specifications, security assessment, compliance documentation
- Stakeholder Coordination: Business users, legal team, compliance team, enterprise architecture, security team