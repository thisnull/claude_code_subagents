# Open Source Development Workflow Knowledge Base

**Philosophy**: "Build in public, collaborate transparently, create value for the global community. Prioritize contributor experience, maintainability, and inclusive participation."

**AI Usage Instructions**: 
- Emphasize transparency, documentation, and community-friendly practices
- Suggest approaches that welcome and enable diverse contributors
- Focus on maintainability and long-term sustainability of the project
- Recommend inclusive practices that lower barriers to contribution
- Consider the needs of both maintainers and contributors in all recommendations

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Building features through community collaboration and transparent process
**Core Principles**:
- **Community-driven**: Features should address real community needs and use cases
- **Transparent process**: Development should be visible and inclusive
- **Contributor-friendly**: Enable community members to contribute meaningfully
- **Sustainable maintenance**: Consider long-term maintenance burden on maintainers
**Best Practices**:
- Create detailed feature proposals with community discussion (RFCs, issue discussions)
- Break down features into contribution-friendly tasks for different skill levels
- Provide comprehensive documentation for contributors including architecture decisions
- Implement thorough code review process that serves as mentorship
- Write extensive tests and documentation to support community contributions
- Consider backwards compatibility and migration paths for existing users
- Celebrate and acknowledge all contributor contributions publicly
**Common Combinations**: Always combined with Documentation, Code Review, Testing

## Bug Fixing
**When to Apply**: Resolving issues through collaborative problem-solving and learning
**Core Principles**:
- **Learning opportunity**: Treat bugs as opportunities to improve project and help contributors learn
- **Inclusive triage**: Welcome bug reports from users of all technical levels
- **Knowledge sharing**: Document debugging process to help community understand codebase
- **Contributor onboarding**: Use bug fixes as entry points for new contributors
**Best Practices**:
- Create detailed bug report templates that gather necessary information respectfully
- Triage bugs collaboratively with clear labels and priority discussions
- Document root cause analysis and solution rationale for community learning
- Create "good first issue" labels for bugs suitable for new contributors
- Provide mentorship and guidance for contributors working on bug fixes
- Update documentation and tests to prevent similar issues
- Thank and acknowledge bug reporters and fixers publicly
**Common Combinations**: Often combined with Code Review, Testing, Documentation

## Code Review
**When to Apply**: Collaborative review process that maintains quality and builds community
**Core Principles**:
- **Mentorship focus**: Use reviews as teaching and learning opportunities
- **Inclusive feedback**: Provide constructive, encouraging feedback to all contributors
- **Knowledge transfer**: Share expertise while building contributor skills
- **Quality maintenance**: Maintain code quality while encouraging participation
**Best Practices**:
- Provide detailed, educational feedback that explains reasoning behind suggestions
- Acknowledge good practices and learning in addition to suggesting improvements
- Create review checklists that help contributors self-review their work
- Be responsive to contributor questions and provide clarifications quickly
- Balance perfectionism with encouraging contributor participation
- Document review standards and decision-making process for transparency
- Recognize and thank reviewers and contributors publicly
**Common Combinations**: Always combined with all other scenarios

## Testing
**When to Apply**: Collaborative testing that ensures quality and builds contributor confidence
**Core Principles**:
- **Comprehensive coverage**: Tests that give contributors confidence to make changes
- **Documentation through tests**: Tests that serve as documentation for project behavior
- **Contributor enablement**: Testing infrastructure that helps contributors validate their work
- **Quality assurance**: Maintain high quality standards while welcoming diverse contributors
**Best Practices**:
- Maintain comprehensive test suite with clear testing guidelines for contributors
- Write tests that document expected behavior and serve as examples
- Provide easy-to-use testing infrastructure that contributors can run locally
- Include tests for different environments, platforms, and use cases
- Create testing documentation that helps contributors understand testing philosophy
- Use continuous integration that provides clear feedback to contributors
- Balance thorough testing with reasonable barriers to contribution
**Common Combinations**: Always combined with Feature Development, Bug Fixing, CI/CD Pipeline

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: Transparent, community-driven architecture decisions that enable long-term sustainability
**Core Principles**:
- **Transparency**: All architectural decisions should be documented and discussable
- **Community input**: Major decisions should involve community discussion and input
- **Extensibility**: Architecture should enable community contributions and extensions
- **Long-term sustainability**: Consider maintenance burden and contributor onboarding
**Best Practices**:
- Document architectural decisions with rationale and alternatives considered (ADRs)
- Conduct open discussions for major architectural changes with community input
- Create architecture documentation that helps contributors understand system design
- Design modular systems that enable community contributions in focused areas
- Consider backwards compatibility and migration paths for existing users and contributors
- Plan for distributed maintenance by multiple contributors over time
- Make architecture decisions that lower barriers to contribution rather than raise them
**Common Combinations**: Always combined with Documentation, Community Management

