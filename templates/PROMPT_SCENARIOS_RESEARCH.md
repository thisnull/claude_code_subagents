# Research & Academic Development Workflow Knowledge Base

**Philosophy**: "Scientific rigor, reproducibility, and open knowledge sharing. Prioritize methodological soundness, peer review readiness, and contributions to the broader scientific community."

**AI Usage Instructions**: 
- Emphasize reproducibility and methodological rigor in all recommendations
- Suggest approaches that facilitate peer review and scientific validation
- Focus on open science principles and knowledge sharing practices
- Recommend documentation standards that support scientific publication
- Consider ethical implications and research integrity in all suggestions

---

# 🚀 DEVELOPMENT LIFECYCLE

## Feature Development
**When to Apply**: Implementing research tools, experiments, and scientific applications
**Core Principles**:
- **Reproducibility**: All implementations must be reproducible by other researchers
- **Methodological soundness**: Follow established scientific computing best practices  
- **Open science**: Design for sharing and collaboration with the research community
- **Hypothesis-driven**: Every feature should serve a clear research hypothesis or question
**Best Practices**:
- Document all implementation decisions with scientific rationale and literature references
- Use version control for all code, data, and analysis scripts with detailed commit messages
- Implement parameter logging and experiment tracking for reproducibility
- Follow established scientific computing frameworks and conventions
- Create modular, reusable components that other researchers can build upon
- Include comprehensive unit tests and validation against known results
- Plan for computational reproducibility across different environments and platforms
**Common Combinations**: Always combined with Documentation, Testing, Data Management

## Bug Fixing
**When to Apply**: Correcting errors in research code, analysis scripts, or scientific applications
**Core Principles**:
- **Scientific accuracy**: Bugs in research code can invalidate scientific conclusions
- **Methodological transparency**: Document all bug fixes and their impact on results
- **Reproducibility maintenance**: Ensure fixes don't break existing reproducible workflows
- **Peer review readiness**: Fix bugs with the same rigor as initial implementation
**Best Practices**:
- Analyze the scientific impact of bugs on published or pending research results
- Document bug fixes with detailed analysis of impact on previous results
- Re-run affected analyses and update results if scientific conclusions are impacted
- Implement regression tests to prevent similar bugs in future research
- Notify collaborators and reviewers if bug fixes affect shared research outcomes
- Use version control to track exactly when and how bugs were fixed
- Consider whether bug fixes warrant correction notices or updates to published work
**Common Combinations**: Often combined with Data Validation, Peer Review, Documentation

## Code Review
**When to Apply**: Scientific peer review of research code, analysis scripts, and computational methods
**Core Principles**:
- **Scientific rigor**: Review code for methodological soundness and accuracy
- **Reproducibility verification**: Ensure code can be reproduced by other researchers
- **Best practices compliance**: Follow established scientific computing standards
- **Knowledge sharing**: Use reviews as opportunities for methodological learning
**Best Practices**:
- Review code against established scientific computing best practices and domain standards
- Verify that implementations match described methods and theoretical foundations
- Check for appropriate statistical methods and computational approaches
- Ensure adequate documentation for reproducibility and peer review
- Validate that code handles edge cases and error conditions scientifically appropriately
- Review for ethical considerations and responsible research practices
- Provide constructive feedback that improves both code quality and scientific rigor
**Common Combinations**: Always combined with Peer Review, Documentation, Methodology Validation

## Testing
**When to Apply**: Validation of research code, scientific algorithms, and computational experiments
**Core Principles**:
- **Scientific validation**: Tests must verify scientific accuracy, not just technical functionality
- **Known results validation**: Test against established benchmarks and known results
- **Statistical significance**: Include appropriate statistical testing and validation
- **Reproducibility verification**: Tests should verify that results can be reproduced
**Best Practices**:
- Test implementations against analytical solutions and established benchmarks
- Include statistical tests for algorithms that should produce specific statistical properties
- Validate numerical stability and precision requirements for scientific computations
- Test edge cases and boundary conditions relevant to scientific domains
- Implement integration tests that verify entire research workflows
- Include tests for data quality and validation procedures
- Document test methodologies and their scientific rationale
**Common Combinations**: Always combined with Validation, Scientific Computing, Quality Assurance

