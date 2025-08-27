# Maintenance Mode Development Workflow Knowledge Base

**Philosophy**: "Stability first, risk minimization, and careful evolution. Preserve existing functionality while making gradual improvements that enhance rather than disrupt the current system."

**AI Usage Instructions**: 
- Prioritize backward compatibility and stability over new features
- Suggest conservative approaches with proven track records
- Focus on risk mitigation and thorough testing before changes
- Recommend incremental improvements rather than major overhauls
- Emphasize monitoring and observability to catch issues early

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Adding functionality to established systems with focus on stability preservation
**Core Principles**:
- **Compatibility first**: All new features must maintain backward compatibility
- **Risk assessment**: Evaluate impact on existing functionality before implementation
- **Incremental addition**: Add features gradually to minimize disruption
- **User impact consideration**: Prioritize features that enhance rather than change existing workflows
**Best Practices**:
- Conduct thorough impact analysis before implementing any new features
- Use feature flags to enable gradual rollout and quick rollback if needed
- Implement new features as additive changes rather than modifications to existing code
- Ensure comprehensive testing of both new functionality and existing features
- Document all changes with clear rationale and potential impact assessment
- Plan migration paths for any changes that affect existing user workflows
**Common Combinations**: Always combined with Testing, Code Review, Risk Assessment

## Bug Fixing
**When to Apply**: Resolving issues in production systems with minimal risk approach
**Core Principles**:
- **Root cause analysis**: Understand the underlying cause, not just the symptoms
- **Minimal change principle**: Make the smallest change necessary to fix the issue
- **Regression prevention**: Ensure fixes don't break existing functionality
- **Monitoring and validation**: Verify fixes work in production without side effects
**Best Practices**:
- Analyze the full system impact before implementing any bug fix
- Create comprehensive test cases that reproduce the bug before fixing it
- Implement fixes using the most conservative approach possible
- Add monitoring and alerting to detect similar issues in the future
- Document the root cause analysis and solution rationale for future reference
- Plan rollback procedures for every bug fix deployment
- Validate fixes in production-like environments before deployment
**Common Combinations**: Always combined with Testing, Code Review, Monitoring

## Code Review
**When to Apply**: Rigorous review process with focus on stability and risk mitigation
**Core Principles**:
- **Stability verification**: Ensure changes don't introduce instability
- **Best practices adherence**: Follow established patterns and conventions
- **Performance impact assessment**: Verify changes don't degrade system performance
- **Security consideration**: Review all changes for potential security implications
**Best Practices**:
- Require multiple reviewers for any changes to critical system components
- Use automated tools to check for common issues and regressions
- Review changes against established coding standards and architectural patterns
- Verify that adequate test coverage exists for all modified code
- Check for proper error handling and logging in all changes
- Ensure changes include appropriate documentation updates
- Validate that changes follow the principle of least privilege and minimal change
**Common Combinations**: Always combined with Security Audit, Testing, Performance Analysis

## Testing
**When to Apply**: Comprehensive testing strategy to prevent regressions and ensure stability
**Core Principles**:
- **Regression prevention**: Extensive regression testing for all changes
- **Production-like testing**: Test in environments that closely mirror production
- **Comprehensive coverage**: Test both happy paths and edge cases thoroughly
- **Automated validation**: Use automated tests to catch regressions consistently
**Best Practices**:
- Maintain comprehensive regression test suites that cover critical functionality
- Implement automated testing pipelines that run on every change
- Perform thorough integration testing to ensure components work together correctly
- Conduct load testing to verify that changes don't impact system performance
- Use canary deployments and gradual rollouts to test changes with real traffic
- Maintain test environments that accurately reflect production configurations
- Document test procedures and keep test cases up-to-date with system changes
**Common Combinations**: Always combined with all maintenance scenarios

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: Architectural decisions for stable systems with focus on evolutionary rather than revolutionary change
**Core Principles**:
- **Evolutionary architecture**: Make gradual improvements rather than major rewrites
- **Proven patterns**: Use well-established architectural patterns with known characteristics
- **Minimal disruption**: Design changes that integrate smoothly with existing systems
- **Long-term maintainability**: Focus on sustainability and operational excellence
**Best Practices**:
- Conduct thorough architecture reviews before making any structural changes
- Use the Strangler Fig pattern to gradually replace legacy components
- Implement architectural changes incrementally with clear rollback plans
- Document architectural decisions and their rationale for future maintainers
- Consider operational requirements and monitoring needs in all architectural decisions
- Plan for graceful degradation and fault tolerance in architectural designs
- Ensure new architecture aligns with existing operational procedures and team skills
**Common Combinations**: Often combined with Legacy System Modernization, Performance Optimization

