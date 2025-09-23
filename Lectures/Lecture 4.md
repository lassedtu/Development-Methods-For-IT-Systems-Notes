## Glossary

A glossary documents all the important terms used in your project

It ensures every stakeholder and team member understands and agrees on the meaning of terms

This helps avoid confusion and miscommunication during the project

The glossary can include definitions of technical terms business jargon acronyms and any other relevant vocabulary

Keeping the glossary up to date is important as new terms may arise during the project

A clear glossary supports better collaboration and shared understanding across diverse teams
### Glossary Example

| Term           | Definition                                                                 |
| -------------- | -------------------------------------------------------------------------- |
| User           | A person who interacts with the system to achieve a goal                   |
| Stakeholder    | Anyone with an interest in the project including users managers and sponsors |
| Use Case       | A description of a specific way the system is used to achieve a goal      |
| Iteration      | A short development cycle where a set of tasks are completed               |
| Bug            | An error or defect in the software that causes it to behave unexpectedly   |
| Net Sale       | The total sales price of an order before discounts allowances shipping and other charges |

This example shows how terms are clearly defined to ensure everyone understands their meaning in the project context

---
## Supplementary Specification

A supplementary specification is a document that contains textual descriptions of all other requirements not covered in the main functional requirements

It includes non-functional requirements such as usability reliability performance supportability and other quality attributes often summarised by the acronym URPS+

It also covers additional requirements like reports documentation packaging installation and maintenance needs

The supplementary specification complements the main requirements by capturing details that affect how the system operates but are not directly related to specific functions

### Example  
See page 104 of the textbook for a detailed example of a supplementary specification document

Maintaining a supplementary specification helps ensure all aspects of the system are considered and documented clearly

---
## Business Rules

Business rules are statements that provide the criteria and conditions for making decisions. They define how things should be done or interpreted within the business context.

These rules capture policies, constraints, calculations, and definitions that govern the business. They help ensure consistency and correctness in business processes and decisions.

Business rules focus on the business logic and are independent of software implementation. Although they are not part of the software requirements, they influence how the software should behave.

Understanding business rules is important for designing systems that align with business needs. They can range from simple definitions to complex conditions involving multiple factors.

Typically, business rules come from domain experts, business analysts, or regulatory requirements.

### Example  
"Net sale is defined as the total sales price of an order before discounts, allowances, shipping, and other charges."

Other examples of business rules include:  
- Customers must be at least 18 years old to register.  
- Orders over 1000 dollars require manager approval.  
- Returns are accepted within 30 days of purchase.

Documenting business rules separately helps clarify what the business expects without mixing them with technical details. This separation supports better communication between business stakeholders and development teams.

---
# Risk Management

## Risks

Risk means the probability of an adverse circumstance or event that could negatively affect the project product or business

Risks represent uncertainties that may cause problems or delays if they occur

Understanding and managing risks is essential to increase the chances of project success

There are three main types of risks to consider

- **Project risks**  
  These are risks related to the management and execution of the project itself  
  Examples include staff turnover management change hardware unavailability requirements change and specification delays

- **Product risks**  
  These risks concern the quality and performance of the product being developed  
  Examples include requirements change specification delays size underestimate and software tool underperformance

- **Business risks**  
  These risks affect the broader business environment or market  
  Examples include technology change and product competition

![[Risk Types.png | center | 700]]

### Project Risks

Project risks are risks related to the management and execution of the project itself

They affect how well the project is planned organised and controlled

#### Examples

- **Staff turnover**  
  Experienced staff will leave the project before it is finished causing loss of knowledge and delays

- **Management change**  
  Changes in company management bring different priorities that may affect project direction or funding

- **Hardware unavailability**  
  Essential hardware needed for the project will not be delivered on schedule causing delays

- **Requirements change**  
  A larger number of changes to the requirements than anticipated disrupt planning and development

- **Specification delays**  
  Specifications and essential interfaces are not available on time slowing progress

Managing project risks involves careful planning realistic scheduling clear communication and monitoring progress regularly
### Product Risks

Product risks concern the quality performance and functionality of the product being developed

They affect whether the product meets requirements and satisfies users

