# Startup Development Workflow Knowledge Base

**Philosophy**: "Move fast, learn quickly, pivot when necessary. Optimize for learning and speed over perfection. Build to validate assumptions and find product-market fit."

**AI Usage Instructions**: 
- Prioritize speed to market and user feedback over perfect solutions
- Suggest lean approaches that maximize learning with minimal resources
- Focus on validating business assumptions and hypotheses
- Recommend scrappy, resourceful solutions that can scale later
- Emphasize metrics that matter for growth and product-market fit

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Building features to test business hypotheses and find product-market fit
**Core Principles**:
- **Hypothesis-driven**: Every feature should test a specific business assumption
- **Build-Measure-Learn**: Focus on learning from real user behavior
- **Speed over perfection**: Get to market fast, iterate based on data
- **Resource optimization**: Maximize value with minimal engineering time
**Best Practices**:
- Define clear success metrics and business hypotheses before building
- Build minimum viable version to test core assumption
- Use no-code/low-code solutions when possible to save engineering time
- Focus on one key metric per feature (activation, retention, revenue)
- Ship to small user segment first, expand based on results
- Be ready to pivot or kill features that don't show traction
**Common Combinations**: Often combined with Data Analysis, Performance Optimization (for growth)

## Bug Fixing
**When to Apply**: Fixing issues that impact growth metrics or user experience
**Core Principles**:
- **Triage ruthlessly**: Fix bugs that impact revenue, growth, or critical user flows first
- **Speed over polish**: Quick fixes that work are better than perfect solutions later
- **Learn from patterns**: Use bug patterns to inform product decisions
- **Technical debt is OK**: If it doesn't slow down critical path, defer it
**Best Practices**:
- Prioritize bugs by impact on key business metrics (revenue, retention, growth)
- Fix critical user experience issues immediately, defer nice-to-haves
- Use feature flags to quickly disable broken features
- Document workarounds for users while preparing proper fixes
- Track bug impact on business metrics to inform future priorities
**Common Combinations**: Often combined with Data Analysis, Monitoring

## Code Review
**When to Apply**: Lightweight reviews focused on business impact and learning
**Core Principles**:
- **Speed first**: Don't let reviews slow down critical experiments
- **Business impact**: Focus on code that affects user experience and key metrics
- **Knowledge sharing**: Ensure team can learn from each other's approaches
- **Risk assessment**: Identify changes that could break critical user flows
**Best Practices**:
- Quick reviews focused on functionality and obvious bugs
- Prioritize review of code affecting critical business flows
- Share learnings and patterns that help team move faster
- Use async reviews to avoid blocking development velocity
- Accept technical debt if it means faster time to market
**Common Combinations**: Often combined with Feature Development, Testing

## Testing
**When to Apply**: Focused testing on critical user journeys and business flows
**Core Principles**:
- **Critical path focus**: Test what matters for business success
- **Manual over automated**: Manual testing is often faster for early-stage products
- **User-focused**: Test real user scenarios, not just technical functionality
- **Fail fast**: Catch issues that would prevent user validation
**Best Practices**:
- Test critical user journeys (signup, onboarding, core value delivery)
- Use real user data and scenarios for testing
- Prioritize testing that prevents losing users or revenue
- Manual testing during development, automate only after patterns emerge
- Monitor user behavior to catch issues tests might miss
**Common Combinations**: Often combined with Feature Development, Data Analysis

---

# 🚀 GROWTH & VALIDATION

## Data Analysis
**When to Apply**: Analyzing user behavior to validate business hypotheses and drive growth
**Core Principles**:
- **Actionable insights**: Every analysis should lead to a clear business decision
- **Hypothesis validation**: Use data to confirm or refute business assumptions
- **Growth focus**: Prioritize metrics that indicate product-market fit and scalability
- **Speed over precision**: Quick insights are often more valuable than perfect analysis
**Best Practices**:
- Focus on key startup metrics: activation, retention, revenue, referral
- Use simple analytics tools that provide quick insights
- Analyze user behavior to understand product-market fit signals
- Create simple dashboards showing key business health metrics
- Run simple A/B tests to validate feature and growth hypotheses
- Present findings in terms of business impact and next actions
**Common Combinations**: Often combined with Feature Development, Performance Optimization, UI/UX Design

