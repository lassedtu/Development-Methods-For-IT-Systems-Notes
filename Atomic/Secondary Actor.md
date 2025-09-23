A secondary actor supports the execution of a [[Use Case]] by providing services or resources needed by the [[Primary Actor]] or the system

Secondary actors do not initiate the [[Use Case]] or have the primary goal, but their involvement is necessary for the [[Use Case]] to succeed

Secondary actors typically respond to requests from the system rather than initiating interactions

## Characteristics

- **Provides services** - Offers functionality, data, or resources that the system needs
- **Supports the goal** - Helps fulfill the [[Primary Actor]]'s objective
- **Responds to system** - Usually contacted by the system, not the initiator
- **Outside the [[System Boundary]]** - External to the system being built
- **Service-oriented** - Exists to provide specific capabilities when requested

## Role in Use Cases

### How Secondary Actors Support Use Cases
- **Provide data** - Supply information the system needs to process
- **Perform services** - Execute tasks the system cannot do itself
- **Validate information** - Confirm or verify data provided by [[Primary Actor]]s
- **Store data** - Maintain information that the system needs to access
- **Send notifications** - Communicate results or status to external parties

### Timing of Involvement
- Usually involved **during** [[Use Case]] execution, not at the start
- Contacted by the **system** when their services are needed
- May be involved in **multiple steps** of a complex [[Use Case]]

## Examples

### E-commerce System
**[[Use Case]]**: Process Order
- **[[Primary Actor]]**: Customer  
- **Secondary Actors**: 
  - Payment Gateway - Processes credit card payment
  - Inventory Database - Checks product availability
  - Email Service - Sends order confirmation

### Library System  
**[[Use Case]]**: Borrow Book
- **[[Primary Actor]]**: Library Member
- **Secondary Actors**:
  - Member Database - Validates member status
  - Fine Calculation Service - Checks for outstanding fines
  - Notification System - Sends due date reminders

### Hospital System
**[[Use Case]]**: Schedule Appointment  
- **[[Primary Actor]]**: Patient
- **Secondary Actors**:
  - Doctor Schedule System - Checks availability
  - Insurance Verification Service - Validates coverage
  - SMS Service - Sends appointment confirmations

### ATM System
**[[Use Case]]**: Withdraw Money
- **[[Primary Actor]]**: Bank Customer
- **Secondary Actors**:
  - Bank Database - Verifies account and balance
  - Card Validation Service - Confirms card authenticity
  - Cash Dispenser - Provides physical money

## Relationship to Other Actors

### vs [[Primary Actor]]
- **[[Primary Actor]]** initiates and has the goal
- **Secondary Actor** supports and provides services

### vs [[Offstage Actor]]
- **Secondary Actor** directly participates in [[Use Case]] execution  
- **[[Offstage Actor]]** is affected by results but doesn't participate directly

## Types of Secondary Actors

### External Systems
- Databases, web services, APIs
- Payment processors, authentication services
- Legacy systems, partner systems

### Service Providers
- Email servers, SMS gateways
- Printing services, file storage systems
- Notification platforms, monitoring systems

### Validation Services  
- Authentication systems, authorization services
- Data validation services, compliance checkers
- Security scanning systems, fraud detection

## Placement in [[Use-Case Diagram]]s

- Positioned on the **right side** of the [[System Boundary]]
- Connected to relevant [[Use Case]]s with **association lines**
- May have **stereotypes** like `<<s>>` for system or `<<service>>` for service
- Labeled with descriptive names indicating their function

## Importance in System Design

### Interface Requirements
- Secondary actors help identify what **external interfaces** the system needs
- Define **communication protocols** and data formats for integration
- Specify **error handling** for when secondary actors are unavailable

### Architecture Decisions
- Influence **system architecture** by defining external dependencies
- Affect **reliability requirements** since system depends on their availability
- Guide **security requirements** for protecting communication with external actors

### Non-Functional Requirements
- Impact **performance** requirements based on response times
- Affect **reliability** since system depends on secondary actor availability
- Influence **security** requirements for external communications

## Common Mistakes

- **Confusing with [[Primary Actor]]s** - Secondary actors don't initiate or have the primary goal
- **Making internal components actors** - Secondary actors must be external to [[System Boundary]]
- **Ignoring secondary actors** - Missing them leads to incomplete [[Use Case]]s
- **Too many secondary actors** - Including every minor service clutters diagrams
- **Vague actor definitions** - "Database" is less useful than "Customer Database"

## Documentation in Use Cases

When documenting [[Use Case]]s, secondary actors should be:
- **Listed** in the participating actors section
- **Referenced** in the main flow where they provide services
- **Included** in alternative flows for error handling
- **Specified** in non-functional requirements for response times and availability

## Evolution During Development

- **[[Inception]]**: Identify major secondary actors that provide critical services
- **[[Elaboration]]**: Detail secondary actor interfaces and define integration requirements
- **[[Construction]]**: Implement interfaces and integration with secondary actors
- **[[Transition]]**: Test and validate secondary actor integrations in production

Secondary actors are essential for understanding the complete picture of how the system will operate in its real-world environment and what external dependencies must be managed.