---

# 🏗️ TECHNICAL ARCHITECTURE

## Architecture Design
**When to Apply**: Designing computational research infrastructure and scientific computing systems
**Core Principles**:
- **Computational reproducibility**: Architecture must support reproducible computational research
- **Scalability for research**: Design for research-scale computational requirements
- **Data management**: Proper handling of research data with provenance tracking
- **Collaboration support**: Enable multi-investigator collaboration and sharing
**Best Practices**:
- Design systems that capture complete computational provenance and metadata
- Use containerization and environment management for computational reproducibility
- Implement proper data management with version control and access tracking
- Plan for computational scalability from desktop to high-performance computing
- Design APIs and interfaces that support research workflows and collaboration
- Include mechanisms for experiment tracking, parameter management, and result archival
- Consider long-term preservation and accessibility of research computational artifacts
**Common Combinations**: Often combined with Data Management, High-Performance Computing, Collaboration

## API Changes
**When to Apply**: Evolving research software APIs and computational interfaces
**Core Principles**:
- **Backward compatibility**: Maintain compatibility with existing research workflows
- **Scientific accuracy**: API changes must not compromise scientific validity
- **Documentation completeness**: Comprehensive API documentation for scientific users
- **Community coordination**: Coordinate API changes with research community users
**Best Practices**:
- Follow semantic versioning with clear communication about scientific impact of changes
- Provide extensive API documentation with scientific examples and use cases
- Implement comprehensive testing including validation against scientific benchmarks
- Coordinate with research community before making breaking changes
- Provide migration guides that address scientific workflow implications
- Include provenance tracking capabilities in API design
- Design APIs that support batch processing and high-throughput scientific computing
**Common Combinations**: Often combined with Scientific Computing, Community Engagement, Documentation

## Database Changes
**When to Apply**: Managing research databases, experimental data, and scientific datasets
**Core Principles**:
- **Data integrity**: Absolute protection of research data integrity and provenance
- **Metadata preservation**: Maintain comprehensive metadata and data lineage
- **FAIR principles**: Ensure data is Findable, Accessible, Interoperable, and Reusable
- **Ethical compliance**: Follow ethical guidelines for research data management
**Best Practices**:
- Implement comprehensive data validation and integrity checking procedures
- Maintain detailed metadata and provenance information for all research data
- Use database migration procedures that preserve complete data history
- Implement access controls that comply with research ethics and data sharing agreements
- Design database schemas that support scientific querying and analysis workflows
- Plan for long-term data preservation and accessibility requirements
- Include audit trails and version control for all research data modifications
**Common Combinations**: Always combined with Data Management, Ethics Compliance, Metadata Management

---

# 📊 DATA & ANALYTICS

## Data Analysis
**When to Apply**: Scientific data analysis, statistical modeling, and research insights generation
**Core Principles**:
- **Statistical rigor**: Use appropriate statistical methods with proper assumptions validation
- **Reproducibility**: All analyses must be completely reproducible by other researchers
- **Transparency**: Document all analytical decisions and assumptions clearly
- **Peer review readiness**: Structure analysis for scientific peer review and publication
**Best Practices**:
- Document all data preprocessing steps with complete methodology and rationale
- Use appropriate statistical methods with validation of underlying assumptions
- Implement reproducible analysis workflows with version control and environment management
- Include appropriate statistical significance testing and effect size reporting
- Create comprehensive analysis documentation suitable for peer review
- Validate results against known benchmarks and previous research when applicable
- Include sensitivity analyses and robustness checks for key findings
**Common Combinations**: Always combined with Statistical Validation, Reproducibility, Peer Review

