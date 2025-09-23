FURPS+ is a model used to help organise and classify different types of requirements for a system or project. It covers both what the system should do and how well it should do it.
Each letter correlates to a different category of requirements that should be considered when designing a system

| Letter | Category       | Description                                              |
| ------ | -------------- | -------------------------------------------------------- |
| F      | Functional     | What the system does (features, actions)                 |
| U      | Usability      | How easy and pleasant it is to use                       |
| R      | Reliability    | How dependable and consistent it is                      |
| P      | Performance    | How fast and efficient it is                             |
| S      | Supportability | How easy it is to maintain and support                   |
| +      | Plus           | Other requirements (constraints, interfaces, legal, etc) |

## F - Functional Requirements

These are the features and functions the system must perform. They describe what the system should do, such as processing data, authenticating users, generating reports, or sending notifications. Functional requirements are usually written as “the system shall…” statements.

## U - Usability

Usability requirements focus on how easy and pleasant the system is to use. This includes the user interface design, accessibility, documentation, help features, and overall user experience. Usability answers questions like: Is the system intuitive? Can users learn it quickly? Is it accessible to people with disabilities?

Examples:

- The system must provide online help.
- The interface should be easy to navigate for new users.

## R - Reliability

Reliability requirements specify how dependable the system must be. This includes availability (uptime), accuracy, error rates, recoverability, and how the system handles failures. Reliability is about making sure the system works correctly and consistently.

Examples:

- The system must be available 99.9% of the time.
- The system must recover from crashes within 2 minutes.

## P - Performance

Performance requirements describe how fast and efficiently the system should operate. This includes response times, throughput, resource usage, and scalability. Performance ensures the system can handle the expected workload.

Examples:

- The system must respond to user actions within 2 seconds.
- The system must support 1000 concurrent users.

## S - Supportability

Supportability (sometimes called Serviceability) requirements cover how easy it is to maintain, update, and support the system. This includes requirements for diagnostics, logging, configuration, monitoring, and documentation for support staff.

Examples:

- The system must log all errors for troubleshooting.
- The system should allow configuration changes without downtime.

## + (Plus)

The “+” in FURPS+ stands for additional categories that don’t fit neatly into the first five. These can include:

- **Design constraints:** Specific technologies, platforms, or standards that must be used.
- **Implementation requirements:** Programming languages, tools, or methods.
- **Interface requirements:** How the system interacts with other systems.
- **Physical requirements:** Hardware, devices, or environmental needs.
- **Legal and regulatory requirements:** Compliance with laws or industry standards.