#### Examples

- **Requirements change**  
  Frequent or late changes to requirements cause rework and uncertainty

- **Specification delays**  
  Delays in receiving detailed specifications hinder development and testing

- **Size underestimate**  
  The size or complexity of the system is underestimated leading to insufficient resources or time

- **Software tool underperformance**  
  Software tools that support the product do not perform as anticipated reducing productivity or quality

Reducing product risks requires thorough requirements analysis careful design testing and user feedback
### Business Risks

Business risks affect the broader business environment market or organisation

They influence the viability and success of the project beyond technical or project concerns

#### Examples

- **Technology change**  
  The underlying technology on which the system is built is superseded by new technology making the product obsolete or requiring redesign

- **Product competition**  
  A competitive product is marketed before the system is completed reducing market share or demand

Managing business risks involves market research monitoring external factors and aligning the project with business strategy

## Risk Identification

Risk identification is the process of finding and describing risks that could affect the project product or business

It is the first step in risk management and critical for preparing effective responses

Identifying risks early helps the team anticipate problems and plan accordingly

### How to identify risks

- **Brainstorming**  
    Gather the team and stakeholders to discuss possible risks based on experience and knowledge

- **Checklists**  
    Use lists of common risks from previous projects or industry standards as prompts

- **Interviews**  
    Talk to experts and key stakeholders to uncover risks they foresee

- **Analysis of project documents**  
    Review requirements plans designs and contracts for unclear or challenging areas

- **SWOT analysis**  
    Examine strengths weaknesses opportunities and threats related to the project

- **Risk workshops**  
    Facilitate structured sessions focused on risk discovery and assessment

### Documenting identified risks

Each identified risk should be described clearly including

- The risk event or condition
- The area it affects (project product business) 
- Possible causes
- Potential impact if it occurs

### Example

- Risk: Key developer may leave the project
- Affects: Project
- Cause: High workload and competing job offers
- Impact: Loss of knowledge delays in development

Regularly revisiting risk identification throughout the project lifecycle is important as new risks can emerge and existing ones may change

---
## Assignment: Identify risks of chat application

### Project Risks
- Requirements change  
  Maybe it is discovered late that new features are needed to stand out.
- Staff turnover  
  Key developers or team members may leave during the project causing delays and loss of knowledge.
### Product Risks
- Size underestimate  
  Security measures such as end-to-end encryption are a necessity when dealing with chat applications that need to be secure not having a plan for implementing advanced security measures.
- Software tool underperformance  
  A chat application can be very hard to scale if a lot of users suddenly come in at once.
- Integration challenges
  Difficulties integrating with other platforms or services like contacts or media sharing can cause delays or reduce functionality.
### Business Risks
- Product competition  
  Chat applications are mostly a closed system. It would be extremely hard for a new competitor to enter and they would have to offer something no one else offers.
- Market demand shift  
  User preferences may change towards new communication methods or platforms reducing demand for the chat app

## Assignment 2: Perform a risk analysis

| Risk                           | Probability (1-5) | Impact (1-5) | Description                                                                                   | Notes on Mitigation                                 |
| ------------------------------ | ----------------- | ------------ | --------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| **Project Risks**              |                   |              |                                                                                               |                                                     |
| Requirements change            | 4                 | 5            | Late discovery of new features needed to stand out can disrupt planning and increase workload | Use clear initial requirements and frequent reviews |
| Staff turnover                 | 3                 | 4            | Key developers leaving causes delays and loss of knowledge                                    | Cross-training and documentation to reduce impact   |
| **Product Risks**              |                   |              |                                                                                               |                                                     |
| Size underestimate             | 4                 | 5            | Underestimating complexity of security measures like end-to-end encryption                    | Early prototyping and security planning             |
| Software tool underperformance | 3                 | 4            | Scaling issues if many users join simultaneously                                              | Load testing and scalable architecture design       |
| Integration challenges         | 3                 | 4            | Difficulties integrating with contacts or media sharing platforms                             | Early integration testing and modular design        |
| **Business Risks**             |                   |              |                                                                                               |                                                     |
| Product competition            | 2                 | 4            | Hard for new competitors to enter but must offer unique features                              | Market research and innovation focus                |
| Market demand shift            | 3                 | 4            | Changes in user preferences reducing demand                                                   | Monitor trends and adapt product roadmap            |