## Performance Optimization
**When to Apply**: Optimizing for growth metrics and user experience that drives business results
**Core Principles**:
- **Growth impact**: Focus on performance issues that affect conversion and retention
- **User experience**: Optimize what users actually experience and care about
- **Resource efficiency**: Get maximum impact with minimal engineering resources
- **Measurement driven**: Only optimize what you can measure and what matters
**Best Practices**:
- Focus on performance metrics that correlate with business metrics
- Optimize critical user flows (landing pages, signup, core product experience)
- Use simple performance monitoring to identify real user impact
- Choose high-impact, low-effort optimizations first
- Monitor how performance changes affect conversion and retention
**Common Combinations**: Often combined with Data Analysis, UI/UX Design, Monitoring

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: Building architecture that enables rapid iteration and scaling
**Core Principles**:
- **Speed to market**: Choose architecture that enables fastest development
- **Pivot-friendly**: Build systems that can adapt as business model evolves
- **Scale when needed**: Don't over-engineer for problems you don't have yet
- **Resource conscious**: Optimize for development speed and operational costs
**Best Practices**:
- Start with simple, monolithic architecture using proven frameworks
- Use managed services (PaaS, SaaS) to minimize operational overhead
- Choose boring, reliable technology over cutting-edge solutions
- Plan for rapid feature development and easy deployments
- Design for instrumentation and measurement from day one
- Keep technical debt manageable but don't let it block business progress
**Common Combinations**: Often combined with Data Analysis, Performance Optimization, Deployment

## API Changes
**When to Apply**: API development focused on enabling rapid product iteration
**Core Principles**:
- **Iteration friendly**: Design APIs that can evolve quickly with product needs
- **Client-focused**: Optimize API design for frontend and mobile development speed
- **Simple patterns**: Use consistent, predictable patterns to reduce development time
- **Growth enabling**: Design APIs that support business growth and scaling
**Best Practices**:
- Design APIs that enable rapid frontend development and iteration
- Use simple, RESTful patterns that team can implement quickly
- Version APIs only when absolutely necessary for business continuity
- Focus on APIs that enable key user experiences and business metrics
- Document APIs with practical examples for quick onboarding
**Common Combinations**: Often combined with Feature Development, Data Analysis

## Database Changes
**When to Apply**: Database evolution that supports rapid product development
**Core Principles**:
- **Iteration support**: Database design that enables quick feature development
- **Data-driven decisions**: Schema that supports analytics and growth metrics
- **Simple operations**: Database operations that team can handle without DBA expertise
- **Growth preparation**: Design that can handle business growth without major rewrites
**Best Practices**:
- Design schema to support key analytics and business metrics
- Use simple migration patterns that don't require complex coordination
- Plan for data collection that enables user behavior analysis
- Choose database solutions that scale with business growth
- Keep backup and recovery simple but reliable
**Common Combinations**: Often combined with Feature Development, Data Analysis

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Essential security measures that protect business and build user trust
**Core Principles**:
- **Business protection**: Focus on security issues that could destroy business
- **User trust**: Implement security measures that build user confidence
- **Regulatory basics**: Meet minimum compliance requirements for your market
- **Cost-effective**: Use security solutions that don't drain engineering resources
**Best Practices**:
- Implement basic security hygiene (HTTPS, input validation, authentication)
- Use established security services and libraries rather than building custom solutions
- Focus on protecting user data and preventing business-critical security incidents
- Implement security monitoring that alerts on business-threatening issues
- Regular security reviews focused on high-risk areas
**Common Combinations**: Often combined with Compliance, API Changes