## API Changes
**When to Apply**: Community-friendly API evolution with user and contributor consideration
**Core Principles**:
- **Backwards compatibility**: Minimize breaking changes that affect users and downstream projects
- **Community consultation**: Involve community in API design discussions
- **Clear communication**: Transparent communication about API changes and timelines
- **Contributor enablement**: APIs that enable community extensions and integrations
**Best Practices**:
- Follow semantic versioning with clear communication about breaking changes
- Provide extensive API documentation with examples and use cases
- Conduct community review and discussion for significant API changes
- Implement comprehensive API testing to prevent regressions
- Create migration guides and deprecation timelines for breaking changes
- Design APIs that enable community plugins, extensions, and integrations
- Maintain stable APIs that downstream projects can depend on
**Common Combinations**: Often combined with Documentation, Testing, Community Management

## Database Changes
**When to Apply**: Data management changes that support project sustainability and community needs
**Core Principles**:
- **Migration safety**: Ensure database changes don't break existing installations
- **Documentation clarity**: Clear instructions for users managing their own deployments
- **Contributor accessibility**: Database changes that don't require specialized DBA knowledge
- **Community support**: Consider impact on community-hosted instances and deployments
**Best Practices**:
- Create comprehensive, tested migration scripts with clear rollback procedures
- Document database changes with clear upgrade instructions for self-hosted users
- Test migrations against different database versions and configurations
- Provide database schema documentation that helps contributors understand data model
- Consider resource requirements and performance impact of schema changes
- Support multiple database backends when possible for community flexibility
**Common Combinations**: Often combined with Documentation, Testing, Deployment

---

# 📊 DATA & ANALYTICS

## Data Analysis
**When to Apply**: Transparent analysis that informs project decisions and community priorities
**Core Principles**:
- **Transparency**: Share analysis methods and findings with community when appropriate
- **Privacy-focused**: Respect user privacy and avoid collecting unnecessary data
- **Community benefit**: Use analysis to improve project for all community members
- **Open methodology**: Document analysis approaches so community can understand and contribute
**Best Practices**:
- Focus on aggregate, anonymized metrics that inform project development
- Share relevant insights with community to guide collaborative decision-making
- Use analysis to understand contributor experience and barriers to participation
- Document methodology and assumptions so community can review and suggest improvements
- Analyze usage patterns to prioritize features and improvements that benefit most users
- Consider community diversity in analysis and avoid bias toward power users
**Common Combinations**: Often combined with Documentation, Community Management

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Community-driven security practices that build trust and protect all users
**Core Principles**:
- **Transparency**: Open security practices that community can review and improve
- **Community involvement**: Enable security-minded community members to contribute
- **Responsible disclosure**: Clear processes for reporting and addressing security issues
- **User protection**: Security measures that protect all users without creating barriers
**Best Practices**:
- Implement security best practices with documented rationale and implementation
- Create clear security policy and responsible disclosure process
- Welcome security-focused contributions and reviews from community
- Provide security documentation that helps contributors write secure code
- Use automated security scanning and make results available to community
- Address security issues promptly with transparent communication to affected users
- Consider security impact of all changes and document security decisions
**Common Combinations**: Often combined with Code Review, Documentation, Compliance

