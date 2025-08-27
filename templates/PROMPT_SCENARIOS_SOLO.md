# Solo Development Workflow Knowledge Base

**Philosophy**: "Efficient personal development with balanced quality. Optimize for individual productivity while maintaining code that future-you can understand and maintain."

**AI Usage Instructions**: 
- Prioritize solutions that balance speed with long-term maintainability
- Suggest self-documenting approaches that don't require extensive external documentation
- Focus on sustainable personal workflows that prevent burnout
- Recommend tooling and practices suitable for one-person teams
- Emphasize knowledge retention and personal skill development

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Building features as an individual developer with focus on personal productivity
**Core Principles**:
- **Self-sufficiency**: Choose technologies and patterns you can fully understand and maintain
- **Future-proof for yourself**: Write code that you'll understand in 6 months
- **Reasonable scope**: Avoid feature creep that overwhelms a single developer
- **Personal velocity**: Maintain sustainable development pace without burnout
**Best Practices**:
- Break large features into manageable daily tasks that provide visible progress
- Document key design decisions inline with code rather than separate documents
- Use familiar technologies unless learning new ones provides clear value
- Implement core functionality first, add polish incrementally
- Set realistic timelines that account for being the only person on the project
- Create personal code reviews by taking breaks between writing and reviewing
**Common Combinations**: Often combined with Testing, Performance Optimization, Documentation

## Bug Fixing
**When to Apply**: Individual troubleshooting with focus on learning and prevention
**Core Principles**:
- **Learning opportunity**: Use bugs as chances to understand the system better
- **Root cause focus**: Don't just patch symptoms since you'll be maintaining this long-term
- **Knowledge capture**: Document insights for future reference
- **Prevention mindset**: Consider what could prevent similar issues
**Best Practices**:
- Keep a personal bug log with root causes and solutions for future reference
- Take time to understand the full context of the bug, not just the immediate fix
- Write regression tests for bugs you've fixed to prevent recurrence
- Consider if the bug reveals larger architectural or design issues
- Use debugging as an opportunity to improve code organization and clarity
**Common Combinations**: Often combined with Code Review, Testing, Documentation

## Code Review
**When to Apply**: Self-review practices and occasional external feedback
**Core Principles**:
- **Self-review discipline**: Develop strong personal review habits
- **Code clarity**: Focus on making code readable for future-you
- **Architectural consistency**: Maintain consistent patterns across your codebase
- **External perspective**: Occasionally seek outside reviews for important changes
**Best Practices**:
- Implement a personal code review checklist covering your common mistake patterns
- Take breaks between writing and reviewing code to gain fresh perspective
- Read your code aloud or explain it to yourself to identify unclear sections
- Use static analysis tools to catch issues you might miss in solo review
- Seek peer reviews for critical components or when learning new technologies
- Review your own code after 1-2 weeks to identify areas for improvement
**Common Combinations**: Often combined with Feature Development, Bug Fixing

## Testing
**When to Apply**: Practical testing approach that provides confidence without excessive overhead
**Core Principles**:
- **Confidence-building**: Focus on tests that give you confidence to make changes
- **Maintainable test suite**: Keep tests simple enough for one person to maintain
- **Critical path coverage**: Ensure your most important features are well-tested
- **Personal testing style**: Develop testing approaches that fit your working style
**Best Practices**:
- Focus on testing business logic and complex algorithms rather than simple getters/setters
- Write integration tests for critical user workflows you can't afford to break
- Use Test-Driven Development selectively for complex problems that benefit from design clarity
- Maintain a balance between test coverage and development velocity
- Automate tests for repetitive scenarios you test manually
- Keep test data and setup simple to minimize maintenance overhead
**Common Combinations**: Often combined with Feature Development, Performance Optimization

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: System design decisions for maintainable solo projects
**Core Principles**:
- **Personal comprehensibility**: Choose architectures you can fully understand and debug
- **Maintainable complexity**: Balance sophistication with your ability to maintain it
- **Incremental evolution**: Design for gradual improvement rather than upfront perfection
- **Technology familiarity**: Prefer technologies you know well unless clear benefits justify learning new ones
**Best Practices**:
- Start with simple architectures and evolve complexity only when needed
- Document architectural decisions and rationale for future reference
- Choose frameworks and libraries with good documentation and active communities
- Plan for one-person operational requirements (deployment, monitoring, debugging)
- Consider your personal strengths and preferences in technology selection
- Design modular systems that allow you to work on one part at a time
**Common Combinations**: Often combined with Performance Optimization, Documentation

