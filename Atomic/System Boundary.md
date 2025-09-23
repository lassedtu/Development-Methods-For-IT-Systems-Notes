The system boundary defines what is inside the system being built and what is outside of it

It separates the parts of the world that the system will control from everything else in the environment

The system boundary is crucial for understanding the scope of the system and determining which functionalities belong to the system versus external entities

## Visual Representation

- Shown as a **rectangle** in [[Use-Case Diagram]]s
- Everything **inside the rectangle** is part of the system
- Everything **outside the rectangle** is external to the system
- The **system name** is usually written at the top of the rectangle

## Key Rules

### What Goes Inside
- **[[Use Case]]s** - The functions and goals the system provides
- **System functionality** - What the system is responsible for
- **Internal processes** - Business logic controlled by the system

### What Goes Outside  
- **[[Actor]]s** - Users, external systems, and organizations
- **External systems** - Other software systems the system interacts with
- **External entities** - People, organizations, or devices not part of the system

## Importance in System Design

### Clarifies Scope
- Helps determine what features to build versus what to integrate with
- Prevents scope creep by clearly defining system limits
- Guides architectural decisions about system interfaces

### Defines Interfaces  
- Identifies where the system needs to interact with external entities
- Helps specify communication protocols and data exchanges
- Determines integration requirements with other systems

### Supports Analysis
- Helps identify all [[Actor]]s that interact with the system
- Clarifies responsibilities - what the system does vs what others do
- Guides requirements gathering by focusing on system capabilities

## Examples

### Library Management System
- **Inside boundary**: Book lending, user registration, catalog management
- **Outside boundary**: Library members, book suppliers, payment systems

### E-commerce Website  
- **Inside boundary**: Product catalog, order processing, user accounts
- **Outside boundary**: Customers, suppliers, payment gateways, shipping companies

### Hospital System
- **Inside boundary**: Patient records, appointment scheduling, billing
- **Outside boundary**: Patients, doctors, insurance companies, lab systems

## Decision Factors

When deciding what belongs inside the system boundary, consider:

### Control and Responsibility
- Can the system directly control or modify this functionality?
- Is the system responsible for maintaining this information?
- Does the system own the business logic for this process?

### Business Requirements
- What capabilities must the system provide to meet business goals?
- Which processes are core to the system's purpose?
- What external services can be integrated versus built?

### Technical Constraints
- What can realistically be built within project constraints?
- What existing systems must be integrated with?
- What external services are available and reliable?

## Common Mistakes

- **Including [[Actor]]s inside the boundary** - Actors are always external
- **Making boundary too large** - Including everything makes the project unmanageable  
- **Making boundary too small** - Missing critical system functionality
- **Unclear boundaries** - Ambiguity about what the system does versus external systems
- **Moving boundaries frequently** - Changing scope without proper change management

## Relationship to Other Concepts

- **Defines scope** for [[Use Case]]s that will be developed
- **Identifies [[Actor]]s** that will interact with the system
- **Guides [[Stakeholder]]** identification and requirements gathering
- **Informs architecture** decisions about system interfaces and integration
- **Supports project planning** by clarifying what will be built versus integrated

## Evolution During Development

- **[[Inception]]**: Initial boundary definition based on high-level requirements
- **[[Elaboration]]**: Refined boundary as requirements and architecture become clearer
- **[[Construction]]**: Stable boundary guides implementation decisions
- **[[Transition]]**: Final validation that boundary meets business needs

The system boundary is a foundational decision that affects all aspects of system development, from requirements analysis to architecture design to implementation planning.