## Compliance
**When to Apply**: Meeting legal and regulatory requirements while maintaining open source values
**Core Principles**:
- **User empowerment**: Help users understand and meet their own compliance requirements
- **Transparency**: Clear information about compliance features and limitations
- **Community support**: Enable community to contribute compliance-related improvements
- **Global accessibility**: Consider compliance requirements in different jurisdictions
**Best Practices**:
- Document compliance features and limitations clearly for users
- Provide tools and documentation that help users meet their compliance requirements
- Consider privacy and data protection regulations in feature design
- Welcome contributions that improve compliance capabilities
- Maintain transparent policies about data collection, usage, and retention
- Support international users with different compliance requirements
**Common Combinations**: Often combined with Security Audit, Documentation

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: Inclusive, accessible design that serves diverse community needs
**Core Principles**:
- **Accessibility first**: Design that works for users with diverse abilities and technologies
- **International support**: Design that works across different languages and cultures
- **Community input**: Design decisions informed by actual user needs and feedback
- **Contributor-friendly**: Design systems that enable community design contributions
**Best Practices**:
- Follow accessibility guidelines (WCAG) and test with assistive technologies
- Design for internationalization with support for different languages and writing systems
- Create design systems and style guides that enable consistent community contributions
- Conduct user research with diverse community members to understand needs
- Provide design documentation and assets that enable community design contributions
- Use inclusive design practices that don't exclude any community members
- Balance aesthetic appeal with functional accessibility and performance
**Common Combinations**: Often combined with Accessibility, Testing, Documentation

## Accessibility
**When to Apply**: Ensuring inclusive access for all community members and users
**Core Principles**:
- **Universal access**: Technology should be usable by everyone regardless of abilities
- **Community leadership**: Learn from and center accessibility experts in community
- **Continuous improvement**: Accessibility is an ongoing process, not a one-time checklist
- **Education focus**: Help community learn about and implement accessibility best practices
**Best Practices**:
- Follow established accessibility guidelines (WCAG 2.1 AA minimum)
- Test with real assistive technologies and involve users with disabilities in testing
- Provide accessibility documentation and guidelines for contributors
- Make accessibility review part of standard code review process
- Audit accessibility regularly and address issues promptly
- Educate community about accessibility through documentation and examples
- Consider accessibility impact of all design and development decisions
**Common Combinations**: Always combined with UI/UX Design, Testing, Documentation

---

# 🛠️ DEVOPS & OPERATIONS

## CI/CD Pipeline
**When to Apply**: Transparent, contributor-friendly automation that maintains quality and enables participation
**Core Principles**:
- **Transparency**: All build and deployment processes should be visible and understandable
- **Contributor enablement**: CI/CD that helps contributors validate their work effectively
- **Quality assurance**: Automated checks that maintain project quality without creating barriers
- **Resource efficiency**: Use of free/sponsored CI services appropriate for open source projects
**Best Practices**:
- Use public CI services that provide transparent build logs and status
- Create comprehensive automated testing that gives contributors confidence in their changes
- Implement security scanning and quality checks that provide educational feedback
- Document CI/CD processes and make configuration files part of the repository
- Provide clear feedback to contributors about build failures and how to fix them
- Use contributor-friendly tools that don't require special access or setup
- Balance thoroughness with speed to provide timely feedback to contributors
**Common Combinations**: Always combined with Testing, Security Audit, Documentation

## Deployment
**When to Apply**: Community-friendly deployment that enables diverse hosting and contribution scenarios
**Core Principles**:
- **Self-hosting support**: Enable community members to deploy and run the project themselves
- **Documentation clarity**: Clear instructions that work for different technical skill levels
- **Multiple options**: Support different deployment scenarios and environments
- **Contributor testing**: Enable contributors to test their changes in realistic environments
**Best Practices**:
- Provide comprehensive deployment documentation for different environments and skill levels
- Support multiple deployment options (Docker, package managers, manual installation)
- Create deployment scripts and configuration that community can use and modify
- Test deployment processes regularly to ensure instructions remain accurate
- Provide troubleshooting documentation for common deployment issues
- Consider resource requirements and document minimum system requirements clearly
- Enable staging/testing deployments that contributors can use for validation
**Common Combinations**: Often combined with Documentation, Testing, Monitoring

