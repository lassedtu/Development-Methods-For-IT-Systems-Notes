## Inception
The inception phase is a very short 1-2 week phase where you start your project.
During this phase we're going to decide if we can go ahead with the project or if it's not worth it.
You try to establish a common vision and scope for the product.

---
## Artifacts of the Inception phase
Artifacts are the important documents and notes created during the inception phase. They show what the project is about, who is involved, and what needs to be done. These help everyone understand and agree on the project before it really starts.

### Examples of Artifacts
- [[Vision Statement]]
- [[Business Case]]
- [[Stakeholder List]]
- [[Initial requirements]]
- [[Risk assessment]]
- [[Project plan]]
- [[Use-case model]]
- [[Domain model]]
- [[Glossary]]
- [[Iteration Plan]]

You don’t have to create every artifact listed. You should choose the ones that make sense for your project. For the inception phase, you only need to write about 10-20% of the functional requirements, just enough to get started and show the main ideas.

---
## What does vision look like?

- Who does the product benefit?
- What problem does it solve?
- What is the ultimate goal or purpose of the project?

Vision in the inception phase is about defining and agreeing on the big-picture purpose and intended impact of the product before moving forward with detailed planning or development.

A vision statement is a short description that explains what the project aims to achieve and why it exists. It describes the main goal of the product, who it is for, and what problem it will solve. The vision statement helps everyone understand the big-picture purpose and direction of the project before any further work begins.

---
## Iteration Plan

An iteration plan is a short document that lists what the team will work on during the next development cycle (called an iteration). It includes the tasks to be done, who will do them, and the goals for that period. The plan helps the team stay organised and focused on what needs to be completed in each step of the project.

---

## Stakeholder

A stakeholder is anyone who has an interest in the system or project. This includes anyone who is impacted by the project, can help make decisions about it, or takes part in building or using it. Stakeholders can provide requirements, feedback, and support, and their needs should be taken into consideration throughout the project.

### Examples of stakeholders

- Funding partners
- Private organisations
- Schools, universities
- General population
- End users
- Project managers
- Government agencies

---
## Actor

Actors are people or external systems that interact with the system, but are not part of the system. They either use the system to achieve a goal or are used by the system to perform certain tasks.

### The three types of actors

- **Primary Actor:**  
    The main user or system that initiates interactions to achieve a goal (like a customer placing an order).  

- **Secondary Actor:**  
    Supports the system or helps the primary actor, often providing a service or information (like a payment gateway, a database).  

- **Offstage Actor (Tertiary Actor):**  
    Does not interact directly with the system but is affected by its outcome or has an interest in it (like a manager who receives reports, a government agency monitoring compliance).  


---

## Use-Case Diagrams

Use-case diagrams are a type of UML diagram used to show how different users (actors) interact with a system. They help visualise the system’s main functions and who uses them.

### Key Elements

- **Actors:**  
    Shown as stick figures outside the system boundary. Actors can be people, organisations, or external systems that interact with your system.

- **Use Cases:**  
    Shown as ovals inside the system boundary. Each use case represents a specific function or goal the system provides.

- **System Boundary:**  
    Drawn as a rectangle that contains all the use cases. The system’s name is usually written at the top.


### Stereotypes

- Stereotypes help clarify the type of actor (human, system, organisation).
- Written as `<<Stereotype>>` above the actor’s name.
- Example:
    - `<<human>>` Customer
    - `<<system>>` Payment Gateway
    - `<<organization>>` School

### Placement of Actors

- **Primary actors** are placed on the left side of the system boundary.
- **Secondary actors** are placed on the right side.
- **Offstage (tertiary) actors** are often placed at the bottom or away from the main actors (sometimes with a dashed line to show indirect involvement).

### Connections

- Solid lines connect actors to the use cases they interact with.
- Actors are always outside the system boundary while use cases are inside

---

## FURPS+
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

### F - Functional Requirements

These are the features and functions the system must perform. They describe what the system should do, such as processing data, authenticating users, generating reports, or sending notifications. Functional requirements are usually written as “the system shall…” statements.

### U - Usability

Usability requirements focus on how easy and pleasant the system is to use. This includes the user interface design, accessibility, documentation, help features, and overall user experience. Usability answers questions like: Is the system intuitive? Can users learn it quickly? Is it accessible to people with disabilities?

Examples:

- The system must provide online help.
- The interface should be easy to navigate for new users.

### R - Reliability

Reliability requirements specify how dependable the system must be. This includes availability (uptime), accuracy, error rates, recoverability, and how the system handles failures. Reliability is about making sure the system works correctly and consistently.

Examples:

- The system must be available 99.9% of the time.
- The system must recover from crashes within 2 minutes.

### P - Performance

Performance requirements describe how fast and efficiently the system should operate. This includes response times, throughput, resource usage, and scalability. Performance ensures the system can handle the expected workload.

Examples:

- The system must respond to user actions within 2 seconds.
- The system must support 1000 concurrent users.

### S - Supportability

Supportability (sometimes called Serviceability) requirements cover how easy it is to maintain, update, and support the system. This includes requirements for diagnostics, logging, configuration, monitoring, and documentation for support staff.

