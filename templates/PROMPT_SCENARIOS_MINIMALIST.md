# Minimalist Development Workflow Knowledge Base

**Philosophy**: "Build the simplest thing that works. Avoid over-engineering. Focus on core functionality and user value."

**AI Usage Instructions**: 
- Prioritize simple, direct solutions over complex architectures
- Suggest minimal viable implementations first
- Avoid recommending unnecessary processes or documentation
- Focus on getting working software shipped quickly
- Recommend complexity only when absolutely necessary

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Building new features with MVP approach
**Core Principles**:
- **Start simple**: Build the minimum viable version first
- **Avoid complexity**: Don't add features "just in case"
- **Ship fast**: Get working software in users' hands quickly
- **Iterate based on feedback**: Let real usage drive improvements
**Best Practices**:
- Write just enough tests to ensure core functionality works
- Document only what users actually need to know
- Choose simple, proven technologies over cutting-edge solutions
- Defer optimization until performance becomes a real problem
- Focus on one feature at a time to avoid scope creep
**Common Combinations**: Often combined with Bug Fixing, Testing (minimal)

## Bug Fixing
**When to Apply**: Resolving issues with focus on speed and simplicity
**Core Principles**:
- **Fix root cause**: Don't just patch symptoms
- **Keep it simple**: Avoid complex fixes for simple problems
- **Ship quickly**: Don't let perfect be the enemy of good
- **Learn from patterns**: Notice repeated issues but don't over-engineer solutions
**Best Practices**:
- Write minimal tests to verify the fix works
- Document fixes only if they involve non-obvious business logic
- Prefer simple, readable code over clever optimizations
- Fix in production if it's faster than staging (with proper backups)
**Common Combinations**: Often combined with Testing (targeted)

## Code Review
**When to Apply**: Quick quality checks without bureaucracy
**Core Principles**:
- **Focus on correctness**: Does it work and solve the problem?
- **Readability matters**: Can someone understand this in 6 months?
- **No bike-shedding**: Avoid nitpicking on style preferences
- **Ship when ready**: Don't delay for minor improvements
**Best Practices**:
- Check for obvious bugs and security issues
- Ensure code follows basic project conventions
- Ask "Is this the simplest way to solve the problem?"
- Approve quickly if functionality is correct
**Common Combinations**: Often combined with Bug Fixing

## Testing
**When to Apply**: Essential testing without over-testing
**Core Principles**:
- **Test what matters**: Focus on business-critical functionality
- **Avoid test theater**: Don't write tests just to hit coverage metrics
- **Fast feedback**: Prefer quick manual testing over slow automated suites
- **User-focused**: Test from user perspective, not implementation details
**Best Practices**:
- Write tests for core business logic and edge cases
- Use manual testing for UI and user experience validation
- Skip tests for simple getters/setters and obvious code
- Run tests locally before pushing, skip CI/CD complexity when possible
**Common Combinations**: Often combined with Feature Development, Bug Fixing

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: When simple solutions become genuinely insufficient
**Core Principles**:
- **Monolith first**: Start simple, split only when necessary
- **Boring technology**: Choose proven, stable solutions
- **YAGNI principle**: You Aren't Gonna Need It
- **Scale when needed**: Don't design for problems you don't have
**Best Practices**:
- Start with the simplest architecture that could work
- Use existing platforms and services instead of building from scratch
- Prefer configuration over custom code
- Document only the non-obvious architectural decisions
**Common Combinations**: Often combined with Performance Optimization (when needed)

## API Changes
**When to Apply**: Simple API modifications without over-engineering
**Core Principles**:
- **Backward compatibility**: Don't break existing users
- **Simple versioning**: Use URL versioning (/v1, /v2) only when necessary
- **Progressive enhancement**: Add new fields, don't remove old ones
- **User-focused**: Design APIs for ease of use, not theoretical perfection
**Best Practices**:
- Add new endpoints rather than modifying existing ones
- Use simple, obvious naming conventions
- Include basic examples in documentation
- Test API changes with real client code
**Common Combinations**: Often combined with Feature Development, Testing

## Database Changes
**When to Apply**: Database modifications with safety focus
**Core Principles**:
- **Safety first**: Always have backups and rollback plan
- **Incremental changes**: Make small, reversible modifications
- **Keep it simple**: Use standard SQL, avoid fancy database features
- **Data integrity**: Ensure data consistency but don't over-normalize
**Best Practices**:
- Test migrations on copy of production data
- Use database tools for migrations, not custom scripts
- Add columns instead of modifying existing ones when possible
- Keep old columns until sure new ones work
**Common Combinations**: Often combined with Feature Development, Data Migration

---

# 📊 DATA & ANALYTICS

