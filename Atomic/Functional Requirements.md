Functional requirements specify what the system must do - the specific behaviours, functions, and features that the system must provide to meet user needs

They describe the system's functionality from the user's perspective and define the services the system should provide

Functional requirements are typically the most visible and understood type of requirements because they directly relate to user goals and system capabilities

## Characteristics

- Describe **what** the system should do, not **how** it should do it
- Focus on system behavior and functionality
- Are usually testable and measurable
- Often written as "the system shall..." statements
- Form the basis for [[Use Case]]s and user stories

## Examples

- The system shall allow users to create an account
- The system shall authenticate users before granting access
- The system shall generate monthly sales reports
- The system shall process credit card payments
- The system shall send email notifications for password resets
- The system shall allow users to search for products by category

## Relationship to FURPS+

Functional requirements correspond to the "F" in [[FURPS+]], which categorizes different types of requirements

While functional requirements describe what the system does, [[Non-Functional Requirements]] describe how well it should do it

## Sources of Functional Requirements

- [[Stakeholder]] interviews and workshops
- [[Use Case]]s and user stories
- [[Business Rules]] and policies
- Existing system analysis
- User observation and task analysis
- Regulatory and compliance needs

## Documentation Formats

Functional requirements can be documented in several ways:

- **Formal requirement statements** - "The system shall..."
- **[[Use Case]]s** - Detailed interaction scenarios
- **User stories** - "As a [user], I want [goal] so that [benefit]"
- **Feature lists** - High-level capability descriptions

## Traceability

Each functional requirement should be:
- **Traceable to** [[Stakeholder]] needs and [[Business Case]]
- **Traceable from** [[Use Case]]s, design elements, and test cases
- **Linked to** [[Non-Functional Requirements]] that affect its implementation

## During Development Phases

- **[[Inception]]**: Capture 10-20% of functional requirements for feasibility
- **[[Elaboration]]**: Detail 60-80% of functional requirements for architecture
- **[[Construction]]**: Complete remaining functional requirements through implementation
- **[[Transition]]**: Validate functional requirements meet user needs

## Quality Criteria

Good functional requirements are:
- **Complete** - Cover all necessary functionality
- **Consistent** - Don't contradict each other
- **Unambiguous** - Have only one interpretation
- **Verifiable** - Can be tested or validated
- **Traceable** - Linked to business needs and design

## Common Mistakes

- Mixing functional and [[Non-Functional Requirements]]
- Specifying implementation details rather than required functionality
- Using vague or ambiguous language
- Missing error handling and exception scenarios
- Not considering all user types and scenarios