## Machine Learning
**When to Apply**: ML applications in research contexts with emphasis on interpretability and validation
**Core Principles**:
- **Scientific interpretability**: ML models must be interpretable and scientifically meaningful
- **Rigorous validation**: Use appropriate validation methodologies for scientific applications
- **Reproducibility**: Complete reproducibility of ML workflows and results
- **Ethical considerations**: Address bias, fairness, and ethical implications in research contexts
**Best Practices**:
- Use cross-validation and holdout testing appropriate for scientific research questions
- Implement model interpretability and explainability techniques suitable for peer review
- Document complete ML pipelines including data preprocessing, feature engineering, and model selection
- Include appropriate baseline comparisons and statistical significance testing
- Address potential biases and ethical implications of ML applications in research
- Use reproducible ML workflows with version control for code, data, and models
- Validate ML results against domain knowledge and established scientific principles
**Common Combinations**: Often combined with Statistical Analysis, Ethics Review, Interpretability

## Data Management
**When to Apply**: Research data lifecycle management, sharing, and preservation
**Core Principles**:
- **FAIR principles**: Make research data Findable, Accessible, Interoperable, and Reusable
- **Data integrity**: Maintain complete data integrity and provenance throughout lifecycle
- **Ethical compliance**: Follow ethical guidelines and legal requirements for research data
- **Long-term preservation**: Plan for long-term accessibility and preservation of research data
**Best Practices**:
- Implement comprehensive data management plans following funding agency requirements
- Use standardized metadata schemas and controlled vocabularies for research domains
- Establish proper access controls and sharing agreements for research data
- Plan for data preservation and long-term accessibility beyond project duration
- Implement version control and provenance tracking for all research datasets
- Follow domain-specific data sharing standards and repository requirements
- Include data quality assessment and validation procedures
**Common Combinations**: Always combined with Ethics Compliance, Metadata Standards, Preservation

---

# 🔒 SECURITY & COMPLIANCE

## Security Audit
**When to Apply**: Protecting research data and computational infrastructure
**Core Principles**:
- **Research data protection**: Secure handling of sensitive research data and participants' information
- **Intellectual property protection**: Protect proprietary research methods and unpublished results
- **Collaborative security**: Secure sharing and collaboration while maintaining openness
- **Compliance**: Meet institutional and funding agency security requirements
**Best Practices**:
- Implement appropriate access controls for sensitive research data and computing resources
- Use encryption and secure communication for confidential research collaboration
- Follow institutional and funding agency security requirements and guidelines
- Implement secure backup and disaster recovery procedures for research data and code
- Monitor and audit access to research computing resources and sensitive data
- Provide security training for research team members handling sensitive data
- Plan for incident response and breach notification procedures specific to research contexts
**Common Combinations**: Often combined with Ethics Compliance, Data Protection, Institutional Policy

## Compliance
**When to Apply**: Meeting regulatory, ethical, and funding requirements for research projects
**Core Principles**:
- **Ethics compliance**: Follow human subjects research ethics and institutional guidelines
- **Funding compliance**: Meet all funding agency requirements and reporting obligations
- **Data protection**: Comply with data protection regulations (GDPR, HIPAA, etc.)
- **Institutional policy**: Follow all institutional research policies and procedures
**Best Practices**:
- Obtain necessary ethics approvals and institutional review board clearances
- Follow funding agency requirements for data management, sharing, and preservation
- Implement appropriate consent and privacy protection procedures for human subjects research
- Maintain comprehensive documentation for compliance audits and reporting
- Coordinate with institutional compliance offices for complex regulatory requirements
- Plan for ongoing compliance monitoring and reporting throughout research project lifecycle
- Include compliance considerations in research planning and resource allocation
**Common Combinations**: Always combined with Ethics Review, Data Protection, Institutional Oversight

---

# 🎨 USER EXPERIENCE

## UI/UX Design
**When to Apply**: Designing interfaces for research tools, scientific applications, and data visualization
**Core Principles**:
- **Scientific workflow support**: Design interfaces that support actual research workflows
- **Data visualization excellence**: Create clear, accurate, and meaningful visualizations
- **Accessibility for researchers**: Ensure interfaces are accessible to researchers with diverse needs
- **Domain expertise integration**: Design with deep understanding of scientific domain requirements
**Best Practices**:
- Conduct user research with actual researchers and scientific domain experts
- Design interfaces that support complex scientific workflows and data exploration
- Create visualization interfaces that accurately represent scientific data and uncertainty
- Follow established scientific visualization best practices and conventions
- Ensure interfaces are accessible to researchers with diverse abilities and technical backgrounds
- Design for collaboration and sharing of scientific results and visualizations
- Include documentation and help systems tailored to scientific users
**Common Combinations**: Often combined with Scientific Visualization, Domain Expertise, Accessibility

