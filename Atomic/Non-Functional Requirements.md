Non-functional requirements specify **how** the system should perform its functions rather than **what** functions it should provide

They define quality attributes, constraints, and performance criteria that affect how the system operates

Non-functional requirements are often called "quality requirements" because they describe the quality characteristics of [[Functional Requirements]]

## Characteristics

- Describe **how well** the system should perform
- Often harder to test than [[Functional Requirements]]
- Can affect multiple functional requirements simultaneously
- Usually measurable with specific criteria
- Critical for user satisfaction and system success

## FURPS+ Categories

Non-functional requirements align with the URPS+ portion of [[FURPS+]]:

### U - Usability
- How easy and pleasant the system is to use
- User interface design and user experience requirements
- Accessibility requirements for users with disabilities
- Learning curve and training requirements

**Examples:**
- New users must be able to complete registration within 5 minutes
- The system must be accessible to users with visual impairments
- Online help must be available on every screen

### R - Reliability
- How dependable and consistent the system must be
- Availability, accuracy, and fault tolerance requirements
- Error handling and recovery capabilities

**Examples:**
- The system must be available 99.9% of the time
- The system must recover from crashes within 2 minutes
- Data must be backed up every hour

### P - Performance
- How fast and efficiently the system should operate
- Response times, throughput, and resource usage
- Scalability requirements

**Examples:**
- The system must respond to user actions within 2 seconds
- The system must support 1000 concurrent users
- Database queries must return results in under 500ms

### S - Supportability
- How easy the system is to maintain and support
- Monitoring, logging, and diagnostic capabilities
- Configuration and update procedures

**Examples:**
- The system must log all errors for troubleshooting
- Configuration changes must be possible without downtime
- System monitoring must provide real-time status information

### + (Plus)
- Design constraints and implementation requirements
- Interface requirements with other systems
- Physical and environmental requirements
- Legal and regulatory compliance

**Examples:**
- The system must run on Windows 10 or higher
- All data must be encrypted using AES-256
- The system must comply with GDPR regulations

## Sources of Non-Functional Requirements

- [[Stakeholder]] expectations and constraints
- [[Business Rules]] and policies
- Technical architecture decisions
- Regulatory and compliance requirements
- Industry standards and best practices
- Operational environment constraints

## Documentation

Non-functional requirements are often documented in:
- [[Supplementary Specification]] documents
- Architecture and design documents
- Service level agreements (SLAs)
- Technical specifications

## Relationship to Functional Requirements

- Non-functional requirements **constrain** how [[Functional Requirements]] are implemented
- They often affect **multiple** functional requirements
- They can be **more expensive** to implement than functional requirements
- They are critical for **system acceptance** and user satisfaction

## Testing and Validation

Non-functional requirements require special testing approaches:
- **Performance testing** for speed and scalability
- **Usability testing** with real users
- **Security testing** for protection requirements
- **Reliability testing** for availability and recovery

## Common Challenges

- Often overlooked during requirements gathering
- Difficult to quantify and measure
- Can conflict with each other (e.g., security vs. usability)
- May emerge late in the development process
- Can be expensive to implement if not considered early

## During Development Phases

- **[[Inception]]**: Identify critical non-functional constraints
- **[[Elaboration]]**: Detail non-functional requirements that affect architecture
- **[[Construction]]**: Implement and test non-functional requirements
- **[[Transition]]**: Validate non-functional requirements in production environment