## API Changes
**When to Apply**: API development focused on clarity and personal maintainability
**Core Principles**:
- **Self-documenting design**: Create APIs that are intuitive and self-explanatory
- **Backward compatibility**: Maintain compatibility to avoid breaking your own applications
- **Simple versioning**: Use straightforward versioning strategies you can manage alone
- **Clear contracts**: Define clear API contracts that are easy to remember and use
**Best Practices**:
- Design APIs that follow consistent patterns you can remember without constant reference
- Use descriptive naming conventions that make the API's purpose obvious
- Implement comprehensive error handling with clear error messages
- Create simple API documentation with practical examples
- Test API changes thoroughly since you're the primary user and maintainer
- Version APIs conservatively to minimize compatibility issues
**Common Combinations**: Often combined with Feature Development, Documentation

## Database Changes
**When to Apply**: Database evolution with focus on simplicity and data safety
**Core Principles**:
- **Data safety first**: Never risk losing data due to complex migration procedures
- **Simple migrations**: Use straightforward migration strategies you can troubleshoot alone
- **Rollback readiness**: Always have clear rollback procedures for database changes
- **Personal data management**: Organize data in ways that make sense for your application
**Best Practices**:
- Always backup data before making schema changes
- Use database migration tools rather than manual SQL scripts
- Test migrations on copy of production data before applying to live systems
- Keep database schema simple and well-normalized unless performance requires denormalization
- Document database design decisions and constraints for future reference
- Plan for data growth and performance needs based on realistic usage projections
**Common Combinations**: Often combined with Feature Development, Data Migration

---

# 📊 DATA & ANALYTICS

## Data Analysis
**When to Apply**: Personal analytics and insights for solo projects
**Core Principles**:
- **Actionable insights**: Focus on analysis that leads to concrete decisions or improvements
- **Simple tools**: Use analytics tools that don't require extensive setup or maintenance
- **Personal metrics**: Track metrics that matter for your specific project goals
- **Learning-focused**: Use data analysis as a way to understand your users and system
**Best Practices**:
- Set up basic analytics to understand how your application is being used
- Focus on a few key metrics rather than trying to track everything
- Use simple visualization tools that you can set up and maintain yourself
- Analyze data regularly but don't let analysis paralysis prevent development progress
- Keep analysis tools and processes simple enough to maintain as a solo developer
**Common Combinations**: Often combined with Performance Optimization, Feature Development

## Performance Optimization
**When to Apply**: Performance improvements focused on user experience and maintainability
**Core Principles**:
- **User experience focus**: Optimize what users actually notice and care about
- **Measurement-driven**: Only optimize based on actual performance measurements
- **Sustainable optimization**: Choose optimization strategies you can maintain long-term
- **Cost-benefit analysis**: Balance optimization effort with actual improvement gained
**Best Practices**:
- Profile your application to identify actual bottlenecks rather than guessing
- Focus on optimizing the critical path that users experience most frequently
- Use simple performance monitoring tools that don't require complex setup
- Optimize database queries before optimizing application code
- Cache frequently-accessed data using simple caching strategies
- Monitor performance metrics over time to catch regressions early
**Common Combinations**: Often combined with Monitoring, Architecture Design

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Essential security practices for solo-maintained applications
**Core Principles**:
- **Essential security**: Focus on security practices that provide the most protection
- **Practical implementation**: Use security tools and practices you can implement and maintain alone
- **Standard practices**: Follow well-established security patterns rather than inventing new ones
- **Risk-based approach**: Prioritize security measures based on your specific risks
**Best Practices**:
- Use established authentication and authorization libraries rather than rolling your own
- Implement basic security hygiene: HTTPS, input validation, secure session management
- Keep dependencies updated and use tools to identify vulnerable packages
- Follow OWASP guidelines for your application type and technology stack
- Use security scanning tools that integrate with your development workflow
- Store sensitive configuration securely and never commit secrets to version control
**Common Combinations**: Often combined with Code Review, Compliance