## Scientific Visualization
**When to Apply**: Creating visualizations for scientific data, results, and publications
**Core Principles**:
- **Accuracy**: Visualizations must accurately represent scientific data and relationships
- **Clarity**: Clear communication of scientific concepts and findings
- **Publication quality**: Visualizations suitable for peer review and scientific publication
- **Reproducibility**: Visualization code and methods must be reproducible
**Best Practices**:
- Follow established scientific visualization best practices and domain conventions
- Include appropriate uncertainty visualization and statistical significance indicators
- Use colorblind-friendly color schemes and accessible visualization techniques
- Create publication-quality figures with appropriate resolution and formatting
- Document visualization methods and provide reproducible visualization code
- Include appropriate statistical summaries and significance testing in visualizations
- Design visualizations that support both exploratory analysis and publication
**Common Combinations**: Always combined with Data Analysis, Publication Preparation, Accessibility

---

# 🛠️ DEVOPS & OPERATIONS

## CI/CD Pipeline
**When to Apply**: Automated workflows for research code, analysis pipelines, and scientific applications
**Core Principles**:
- **Reproducibility automation**: Automated workflows that ensure computational reproducibility
- **Quality assurance**: Comprehensive testing and validation appropriate for scientific code
- **Environment management**: Consistent computational environments across development and production
- **Collaboration support**: Pipelines that support multi-investigator collaboration
**Best Practices**:
- Implement automated testing including validation against known scientific results
- Use containerization and environment management for reproducible computational workflows
- Include automated quality checks for code style, documentation, and scientific best practices
- Set up automated workflows for data processing and analysis pipeline execution
- Implement continuous integration testing across multiple computational environments
- Include automated generation of analysis reports and scientific documentation
- Plan for automated archival and preservation of computational workflows
**Common Combinations**: Often combined with Environment Management, Quality Assurance, Collaboration

## Deployment
**When to Apply**: Deploying research applications, computational pipelines, and scientific tools
**Core Principles**:
- **Computational reproducibility**: Deployments must ensure reproducible computational environments
- **Research continuity**: Minimize disruption to ongoing research workflows
- **Collaboration support**: Enable easy access for research collaborators and reviewers
- **Long-term availability**: Plan for long-term availability of research computational tools
**Best Practices**:
- Use containerization and environment specification for reproducible deployments
- Deploy research applications with comprehensive documentation and usage examples
- Implement health monitoring appropriate for research computational workflows
- Plan for scaling deployments from individual use to research group or community use
- Include data backup and disaster recovery procedures for research applications
- Document deployment procedures for research reproducibility and sharing
- Consider computational resource requirements and cost management for research deployments
**Common Combinations**: Often combined with Environment Management, Resource Planning, Documentation

## Monitoring
**When to Apply**: Monitoring research computing infrastructure and scientific applications
**Core Principles**:
- **Research workflow monitoring**: Monitor computational workflows critical to research progress
- **Resource utilization**: Track computational resource usage for research budget management
- **Data integrity monitoring**: Ensure ongoing integrity of research data and computations
- **Performance tracking**: Monitor performance of scientific computations and algorithms
**Best Practices**:
- Monitor computational workflows and alert on failures that would impact research progress
- Track resource utilization for research budget planning and optimization
- Implement data integrity monitoring and validation for research datasets
- Monitor performance of scientific algorithms and computational methods
- Set up monitoring for long-running research computations and experiments
- Include monitoring of research collaboration tools and shared resources
- Plan for monitoring that supports research reproducibility and audit requirements
**Common Combinations**: Often combined with Resource Management, Data Integrity, Performance Analysis