## API Changes
**When to Apply**: API evolution with strict backward compatibility and consumer protection
**Core Principles**:
- **Backward compatibility**: Never break existing API consumers
- **Versioning strategy**: Use clear, predictable versioning for any breaking changes
- **Consumer communication**: Proactively communicate changes to API users
- **Gradual deprecation**: Provide long deprecation timelines with migration support
**Best Practices**:
- Follow semantic versioning strictly and communicate version policies clearly
- Add new fields and endpoints rather than modifying existing ones
- Implement comprehensive API testing including contract testing with consumers
- Provide detailed migration guides and deprecation timelines for any breaking changes
- Monitor API usage patterns to understand impact of potential changes
- Maintain multiple API versions simultaneously during transition periods
- Use feature flags to control API behavior changes without version bumps
**Common Combinations**: Often combined with Testing, Documentation, Consumer Impact Assessment

## Database Changes
**When to Apply**: Database evolution with extreme care for data integrity and system stability
**Core Principles**:
- **Data safety**: Protect existing data at all costs
- **Backward compatibility**: Ensure existing applications continue to work
- **Rollback readiness**: Have tested rollback procedures for all changes
- **Performance preservation**: Maintain or improve database performance
**Best Practices**:
- Create comprehensive backup procedures before any database changes
- Test all migrations thoroughly in production-equivalent environments
- Use online schema migration tools that don't require downtime when possible
- Implement database changes incrementally with validation at each step
- Monitor database performance closely during and after migrations
- Document rollback procedures and test them in staging environments
- Plan for data migration validation and consistency checks
**Common Combinations**: Always combined with Data Migration, Testing, Performance Monitoring

## Legacy System Modernization
**When to Apply**: Gradual improvement of legacy systems without business disruption
**Core Principles**:
- **Minimal business impact**: Ensure continuous business operation during modernization
- **Risk mitigation**: Use proven patterns like Strangler Fig for gradual replacement
- **Functionality preservation**: Maintain all existing functionality throughout transition
- **Knowledge preservation**: Capture and document existing system knowledge
**Best Practices**:
- Conduct comprehensive current state analysis including dependency mapping
- Use the Strangler Fig pattern to gradually replace legacy components
- Maintain parallel operation of old and new systems during transition periods
- Implement comprehensive monitoring to ensure business continuity
- Document existing business rules and functionality before making changes
- Plan modernization in small, independent phases with clear success criteria
- Ensure team has necessary skills and training for new technologies
**Common Combinations**: Often combined with Architecture Design, Data Migration, Risk Assessment

---

# 📊 DATA & ANALYTICS

## Data Analysis
**When to Apply**: Analysis of system performance, usage patterns, and maintenance metrics
**Core Principles**:
- **System health focus**: Monitor metrics that indicate system stability and performance
- **Trend analysis**: Track long-term trends to predict maintenance needs
- **Actionable insights**: Focus on analysis that leads to concrete maintenance actions
- **Historical context**: Use historical data to understand system behavior patterns
**Best Practices**:
- Monitor key system health indicators including performance, error rates, and resource usage
- Analyze usage patterns to identify potential stability issues before they become critical
- Track maintenance metrics to understand system reliability and improvement trends
- Use data analysis to inform capacity planning and infrastructure decisions
- Create automated reports that highlight anomalies and concerning trends
- Maintain historical baselines to identify gradual degradation or improvement
**Common Combinations**: Often combined with Performance Optimization, Monitoring, Capacity Planning