Examples:

- The system must log all errors for troubleshooting.
- The system should allow configuration changes without downtime.

### + (Plus)

The “+” in FURPS+ stands for additional categories that don’t fit neatly into the first five. These can include:

- **Design constraints:** Specific technologies, platforms, or standards that must be used.
- **Implementation requirements:** Programming languages, tools, or methods.
- **Interface requirements:** How the system interacts with other systems.
- **Physical requirements:** Hardware, devices, or environmental needs.
- **Legal and regulatory requirements:** Compliance with laws or industry standards.

---

# MoSCoW

The MoSCoW model is a simple way to prioritise requirements or features in a project. It helps teams decide what is most important to deliver first, and what can wait until later. Each letter in MoSCoW stands for a different level of priority.

### The four categories of MoSCoW

- **Must have**
    These are the requirements that are absolutely essential for the system or project to work. If any "Must have" is missing, the project will fail or not be usable.  
    **Example**: The system must allow users to log in securely.

- **Should have**
    These requirements are important, but not critical. The system can still function without them, but they add significant value and should be included if possible.  
    **Example**: The system should allow users to reset their password via email.

- **Could have**
    These are nice-to-have features. They are not essential and can be left out if there is not enough time or resources. They are often enhancements that improve user experience.  
    **Example**: The system could allow users to customise their dashboard.

- **Won’t have (this time)**
    These are requirements that have been agreed will not be included in this release or iteration. They may be considered for the future, but are not a priority now.  
    **Example**: The system won’t have integration with third-party analytics tools in the first release.

---

# Use Cases and User Stories

|         | Use Case                                 | User Story                                     |
| ------- | ---------------------------------------- | ---------------------------------------------- |
| Format  | Step-by-step scenario                    | Short sentence (“As a user, I want… so that…”) |
| Focus   | How the system and user interact         | What the user wants and why                    |
| Detail  | Detailed, includes all steps and options | Brief, high-level                              |
| Example | Borrow Book (with steps)                 | As a member, I want to borrow a book…          |

---

# Guidelines for finding use cases

### 1. Define the system boundary

Defining the system boundary means deciding what is inside the system you are building, and what is outside of it. The system boundary separates the parts of the world that your system will control from everything else.

- The system boundary is usually shown as a rectangle in a use-case diagram. Everything inside the rectangle is part of the system. Everything outside is not.
- Actors (users, other systems, organisations) are always outside the system boundary. They interact with the system but are not part of it.
- Use cases (the main functions or goals the system provides) are always inside the system boundary.

### 2. Identify the primary actors and their goals

Primary actors are the main users or systems that interact with your system to achieve a specific goal. The system exists to fulfill these goals.

- A primary actor is usually the person or external system that starts an interaction because they want something from the system.
- Each primary actor has a goal—something they want to accomplish by using the system.
- The system should provide use cases that help the primary actor achieve their goal.

### 3. Define use cases that satisfy user’s goals

Once you know who the primary actors are and what their goals are, you need to define use cases that help them achieve those goals.

- Each use case should describe a specific way the system helps a primary actor reach their goal.
- Name each use case according to the goal it fulfills. This makes it clear what the use case is about and who benefits from it.
- Use case names are usually short and action-oriented, like “Borrow Book”, “Place Order”, or “Submit Assignment”.

## Formats for Finding Use-Cases

- Brief - one paragraph
- Casual - Multiple paragraphs
- Fully dressed - All steps in detail. Example: page 68 - 72 of the textbook

## Use-Case Description

- **Name:**  
    Actor’s goal such as Borrow Book

- **ID:**  
    Unique identifier, such as UC-01

- **Participating Actors:**
    - **Primary:** Who starts the use case?
    - **Secondary:** Who else is involved or supports the process?

- **Pre-conditions:**  
    What must be true before this use case can start?

- **Flow of Events:**
    1. Step 1: What does the primary actor do? What does the system do in response?
    2. Step 2: Next action or system response
    3. Continue steps as needed

- **Post-conditions:**  
    What is true after the use case finishes?

- **Alternative Flows:**
    - Describe any exceptions, errors or special cases and how they are handled

## Linking Use-Cases to Requirements

Every use case in your system should be directly linked to one or more requirements. This connection ensures that each use case is justified and traceable back to what the system must do. Typically, use cases help identify and clarify **functional requirements** (what the system should do), but they can also highlight non-functional requirements (such as usability, reliability, or performance).

- Each use case describes a scenario that fulfills a user or stakeholder goal.
- The steps and outcomes in a use case map to specific requirements in your requirements list or specification.
- This linkage helps ensure that all requirements are covered by the system’s functionality, and that nothing important is missed.
- When requirements change, you can quickly see which use cases are affected, making updates easier and more organised.

When documenting use cases it can be very helpful to reference the related requirement IDs (like FR-01, NFR-03) in the use-case description. This makes it easy to trace requirements throughout the project lifecycle.

# Examples of Use-Case Diagrams

![[Use Case Diagram.png]]

![[Use Case Diagram 2.png]]

![[Use Case Diagram 3.png]]

