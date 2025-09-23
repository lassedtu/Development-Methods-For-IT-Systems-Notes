A supplementary specification is a document that contains textual descriptions of all other requirements not covered in the main functional requirements.

It includes non-functional requirements such as usability, reliability, performance, supportability, and other quality attributes often summarised by the acronym URPS+.

It also covers additional requirements like reports, documentation, packaging, installation, and maintenance needs.

The supplementary specification complements the main requirements by capturing details that affect how the system operates but are not directly related to specific functions.
## Example  
For an online bookstore system, the supplementary specification might include:

- **Usability:** The system should support accessibility features such as screen reader compatibility and keyboard navigation.
- **Reliability:** The system must have 99.9% uptime and automatic failover in case of server failure.
- **Performance:** Search queries should return results within 2 seconds under normal load.
- **Supportability:** The system should log all user transactions for audit purposes and provide an admin dashboard for monitoring.
- **Installation:** The software should be deployable on both Windows and Linux servers with automated installation scripts.
- **Documentation:** User manuals and API documentation must be provided in both PDF and HTML formats.

## Example  from Book
See page 104 of the textbook for a detailed example of a supplementary specification document.
A supplementary specification is a document that contains textual descriptions of all requirements not covered in the main [[Functional Requirements]]

It captures [[Non-Functional Requirements]] such as usability, reliability, performance, supportability, and other quality attributes often summarized by the [[FURPS+]] acronym

It also covers additional requirements like reports, documentation, packaging, installation, and maintenance needs

## Purpose

- **Complement [[Functional Requirements]]** by capturing non-functional aspects of the system
- **Centralize quality attributes** that affect multiple [[Use Case]]s or system components
- **Document constraints** that apply to the entire system rather than specific functions
- **Specify system-wide requirements** that don't fit naturally into [[Use Case]]s
- **Provide implementation guidance** for developers and architects

## What to Include

### [[FURPS+]] Categories

#### U - Usability Requirements
- User interface standards and guidelines
- Accessibility requirements for users with disabilities
- User experience requirements and design principles
- Help system and documentation requirements
- Training and learning curve expectations

#### R - Reliability Requirements  
- System availability and uptime requirements
- Fault tolerance and error recovery capabilities
- Data backup and recovery procedures
- System stability and robustness requirements
- Mean time between failures (MTBF) targets

#### P - Performance Requirements
- Response time requirements for different operations
- Throughput requirements for concurrent users
- Resource utilization constraints (memory, CPU, storage)
- Scalability requirements and growth projections
- Network bandwidth and latency requirements

#### S - Supportability Requirements
- System monitoring and logging requirements
- Diagnostic and troubleshooting capabilities
- Configuration management requirements
- Maintenance and update procedures
- Support tools and administrative interfaces

#### + (Plus) - Additional Requirements
- **Design constraints**: Specific technologies, platforms, or standards to use
- **Implementation requirements**: Programming languages, frameworks, or methodologies
- **Interface requirements**: Integration with external systems or legacy applications
- **Physical requirements**: Hardware specifications, environmental conditions
- **Legal requirements**: Regulatory compliance, data protection, industry standards

### System-Wide Constraints

#### Technical Constraints
- Operating system and platform requirements
- Database and middleware requirements
- Security and encryption standards
- Network and communication protocols
- Development tool and environment constraints

#### Business Constraints
- Budget and resource limitations
- Timeline and delivery constraints
- Organizational policies and procedures
- Compliance and regulatory requirements
- Licensing and intellectual property constraints

## Format and Organization

### Standard Structure
1. **Introduction** - Purpose and scope of the document
2. **[[FURPS+]] Requirements** - Organized by category
3. **Design Constraints** - Technical and business limitations
4. **System Requirements** - Hardware and software platforms
5. **Documentation Requirements** - User and system documentation needs
6. **Assumptions and Dependencies** - External factors affecting the system

### Requirement Specification Format
Each requirement should include:
- **Unique identifier** (e.g., PERF-001, SEC-015)
- **Clear description** of the requirement
- **Rationale** explaining why the requirement is needed
- **Acceptance criteria** for testing and validation
- **Priority level** using [[MoSCoW]] or similar prioritization

### Example Requirements

#### Performance Example
```
ID: PERF-001
Requirement: The system must respond to user login requests within 2 seconds under normal load conditions
Rationale: Users expect quick authentication to maintain productivity
Criteria: 95% of login attempts complete within 2 seconds during peak usage
Priority: Must Have
```

#### Usability Example  
```
ID: USE-003
Requirement: The system must be accessible to users with visual impairments
Rationale: Legal compliance with accessibility standards and inclusive design
Criteria: System passes WCAG 2.1 AA compliance testing
Priority: Must Have
```

## Relationship to Other Artifacts

### [[Functional Requirements]]
- **Complements** functional requirements by specifying quality aspects
- **Constrains** how functional requirements are implemented
- **Affects** multiple [[Use Case]]s with cross-cutting concerns

### [[Use Case]]s
- **Referenced** in [[Use Case]] special requirements sections
- **Influences** [[Use Case]] alternative flows for error handling
- **Guides** [[Use Case]] implementation through quality constraints

### Architecture and Design
- **Drives** architectural decisions and design patterns
- **Influences** technology choices and system structure
- **Guides** implementation approaches and frameworks

## Benefits

### For Development Team
- **Clear implementation guidance** for non-functional aspects
- **Centralized location** for system-wide constraints and requirements
- **Testable criteria** for validating system quality
- **Architectural guidance** for design decisions

### For [[Stakeholder]]s
- **Visibility** into quality aspects that affect user experience
- **Assurance** that non-functional concerns are addressed
- **Basis** for acceptance testing and system validation
- **Documentation** of constraints and limitations

### for Project Management
- **[[Risk identification]]** related to non-functional requirements
- **Resource planning** for performance, security, and other quality work
- **Scope management** by clearly defining system boundaries and constraints
- **Quality assurance** planning and testing strategies

## Common Content Areas

### Security Requirements
- Authentication and authorization mechanisms
- Data encryption and protection requirements
- Access control and user permission models
- Audit trails and security logging
- Vulnerability scanning and security testing

### Operational Requirements
- System monitoring and alerting capabilities
- Backup and disaster recovery procedures
- Capacity planning and scalability requirements
- Maintenance windows and update procedures
- Support and help desk integration

### Compliance Requirements
- Industry regulations and standards compliance
- Data privacy and protection requirements
- Audit and reporting capabilities
- Document retention and archival policies
- Quality standards and certification requirements

## Evolution During Development

- **[[Inception]]**: Identify major non-functional constraints that affect feasibility
- **[[Elaboration]]**: Detail supplementary specification to guide architecture decisions
- **[[Construction]]**: Use specification to validate implementation meets quality requirements
- **[[Transition]]**: Verify system meets all supplementary requirements in production

## Common Mistakes

- **Mixing functional and non-functional requirements** - Keep them clearly separated
- **Making requirements untestable** - Ensure acceptance criteria are measurable
- **Overlooking system-wide impacts** - Consider how requirements affect entire system
- **Not prioritizing requirements** - Some non-functional requirements are more critical than others
- **Forgetting maintenance requirements** - Include ongoing operational needs

The supplementary specification is essential for building systems that not only work correctly but also meet user expectations for quality, performance, and usability.