## Documentation
**When to Apply**: Comprehensive documentation for research code, methods, and computational workflows
**Core Principles**:
- **Scientific reproducibility**: Documentation must enable complete reproduction by other researchers
- **Peer review readiness**: Documentation suitable for scientific peer review and publication
- **Methodological transparency**: Complete transparency of methods and implementation decisions
- **Long-term preservation**: Documentation that supports long-term research data and code preservation
**Best Practices**:
- Document all code with comprehensive comments explaining scientific rationale and methodology
- Create detailed README files with complete setup instructions and computational requirements
- Include comprehensive methodology documentation suitable for scientific publication
- Document all data sources, preprocessing steps, and analytical decisions
- Provide worked examples and tutorials for research code and methods
- Include citation information and acknowledgments for research software and data
- Plan for documentation preservation and long-term accessibility
**Common Combinations**: Always combined with all research scenarios

---

# 🤝 RESEARCH COLLABORATION

## Peer Review
**When to Apply**: Scientific peer review of research code, methods, and computational workflows
**Core Principles**:
- **Scientific rigor**: Review for methodological soundness and scientific accuracy
- **Reproducibility verification**: Verify that research can be reproduced by independent researchers
- **Community standards**: Follow established peer review practices in scientific domains
- **Constructive feedback**: Provide feedback that improves both science and code quality
**Best Practices**:
- Review research code against established scientific computing best practices
- Verify reproducibility by attempting to reproduce key results independently
- Check methodological soundness and appropriateness of analytical approaches
- Provide detailed, constructive feedback on both scientific and technical aspects
- Follow community standards for peer review in relevant scientific domains
- Include feedback on documentation quality and suitability for publication
- Coordinate peer review timelines with research publication and funding deadlines
**Common Combinations**: Always combined with Scientific Validation, Community Engagement, Publication

## Community Engagement
**When to Apply**: Engaging with scientific communities and research collaborations
**Core Principles**:
- **Open science**: Promote open sharing of research methods, code, and data
- **Community contribution**: Contribute to scientific community resources and tools
- **Knowledge sharing**: Share research outcomes and methodologies with broader community
- **Collaboration facilitation**: Enable and facilitate scientific collaboration
**Best Practices**:
- Participate actively in relevant scientific communities and professional organizations
- Share research code and data through appropriate scientific repositories and platforms
- Present research methods and results at scientific conferences and workshops
- Contribute to community scientific software and research infrastructure projects
- Engage with other researchers through collaborative platforms and social networks
- Provide mentorship and training for students and early-career researchers
- Support peer review and editorial activities in scientific publication
**Common Combinations**: Often combined with Knowledge Sharing, Mentorship, Publication

---

## AI Usage Guidelines

### For Automated Refinement (`/refine-prompt`)
1. **Scientific Rigor**: Emphasize methodological soundness and scientific accuracy in all recommendations
2. **Reproducibility Focus**: Prioritize approaches that ensure complete computational reproducibility
3. **Peer Review Readiness**: Suggest practices that prepare work for scientific peer review and publication
4. **Open Science**: Recommend approaches that support open science principles and community sharing
5. **Ethical Considerations**: Include research ethics and responsible conduct considerations

### For Interactive Workshop (`/prompt-workshop`)
1. **Research Question Alignment**: Help align technical approaches with underlying research questions
2. **Methodological Validation**: Guide selection of appropriate scientific methods and statistical approaches
3. **Reproducibility Planning**: Develop comprehensive plans for computational reproducibility
4. **Publication Strategy**: Consider publication and dissemination strategies in technical planning

### Example AI Decision Process
**User Input**: "Analyze large genomics dataset to identify disease biomarkers"

**Research AI Analysis**:
- Primary Context: Data Analysis + Machine Learning (scientific research focus)
- Research Considerations: Statistical power analysis, multiple testing correction, biological significance
- Reproducibility Requirements: Complete pipeline documentation, version control, environment specification
- Ethics Requirements: Human subjects considerations, data privacy, consent validation
- Publication Planning: Methods documentation suitable for peer review, result validation, community sharing