## Compliance
**When to Apply**: Meeting necessary compliance requirements without excessive overhead
**Core Principles**:
- **Necessary compliance**: Focus on compliance requirements that actually apply to your project
- **Simple implementation**: Choose compliance strategies that don't overwhelm a solo developer
- **Documentation efficiency**: Create compliance documentation that serves multiple purposes
- **Gradual implementation**: Implement compliance measures incrementally as project grows
**Best Practices**:
- Understand which compliance requirements actually apply to your specific situation
- Use compliance-focused services and tools to reduce custom implementation needs
- Document compliance measures clearly for future audits or reviews
- Implement privacy and data protection measures appropriate to your user base
- Plan compliance considerations early rather than retrofitting them later
**Common Combinations**: Often combined with Security Audit, Documentation

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: User experience design for solo-developed applications
**Core Principles**:
- **User-centered design**: Focus on solving real user problems effectively
- **Simple, clean design**: Create interfaces that are intuitive and easy to maintain
- **Personal design skills**: Work within your design capabilities while gradually improving
- **Iterative improvement**: Continuously improve the user experience based on feedback
**Best Practices**:
- Start with simple, functional designs and improve incrementally
- Use established design patterns and UI component libraries to save time
- Test your interfaces with real users early and often
- Focus on usability and accessibility rather than complex visual design
- Keep design consistent throughout your application
- Learn basic design principles but don't try to compete with professional designers
**Common Combinations**: Often combined with Testing, Accessibility, Feature Development

## Accessibility
**When to Apply**: Making solo-developed applications accessible to all users
**Core Principles**:
- **Universal access**: Design for users with diverse abilities from the start
- **Standard practices**: Follow established accessibility guidelines and practices
- **Incremental improvement**: Gradually improve accessibility rather than trying to be perfect immediately
- **Testing with real users**: Get feedback from users with different accessibility needs
**Best Practices**:
- Learn and apply basic accessibility principles: semantic HTML, keyboard navigation, alt text
- Use accessibility testing tools that integrate with your development workflow
- Test your application with keyboard-only navigation and screen readers
- Choose color schemes and fonts that work for users with visual impairments
- Implement accessible forms with proper labels and error handling
- Learn from accessibility experts and communities but don't let perfectionism paralyze progress
**Common Combinations**: Often combined with UI/UX Design, Testing

---

# 🛠️ DEVOPS & OPERATIONS

## CI/CD Pipeline
**When to Apply**: Automation for solo development that saves time without excessive complexity
**Core Principles**:
- **Time-saving automation**: Automate repetitive tasks that consume significant time
- **Simple pipelines**: Keep CI/CD processes simple enough to troubleshoot and maintain alone
- **Reliable automation**: Prefer reliable, simple automation over complex, fragile systems
- **Incremental automation**: Add automation gradually as you identify time-consuming manual tasks
**Best Practices**:
- Start with simple automated testing and deployment scripts
- Use hosted CI/CD services to minimize infrastructure maintenance overhead
- Automate only the processes that you regularly perform and that benefit from automation
- Keep build and deployment processes simple and well-documented
- Monitor pipeline performance and reliability to ensure automation actually saves time
- Have manual fallback procedures for when automation fails
**Common Combinations**: Often combined with Testing, Deployment