## Data Analysis
**When to Apply**: Simple analysis for quick insights
**Core Principles**:
- **Answer specific questions**: Don't explore data aimlessly
- **Use simple tools**: Excel/Sheets before complex analytics platforms
- **Visual over complex**: Simple charts over advanced statistical analysis
- **Action-oriented**: Focus on insights that lead to decisions
**Best Practices**:
- Start with basic descriptive statistics
- Use simple visualization tools (charts, graphs)
- Document assumptions but avoid academic-level rigor
- Present findings in business language, not technical jargon
**Common Combinations**: Often combined with Performance Optimization

## Performance Optimization
**When to Apply**: Only when performance becomes a real user problem
**Core Principles**:
- **Measure first**: Don't optimize based on assumptions
- **Focus on user impact**: Optimize what users actually experience
- **Low-hanging fruit**: Fix obvious issues before complex optimizations
- **Cost-benefit analysis**: Don't spend weeks optimizing minor issues
**Best Practices**:
- Use simple profiling tools to identify bottlenecks
- Optimize database queries before application code
- Cache frequently accessed data with simple solutions
- Monitor basic metrics (response time, error rate)
**Common Combinations**: Often combined with Bug Fixing, Monitoring

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Basic security without paranoia
**Core Principles**:
- **Common vulnerabilities**: Focus on OWASP Top 10
- **Practical security**: Use proven libraries and frameworks
- **Don't roll your own**: Use existing authentication and encryption
- **Regular updates**: Keep dependencies updated
**Best Practices**:
- Use established authentication libraries
- Sanitize user inputs with proven methods
- Use HTTPS everywhere
- Run basic security scanning tools
- Keep sensitive data out of logs and version control
**Common Combinations**: Often combined with Code Review

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: Simple, user-focused interface design
**Core Principles**:
- **User needs first**: Solve real problems, not imaginary ones
- **Simple interfaces**: Less is more
- **Familiar patterns**: Use conventions users already know
- **Fast iteration**: Build, test, improve quickly
**Best Practices**:
- Start with wireframes or simple mockups
- Use existing UI component libraries
- Test with real users early and often
- Make interfaces obvious and self-explanatory
**Common Combinations**: Often combined with Testing, Performance Optimization

---

# 🛠️ DEVOPS & OPERATIONS

## Deployment
**When to Apply**: Simple, reliable deployment process
**Core Principles**:
- **Simple deployment**: Use platform-as-a-service when possible
- **Fast rollback**: Always have a way to quickly revert changes
- **Minimal downtime**: But don't over-engineer for zero downtime
- **Reliable process**: Prefer boring, proven deployment methods
**Best Practices**:
- Use managed hosting platforms (Heroku, Vercel, etc.)
- Deploy during low-traffic hours
- Keep deployment scripts simple and readable
- Test deployment process on staging environment
**Common Combinations**: Often combined with Monitoring

## Monitoring
**When to Apply**: Basic monitoring without over-engineering
**Core Principles**:
- **Essential metrics**: Monitor what matters for users
- **Simple alerts**: Get notified when things break
- **Easy debugging**: Make it simple to find and fix issues
- **Cost-effective**: Use free/cheap monitoring tools
**Best Practices**:
- Monitor application uptime and basic performance metrics
- Set up alerts for critical errors and downtime
- Use simple logging for debugging (console.log is fine)
- Check logs regularly, don't just rely on automated monitoring
**Common Combinations**: Often combined with Performance Optimization, Deployment

## Documentation
**When to Apply**: Just enough documentation to be useful
**Core Principles**:
- **User-focused**: Write for people who need to use or modify the code
- **Keep it current**: Outdated docs are worse than no docs
- **Just enough**: Don't document the obvious
- **Practical examples**: Show how to do common tasks
**Best Practices**:
- Write README files with setup and usage instructions
- Comment complex business logic in code
- Document deployment and troubleshooting procedures
- Keep documentation in the same repo as the code
**Common Combinations**: Often combined with Feature Development, Deployment

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Simplicity First**: Always suggest the simplest approach that solves the problem
2. **Avoid Over-Engineering**: Don't recommend complex patterns unless absolutely necessary
3. **Practical Focus**: Prioritize solutions that can be implemented quickly
4. **User Value**: Keep the focus on delivering value to end users
5. **Incremental Approach**: Suggest building incrementally rather than big-bang solutions

### For Interactive Workshop (`/prompt-workshop`)
1. **Challenge Complexity**: Ask if simpler approaches might work
2. **Time-Boxing**: Help users focus on what can be delivered quickly
3. **MVP Thinking**: Guide towards minimum viable solutions
4. **Real-World Constraints**: Consider practical limitations like time and resources

### Example AI Decision Process
**User Input**: "Build a scalable microservices architecture for user management"

**Minimalist AI Analysis**:
- Primary Context: Architecture Design (but question the complexity)
- Suggested Approach: "Start with a simple monolithic user service first"
- Focus: Basic CRUD operations, simple database, proven framework
- Avoid: Microservices complexity, over-engineering for unknown scale
- Next Steps: Build simple version, measure actual usage, scale only when needed