## Compliance
**When to Apply**: Meeting essential compliance requirements for business operation
**Core Principles**:
- **Business enablement**: Compliance that enables business operation and growth
- **Market requirements**: Meet minimum requirements for target markets
- **User trust**: Compliance measures that build user and customer confidence
- **Resource efficiency**: Achieve compliance with minimal engineering overhead
**Best Practices**:
- Understand minimum compliance requirements for your industry and markets
- Implement compliance measures that also improve product and user experience
- Use compliance-focused services and tools to minimize custom development
- Document compliance measures for audit and customer trust purposes
- Plan compliance measures that scale with business growth
**Common Combinations**: Often combined with Security Audit, Documentation

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: User experience design focused on growth and product-market fit
**Core Principles**:
- **Conversion optimization**: Design experiences that drive business metrics
- **User validation**: Design based on real user behavior and feedback
- **Rapid iteration**: Enable quick design changes based on data and user feedback
- **Growth focus**: Design that supports user activation, retention, and referral
**Best Practices**:
- Design user onboarding that maximizes activation rates
- Create user experiences that demonstrate product value quickly
- Use simple design patterns and existing component libraries for speed
- Test design changes with real users and measure impact on business metrics
- Focus on mobile-first design if your users are primarily mobile
- Design for viral growth and user referrals
**Common Combinations**: Often combined with Data Analysis, Testing, Performance Optimization

---

# 🛠️ DEVOPS & OPERATIONS

## Deployment
**When to Apply**: Fast, reliable deployment that enables rapid iteration
**Core Principles**:
- **Speed to production**: Deploy features quickly to get user feedback
- **Reliability**: Ensure deployments don't break critical user experiences
- **Rollback readiness**: Quick recovery from deployment issues
- **Cost efficiency**: Minimize operational overhead and infrastructure costs
**Best Practices**:
- Use managed deployment platforms (Heroku, Vercel, Railway) for simplicity
- Implement feature flags for safe deployment and quick rollback
- Deploy frequently in small batches to minimize risk
- Monitor deployment impact on key business metrics
- Keep deployment process simple and team-manageable
**Common Combinations**: Often combined with Monitoring, Feature Development

## Monitoring
**When to Apply**: Monitoring focused on business health and user experience
**Core Principles**:
- **Business metrics**: Monitor metrics that indicate business health and growth
- **User experience**: Track performance and errors that affect user experience
- **Cost consciousness**: Use monitoring solutions that provide value without high costs
- **Actionable alerts**: Only alert on issues that require immediate action
**Best Practices**:
- Monitor key business metrics (user acquisition, activation, retention, revenue)
- Track application performance metrics that correlate with user satisfaction
- Set up alerts for business-critical errors and performance issues
- Use simple, cost-effective monitoring tools that team can manage
- Create dashboards showing business health alongside technical metrics
- Monitor user behavior to identify opportunities for improvement
**Common Combinations**: Often combined with Data Analysis, Performance Optimization, Deployment

## Documentation
**When to Apply**: Minimal, essential documentation that enables team efficiency
**Core Principles**:
- **Team efficiency**: Documentation that helps team move faster
- **Onboarding focus**: Help new team members contribute quickly
- **Living documentation**: Keep docs current and useful, delete outdated ones
- **User-focused**: Document what users and new team members actually need
**Best Practices**:
- Maintain simple README with setup and deployment instructions
- Document critical business logic and non-obvious technical decisions
- Keep API documentation current for frontend and integration development
- Document key metrics, analytics, and business processes
- Focus on documentation that enables faster development and debugging
**Common Combinations**: Often combined with Feature Development, API Changes

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Speed to Market**: Prioritize solutions that get working software to users fastest
2. **Learning Optimization**: Focus on approaches that maximize learning about users and market
3. **Resource Efficiency**: Suggest solutions that minimize engineering time and operational costs
4. **Measurement Focus**: Emphasize instrumentation and metrics that validate business assumptions
5. **Pivot-Friendly**: Recommend flexible approaches that can adapt as business evolves

### For Interactive Workshop (`/prompt-workshop`)
1. **Hypothesis Clarification**: Help identify and articulate business assumptions being tested
2. **Success Metrics**: Define clear, measurable outcomes that indicate success or failure
3. **Resource Planning**: Balance scope with available resources and time constraints
4. **Risk Assessment**: Identify risks that could prevent learning or harm business growth

### Example AI Decision Process
**User Input**: "Build user authentication system for our new social app"

**Startup AI Analysis**:
- Primary Context: Feature Development (enabling core product functionality)
- Business Focus: Enable user accounts for retention and engagement metrics
- Speed Approach: Use authentication service (Auth0, Firebase) rather than building custom
- Measurement: Track signup conversion, authentication success rate, user retention
- Learning Goal: Validate if users will create accounts and return to use the product
- Resource Optimization: Minimize engineering time, maximize learning about user behavior