## Performance Optimization
**When to Apply**: Performance improvements with focus on stability and measured improvement
**Core Principles**:
- **Measurement-driven**: Base all optimization efforts on actual performance measurements
- **Stability preservation**: Ensure optimizations don't introduce instability
- **Incremental improvement**: Make gradual optimizations with careful validation
- **User impact focus**: Prioritize optimizations that improve real user experience
**Best Practices**:
- Establish comprehensive performance baselines before making any optimizations
- Use profiling and monitoring tools to identify actual bottlenecks
- Implement performance improvements incrementally with thorough testing
- Monitor system behavior closely after performance changes
- Document optimization techniques and their measured impact
- Plan rollback procedures for performance changes that cause issues
- Focus on optimizations that provide measurable, sustained improvement
**Common Combinations**: Always combined with Monitoring, Testing, Data Analysis

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Regular security assessment with focus on maintaining security posture
**Core Principles**:
- **Continuous security**: Regular security reviews rather than one-time assessments
- **Risk-based approach**: Focus on the highest-impact security vulnerabilities
- **Compliance maintenance**: Ensure ongoing compliance with security standards
- **Minimal disruption**: Implement security improvements without breaking existing functionality
**Best Practices**:
- Conduct regular security vulnerability assessments and penetration testing
- Implement security patches promptly while testing for regression impacts
- Monitor security logs and alerts continuously for signs of compromise
- Update security configurations and access controls based on principle of least privilege
- Document security procedures and ensure they're followed consistently
- Plan security improvements that enhance rather than disrupt existing workflows
- Maintain security compliance through regular audits and assessments
**Common Combinations**: Always combined with Compliance, Monitoring, Risk Assessment

## Compliance
**When to Apply**: Maintaining regulatory compliance while evolving system capabilities
**Core Principles**:
- **Continuous compliance**: Maintain compliance throughout system evolution
- **Documentation maintenance**: Keep compliance documentation current and accurate
- **Change impact assessment**: Evaluate compliance impact of all system changes
- **Audit readiness**: Maintain systems in audit-ready state at all times
**Best Practices**:
- Review compliance requirements before implementing any system changes
- Maintain comprehensive audit trails and documentation for compliance purposes
- Implement compliance monitoring to detect any deviations from required standards
- Plan compliance validation as part of all change management processes
- Update compliance procedures and documentation as systems evolve
- Ensure all team members understand compliance requirements and procedures
- Coordinate with legal and compliance teams for major system changes
**Common Combinations**: Always combined with Security Audit, Documentation, Change Management

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: User interface improvements with focus on preserving familiar workflows
**Core Principles**:
- **User workflow preservation**: Maintain familiar user workflows and patterns
- **Gradual improvement**: Make incremental UI improvements rather than major redesigns
- **Accessibility maintenance**: Ensure UI changes maintain or improve accessibility
- **User feedback integration**: Base UI changes on actual user feedback and usage data
**Best Practices**:
- Conduct user research to understand how existing interfaces are actually used
- Implement UI changes gradually with user testing and feedback incorporation
- Maintain design consistency with existing system patterns and conventions
- Ensure all UI changes maintain or improve accessibility standards
- Provide user training and documentation for any interface changes
- Use A/B testing to validate UI improvements before full rollout
- Plan rollback procedures for UI changes that negatively impact user experience
**Common Combinations**: Often combined with Accessibility, User Testing, Change Management

## Accessibility
**When to Apply**: Maintaining and improving accessibility in existing systems
**Core Principles**:
- **Standards compliance**: Maintain compliance with accessibility standards (WCAG, ADA)
- **User-centered approach**: Focus on real accessibility needs of actual users
- **Incremental improvement**: Gradually improve accessibility without disrupting existing users
- **Testing with users**: Validate accessibility improvements with users who have disabilities
**Best Practices**:
- Conduct regular accessibility audits to identify areas for improvement
- Implement accessibility improvements incrementally with user testing
- Maintain accessibility testing as part of regular development and maintenance processes
- Ensure accessibility considerations are included in all UI/UX changes
- Provide accessibility training and guidelines for all team members
- Monitor accessibility metrics and user feedback to identify issues
- Document accessibility features and improvements for users and compliance purposes
**Common Combinations**: Always combined with UI/UX Design, Testing, Compliance

---

# 🛠️ DEVOPS & OPERATIONS

## CI/CD Pipeline
**When to Apply**: Mature pipeline management with focus on reliability and risk mitigation
**Core Principles**:
- **Pipeline reliability**: Maintain stable, predictable deployment pipelines
- **Quality gates**: Comprehensive validation at each stage of the pipeline
- **Rollback readiness**: Quick rollback capabilities for failed deployments
- **Monitoring integration**: Comprehensive monitoring and alerting for pipeline operations
**Best Practices**:
- Implement comprehensive automated testing at multiple levels in the pipeline
- Use quality gates that prevent problematic changes from reaching production
- Maintain staging environments that accurately mirror production for testing
- Implement canary deployments and blue-green deployments for risk mitigation
- Monitor pipeline performance and reliability metrics continuously
- Document pipeline procedures and maintain runbooks for common issues
- Plan for pipeline maintenance and updates without disrupting development workflows
**Common Combinations**: Always combined with Testing, Monitoring, Deployment