## Deployment
**When to Apply**: Solo deployment strategies that balance simplicity with reliability
**Core Principles**:
- **Simple deployment**: Use deployment strategies you can execute and troubleshoot alone
- **Rollback readiness**: Always have quick rollback procedures for failed deployments
- **Minimal downtime**: Minimize service disruption while keeping deployment processes simple
- **Documentation**: Document deployment procedures clearly for consistency and troubleshooting
**Best Practices**:
- Use platform-as-a-service solutions to minimize infrastructure management overhead
- Implement health checks and monitoring to detect deployment issues quickly
- Deploy during low-traffic periods when possible to minimize user impact
- Test deployment procedures in staging environments that mirror production
- Keep deployment scripts and procedures well-documented and version-controlled
- Have monitoring and alerting set up to detect issues after deployment
**Common Combinations**: Often combined with Monitoring, CI/CD Pipeline

## Monitoring
**When to Apply**: Observability for solo-maintained applications with focus on actionable alerts
**Core Principles**:
- **Actionable monitoring**: Only monitor and alert on issues you can and will act upon
- **Simple setup**: Use monitoring tools that don't require complex setup or maintenance
- **Essential metrics**: Focus on monitoring the metrics that indicate real problems
- **Personal availability**: Set up monitoring and alerting that respects your personal time
**Best Practices**:
- Monitor application uptime, error rates, and performance metrics that affect users
- Set up alerts for critical issues that require immediate attention
- Use simple logging practices that help you debug issues when they occur
- Monitor resource usage to prevent outages and plan for capacity needs
- Keep monitoring dashboards simple and focused on actionable information
- Review monitoring data regularly to identify trends and potential issues
**Common Combinations**: Often combined with Performance Optimization, Deployment

## Documentation
**When to Apply**: Essential documentation that helps you maintain your own projects
**Core Principles**:
- **Future-you focused**: Write documentation that will help you understand and maintain your project in the future
- **Minimal but sufficient**: Document what's necessary without creating maintenance overhead
- **Living documentation**: Keep documentation current and useful or delete outdated information
- **Practical focus**: Emphasize how-to information over theoretical descriptions
**Best Practices**:
- Maintain clear README files with setup, usage, and troubleshooting information
- Document non-obvious design decisions and architectural choices inline with code
- Keep API documentation current if you're building APIs
- Document deployment and maintenance procedures step-by-step
- Use simple documentation tools that integrate with your development workflow
- Review and update documentation regularly to ensure it remains accurate and helpful
**Common Combinations**: Often combined with Feature Development, Architecture Design

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Personal Efficiency**: Prioritize solutions that maximize individual productivity without overwhelming complexity
2. **Self-Maintainability**: Recommend approaches that a single person can understand, implement, and maintain
3. **Sustainable Practices**: Focus on development practices that prevent burnout and maintain long-term motivation
4. **Skill Development**: Suggest opportunities for personal learning and skill improvement within project constraints
5. **Practical Balance**: Balance ideal practices with realistic constraints of solo development

### For Interactive Workshop (`/prompt-workshop`)
1. **Scope Management**: Help identify realistic project scope for individual development capacity
2. **Technology Assessment**: Evaluate technology choices based on solo developer's ability to learn and maintain them
3. **Time Management**: Consider personal time constraints and sustainable development pace
4. **Knowledge Gaps**: Identify areas where external help or learning may be needed

### Example AI Decision Process
**User Input**: "Build a social media dashboard for personal use"

**Solo AI Analysis**:
- Primary Context: Feature Development + UI/UX Design (personal productivity focus)
- Solo Considerations: Choose familiar technologies, start with MVP, plan for gradual feature addition
- Time Management: Break into daily tasks, avoid feature creep, focus on core value
- Technology Choice: Use established frameworks and libraries, avoid cutting-edge tech unless learning is a goal
- Maintenance Planning: Design for long-term personal maintainability, document key decisions