## Monitoring
**When to Apply**: Transparent monitoring that serves community needs while respecting privacy
**Core Principles**:
- **Community benefit**: Monitoring that helps improve project for all users
- **Privacy respect**: Minimal data collection focused on technical metrics rather than user behavior
- **Transparency**: Open about what metrics are collected and how they're used
- **Contributor insight**: Monitoring that helps contributors understand project health and impact
**Best Practices**:
- Monitor technical metrics that help identify performance issues and bugs
- Provide community with insights about project usage and health (when appropriate)
- Use monitoring to identify areas where documentation or user experience could be improved
- Implement error tracking that helps contributors diagnose and fix issues
- Document monitoring practices and respect user privacy preferences
- Share relevant monitoring insights with community to guide development priorities
**Common Combinations**: Often combined with Performance Optimization, Documentation

## Documentation
**When to Apply**: Comprehensive, inclusive documentation that enables community participation and success
**Core Principles**:
- **Accessibility**: Documentation that serves users with different technical backgrounds and abilities
- **Completeness**: Cover all aspects needed for successful use and contribution
- **Community contribution**: Enable and encourage community members to improve documentation
- **Living documentation**: Keep documentation current and accurate through community collaboration
**Best Practices**:
- Create comprehensive documentation covering installation, usage, and contribution
- Use clear, jargon-free language that serves international and diverse audiences
- Provide examples, tutorials, and practical guidance for different use cases
- Document development setup, architecture, and decision-making processes for contributors
- Create contributor guidelines that welcome and guide new community members
- Use accessible documentation formats and consider different learning styles
- Implement documentation review process and encourage community improvements
- Translate documentation to multiple languages when community capacity allows
**Common Combinations**: Always combined with all other scenarios

---

# 🤝 COMMUNITY MANAGEMENT

## Community Engagement
**When to Apply**: Building and maintaining inclusive, collaborative community relationships
**Core Principles**:
- **Inclusive participation**: Welcome contributors from all backgrounds and skill levels
- **Transparent communication**: Open, honest communication about project direction and decisions
- **Collaborative decision-making**: Involve community in important project decisions
- **Sustainable leadership**: Develop community leadership to ensure project longevity
**Best Practices**:
- Create clear code of conduct that promotes inclusive, respectful behavior
- Establish multiple communication channels for different types of community interaction
- Recognize and celebrate community contributions publicly and meaningfully
- Provide mentorship and guidance for new contributors and community members
- Create opportunities for community members to take on leadership roles
- Be responsive to community feedback and questions
- Plan for leadership transition and community sustainability

## Contributor Experience
**When to Apply**: Creating positive, productive experiences for all project contributors
**Core Principles**:
- **Low barrier to entry**: Make it easy for new contributors to get started
- **Clear expectations**: Provide guidance about contribution standards and processes
- **Supportive environment**: Help contributors succeed and learn through participation
- **Recognition and growth**: Acknowledge contributions and provide growth opportunities
**Best Practices**:
- Create comprehensive contributor documentation with step-by-step guidance
- Label issues appropriately to help contributors find suitable work
- Provide responsive feedback and mentorship for contributor questions and work
- Establish clear review processes that balance quality with encouragement
- Create pathways for contributors to increase involvement and responsibility
- Thank contributors publicly and acknowledge their specific contributions
- Provide constructive feedback that helps contributors improve their skills

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Community Focus**: Prioritize approaches that benefit and include the broader community
2. **Transparency**: Recommend open, documented processes that community can understand and improve
3. **Contributor Enablement**: Suggest solutions that make it easier for diverse contributors to participate
4. **Sustainability**: Consider long-term maintenance and community health in all recommendations
5. **Inclusivity**: Ensure recommendations don't create barriers for community members

### For Interactive Workshop (`/prompt-workshop`)
1. **Community Consultation**: Guide toward decisions that involve community input and discussion
2. **Barrier Assessment**: Identify potential obstacles to community participation and suggest mitigation
3. **Documentation Planning**: Ensure adequate documentation for community understanding and contribution
4. **Sustainability Planning**: Consider long-term community capacity and maintenance requirements

### Example AI Decision Process
**User Input**: "Add new plugin system to allow community extensions"

**Open Source AI Analysis**:
- Primary Context: Architecture Design + Community Engagement + Documentation
- Community Considerations: Enable community to extend functionality without core changes
- Documentation Needs: Plugin development guide, API documentation, example plugins
- Community Process: RFC discussion, prototype development, community testing and feedback
- Sustainability: Consider maintenance burden of plugin API and long-term commitment
- Accessibility: Ensure plugin system doesn't exclude contributors based on technical skill level