This table lists the risks with the highest risk ratings calculated by multiplying probability and impact

| Risk                           | Risk Rating (Probability $\cdot$ Impact) |
| ------------------------------ | ---------------------------------------- |
| Requirements change            | 20 (Catastrophic)                        |
| Size underestimate             | 20 (Catastrophic)                        |
| Staff turnover                 | 12 (Action)                              |
| Software tool underperformance | 12 (Action)                              |
| Integration challenges         | 12 (Action)                              |
| Market demand shift            | 12 (Action)                              |
| Product competition            | 8 (Action)                               |

Focusing on these high risk rating items helps prioritise mitigation efforts where they matter most

---

## Risk Strategies and Planning

Managing risks effectively requires choosing appropriate strategies to handle each identified risk. Common risk strategies include:

- **Transfer**  
  Pass on responsibility for the risk to a third party (e.g., insurance, outsourcing).

- **Accept**  
  Take the chance and accept the risk without specific action, often when the risk impact is low.

- **Mitigate**  
  Take actions to minimize the consequences or likelihood of the risk.

- **Eliminate**  
  Remove the risk entirely by changing the project plan or approach.

---

## Risk Planning Categories

Risk planning involves developing approaches to deal with risks before they occur:

- **Avoidance strategies**  
  Ways to avoid risks altogether by changing plans or requirements.

- **Minimisation strategies**  
  Ways to reduce the possible damage or likelihood of risks.

- **Contingency plans**  
  Preparing for the worst-case scenarios with backup plans if risks materialise.

## Risk Monitoring

Risk monitoring is the continuous process of checking that assumptions about risks remain valid throughout the project lifecycle. It involves:

- Regularly reviewing risks at all project stages.

- Asking key questions such as:  
  - Is the risk becoming more or less probable?  
  - Have the effects of the risk changed?

- Watching for potential indicators of risk types:

| Risk Type      | Potential Indicators                                                                 |
| -------------- | ------------------------------------------------------------------------------------ |
| Estimation     | Failure to meet schedule; unresolved defects                                        |
| Organizational | Gossip; lack of senior management action                                            |
| People         | Poor morale; team conflicts; high turnover                                          |
| Requirements   | Many change requests; customer complaints                                           |
| Technology     | Late hardware/software delivery; frequent tech problems                             |
| Tools          | Reluctance to use tools; complaints about software or hardware                      |

---
# Elaboration

The elaboration phase is the second stage of a project, typically following inception. It usually lasts several weeks and focuses on refining the project’s vision, architecture, and requirements to reduce risks and prepare for detailed design and implementation. Each iteration during this phase typically takes between 2 and 6 weeks.

## Key Goals

- Develop a deeper understanding of the system requirements and architecture.
- Address major technical risks and uncertainties.
- Establish a stable foundation for design and development.
- Expand and clarify functional and non-functional requirements.

## Typical Activities

- Elaborate and prioritise detailed requirements (covering about 60–80% of [[functional requirements]]).
- Create and validate architectural prototypes or models.
- Refine use cases and domain models.
- Identify and mitigate technical risks.
- Plan iterations and releases based on refined scope and risks.

## Outcomes

- A well-defined and stable architecture baseline.
- Detailed and validated requirements ready for design.
- Reduced project risks through early technical validation.
- Clear iteration plans aligned with project goals.

## Artifacts of the Elaboration phase

Artifacts created during elaboration provide detailed guidance for the development team and stakeholders. They help ensure everyone understands the system’s structure and requirements before full-scale development begins.

### Examples of Artifacts
- [[Detailed Requirements]]
- [[Architecture Model]]
- [[Use-case Model]]
- [[Domain Model]]
- [[Risk Planning]]
- [[Iteration Plan]]
- [[Prototypes or Proofs of Concept]]

You should focus on elaborating the most critical and risky parts of the system during this phase to ensure a solid foundation for subsequent development.