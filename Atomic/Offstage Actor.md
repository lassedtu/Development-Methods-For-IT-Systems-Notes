An offstage actor (also called tertiary actor) is an entity that does not interact directly with the system but is affected by its outcome or has an interest in the [[Use Case]] execution

Offstage actors have a stake in the [[Use Case]] results but remain outside the immediate flow of actions between the system and other actors

They represent important [[Stakeholder]]s whose interests must be considered even though they don't directly participate

## Characteristics

- **No direct interaction** - Does not communicate directly with the system during [[Use Case]] execution
- **Affected by outcomes** - Is impacted by the results or consequences of the [[Use Case]]
- **Has interests** - Cares about the success or failure of the [[Use Case]]
- **Outside the [[System Boundary]]** - External to the system being built
- **Indirect involvement** - May receive reports, notifications, or other indirect communication

## Role in Use Cases

### How Offstage Actors Are Affected
- **Receive reports** - Get summaries or analyses of system activity
- **Experience consequences** - Feel the business impact of system operations
- **Monitor compliance** - Oversee regulatory or policy adherence
- **Make decisions** - Use system outputs to guide business choices
- **Audit activities** - Review system operations for various purposes

### When They Matter
- During **requirements gathering** to ensure all [[Stakeholder]] needs are considered
- In **non-functional requirements** that address their concerns about system behavior
- For **compliance requirements** when they represent regulatory bodies
- In **reporting requirements** when they need information about system activities

## Examples

### E-commerce System
**[[Use Case]]**: Process Order
- **[[Primary Actor]]**: Customer
- **[[Secondary Actor]]**: Payment Gateway  
- **Offstage Actors**:
  - Tax Authority - Interested in tax calculations and reporting
  - Company Accountant - Needs sales data for financial records
  - Shipping Manager - Affected by order volume for logistics planning

### Library System
**[[Use Case]]**: Borrow Book
- **[[Primary Actor]]**: Library Member
- **[[Secondary Actor]]**: Member Database
- **Offstage Actors**:
  - Library Director - Monitors circulation statistics for budget planning
  - Book Publisher - Interested in usage data for popular titles
  - City Council - Concerned with library service effectiveness

### Hospital System  
**[[Use Case]]**: Schedule Appointment
- **[[Primary Actor]]**: Patient
- **[[Secondary Actor]]**: Doctor Schedule System
- **Offstage Actors**:
  - Hospital Administrator - Monitors scheduling efficiency and capacity
  - Insurance Company - Interested in appointment frequency and costs
  - Health Department - Tracks public health service utilization

### Banking System
**[[Use Case]]**: Process Loan Application
- **[[Primary Actor]]**: Loan Applicant
- **[[Secondary Actor]]**: Credit Rating Service
- **Offstage Actors**:
  - Bank Regulator - Monitors lending practices for compliance
  - Risk Management Department - Analyzes portfolio risk from new loans
  - Bank Shareholders - Affected by loan performance and profitability

## Relationship to Other Actors

### vs [[Primary Actor]]
- **[[Primary Actor]]** directly interacts and has the goal
- **Offstage Actor** is affected by results but doesn't interact

### vs [[Secondary Actor]]  
- **[[Secondary Actor]]** directly participates by providing services
- **Offstage Actor** has interests but doesn't participate directly

## Types of Offstage Actors

### Regulatory Bodies
- Government agencies requiring compliance reporting
- Industry regulators monitoring business practices
- Auditing organizations checking adherence to standards

### Management and Oversight
- Executives interested in business performance metrics
- Managers affected by operational efficiency changes  
- Board members concerned with strategic outcomes

### External Stakeholders
- Partner organizations impacted by system changes
- Community groups affected by service delivery
- Investors interested in business performance

### Support and Operations  
- IT support teams responsible for system maintenance
- Business analysts monitoring system effectiveness
- Quality assurance teams tracking system performance

## Placement in [[Use-Case Diagram]]s

- Often placed **at the bottom** or away from main actors
- Connected with **dashed lines** to show indirect involvement  
- May be **grouped separately** to show they don't directly interact
- Sometimes **omitted** from diagrams but documented in [[Use Case]] descriptions

## Importance in Requirements

### Non-Functional Requirements
- May drive **reporting requirements** for management dashboards
- Influence **audit trail requirements** for compliance tracking
- Affect **performance requirements** for management reporting systems

### Compliance Requirements
- Help identify **regulatory requirements** that must be met
- Guide **data retention policies** for audit purposes
- Influence **security requirements** for protecting sensitive information

### Reporting Requirements
- Drive **report generation features** for management information
- Influence **data analysis capabilities** for business intelligence
- Affect **dashboard and monitoring features** for operational oversight

## Common Mistakes

- **Confusing with direct actors** - Offstage actors don't interact directly with the system
- **Ignoring them completely** - Missing important [[Stakeholder]] concerns
- **Making them too prominent** - They shouldn't clutter the main [[Use Case]] flow
- **Including internal system components** - Must be external to the [[System Boundary]]
- **Forgetting their influence** - Their requirements can significantly affect system design

## Documentation Considerations

In [[Use Case]] documentation, offstage actors should be:
- **Listed** in stakeholder and interests section
- **Considered** when defining success criteria
- **Included** in reporting and notification requirements
- **Referenced** in compliance and audit requirements

## Evolution During Development

- **[[Inception]]**: Identify key offstage actors and their major interests
- **[[Elaboration]]**: Detail their requirements and how system outcomes affect them
- **[[Construction]]**: Implement reporting and compliance features they require
- **[[Transition]]**: Validate that their information needs are met

Offstage actors are crucial for ensuring the system serves all [[Stakeholder]] interests and complies with business, regulatory, and operational requirements, even if they don't directly interact with the system.
