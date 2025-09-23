A primary actor is the main user or external system that initiates interactions with the system to achieve a specific goal

The primary actor has the goal that the [[Use Case]] is designed to fulfill, and the system exists primarily to serve this actor's needs

Primary actors drive the system's functionality and represent the key stakeholders whose goals the system must satisfy

## Characteristics

- **Initiates the interaction** - Starts the [[Use Case]] by requesting something from the system
- **Has the goal** - The [[Use Case]] exists to help this actor achieve their objective  
- **Main beneficiary** - Receives the primary value from the [[Use Case]] execution
- **Outside the [[System Boundary]]** - Is external to the system being built
- **Goal-oriented** - Interacts with the system to accomplish something specific

## Identification

### How to Find Primary Actors
- Ask "**Who will use this system?**"
- Ask "**Who benefits from this functionality?**"  
- Look for **initiators** of system interactions in requirements
- Identify **goal owners** - who wants the system to do something
- Consider **different user roles** that may have different goals

### Questions to Ask
- Who starts this interaction with the system?
- Who benefits if this [[Use Case]] succeeds?
- Who would be disappointed if this [[Use Case]] fails?
- Who has the business goal this [[Use Case]] supports?

## Examples

### Library System
- **Library Member** - Borrows books, searches catalog, renews loans
- **Librarian** - Processes returns, manages member accounts, handles fines

### E-commerce System  
- **Customer** - Browses products, places orders, tracks shipments
- **Store Manager** - Updates inventory, processes refunds, views reports

### Hospital System
- **Patient** - Schedules appointments, views test results, updates information
- **Doctor** - Reviews patient records, prescribes treatments, schedules procedures

### ATM System
- **Bank Customer** - Withdraws money, checks balance, transfers funds

## Relationship to Other Actors

### vs [[Secondary Actor]]
- **Primary actor** initiates and has the goal
- **[[Secondary Actor]]** supports or provides services to help achieve the goal

### vs [[Offstage Actor]]  
- **Primary actor** directly interacts with the system
- **[[Offstage Actor]]** is affected by results but doesn't directly interact

## Multiple Primary Actors

A [[Use Case]] can have **multiple primary actors** when:
- Different actors can initiate the same goal-oriented interaction
- The [[Use Case]] serves multiple stakeholder groups simultaneously
- Various user roles need the same functionality

**Example**: "Process Payment" could have both Customer and Store Clerk as primary actors since either might initiate payment processing.

## Placement in [[Use-Case Diagram]]s

- Positioned on the **left side** of the [[System Boundary]]
- Connected to relevant [[Use Case]]s with **association lines**
- May have **stereotypes** like `<<human>>` or `<<system>>` to clarify type
- Labeled with descriptive names representing their role

## Importance in Requirements

### Drives Functional Requirements
- Primary actors help identify what [[Functional Requirements]] the system needs
- Their goals become the basis for [[Use Case]]s
- Their needs influence system features and capabilities

### Guides User Experience  
- Understanding primary actors helps design appropriate user interfaces
- Their skills and context influence [[Non-Functional Requirements]] like usability
- Their workflows affect how the system should be organized

### Supports Validation
- Primary actors help validate that the system meets real user needs
- They participate in testing and acceptance criteria definition
- Their feedback guides system refinements

## Common Mistakes

- **Confusing with [[Secondary Actor]]s** - Supporting actors are not primary
- **Making actors too generic** - "User" is less useful than "Library Member"
- **Including system components** - Actors must be external to the [[System Boundary]]
- **Missing actor variations** - Different user types may need different [[Use Case]]s
- **Ignoring actor relationships** - Some actors may have hierarchical relationships

## Evolution During Development

- **[[Inception]]**: Identify key primary actors and their major goals
- **[[Elaboration]]**: Refine actor definitions and discover additional actors
- **[[Construction]]**: Use actor definitions to guide user interface and workflow design
- **[[Transition]]**: Validate with actual primary actors that system meets their needs

Primary actors are fundamental to successful system development because they represent the real-world users whose problems the system is designed to solve.