## Deployment
**When to Apply**: Production deployments with comprehensive risk management and rollback planning
**Core Principles**:
- **Risk minimization**: Use deployment strategies that minimize risk of service disruption
- **Rollback readiness**: Have tested rollback procedures for every deployment
- **Monitoring verification**: Comprehensive post-deployment monitoring and validation
- **Communication**: Clear communication with stakeholders about deployment status and impact
**Best Practices**:
- Use deployment strategies like canary releases or blue-green deployments for risk mitigation
- Implement comprehensive health checks and monitoring during deployments
- Maintain detailed deployment procedures and rollback plans
- Test deployment procedures regularly in staging environments
- Coordinate deployments with stakeholders and plan for appropriate maintenance windows
- Monitor system performance and user experience closely after deployments
- Document deployment outcomes and lessons learned for continuous improvement
**Common Combinations**: Always combined with Monitoring, CI/CD Pipeline, Communication

## Monitoring
**When to Apply**: Comprehensive system observability with focus on early problem detection
**Core Principles**:
- **Proactive monitoring**: Detect and alert on issues before they impact users
- **Comprehensive observability**: Monitor all critical system components and interactions
- **Actionable alerts**: Provide alerts that enable quick problem resolution
- **Historical analysis**: Use monitoring data to identify trends and prevent future issues
**Best Practices**:
- Implement comprehensive monitoring coverage including infrastructure, applications, and user experience
- Create monitoring dashboards that provide clear visibility into system health
- Set up alerting rules that balance sensitivity with actionability
- Use monitoring data to inform capacity planning and performance optimization
- Maintain monitoring system reliability and ensure monitoring infrastructure is itself monitored
- Document monitoring procedures and alert response processes
- Regularly review and update monitoring configurations based on system evolution
**Common Combinations**: Always combined with all maintenance scenarios

## Documentation
**When to Apply**: Comprehensive documentation maintenance for system continuity
**Core Principles**:
- **Living documentation**: Keep documentation current and accurate as systems evolve
- **Operational focus**: Emphasize documentation that supports daily operations and maintenance
- **Knowledge preservation**: Capture institutional knowledge and experience
- **User-centered**: Create documentation that serves the needs of different audiences
**Best Practices**:
- Maintain comprehensive runbooks for common operational procedures
- Document system architecture, dependencies, and configuration details
- Keep troubleshooting guides current and based on actual incident experience
- Create and maintain disaster recovery and business continuity documentation
- Document change procedures and approval processes clearly
- Ensure documentation is accessible and searchable for operations teams
- Review and update documentation regularly as part of maintenance procedures
**Common Combinations**: Always combined with all maintenance scenarios

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Stability First**: Always prioritize system stability and backward compatibility in recommendations
2. **Risk Assessment**: Include comprehensive risk analysis for any proposed changes
3. **Incremental Approach**: Suggest gradual, incremental improvements rather than major overhauls
4. **Proven Solutions**: Recommend established, well-tested approaches over experimental ones
5. **Rollback Planning**: Include rollback and contingency planning in all recommendations

### For Interactive Workshop (`/prompt-workshop`)
1. **Change Impact Analysis**: Help assess the full impact of proposed changes on existing systems
2. **Risk Mitigation Planning**: Guide through comprehensive risk assessment and mitigation strategies  
3. **Testing Strategy**: Develop thorough testing approaches for changes to stable systems
4. **Stakeholder Coordination**: Consider all stakeholders who might be affected by maintenance changes

### Example AI Decision Process
**User Input**: "Upgrade our authentication system to use OAuth 2.0"

**Maintenance AI Analysis**:
- Primary Context: Architecture Design + Security Audit (system evolution with stability focus)
- Maintenance Considerations: Backward compatibility for existing users, gradual migration strategy
- Risk Assessment: Impact on all existing user sessions, integration points, and downstream systems
- Implementation Approach: Phased rollout with parallel operation period, comprehensive testing
- Rollback Planning: Ability to revert to existing system if OAuth implementation causes issues