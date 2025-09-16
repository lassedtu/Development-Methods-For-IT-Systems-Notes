A use-case describes a specific way a user (or another system) interacts with a system to achieve a goal. Use-cases capture the functional requirements of a system by outlining the steps involved in each interaction.

## Purpose

- Clarifies how the system should behave from the user's perspective.
- Helps identify and document functional requirements.
- Serves as a foundation for system design, testing, and user documentation.

## Structure

A typical use-case includes:
- **Name:** The goal or function (e.g., "Borrow Book").
- **ID:** Unique identifier (e.g., UC-01).
- **Participating Actors:** Who is involved (primary and secondary).
- **Pre-conditions:** What must be true before the use-case starts.
- **Flow of Events:** Step-by-step scenario of interactions.
- **Post-conditions:** What is true after the use-case finishes.
- **Alternative Flows:** Exceptions, errors, or special cases.

## Formats

- **Brief:** One paragraph summary.
- **Casual:** Multiple paragraphs with main flow and alternatives.
- **Fully Dressed:** All steps and details, including pre/post-conditions and exceptions.

## Use-Case Diagrams

Use-case diagrams are a type of UML diagram that visually represent use-cases, actors, and their interactions with the system. See [[Use-Case Diagram]] for more details.

## Use-Cases vs User Stories

|         | Use-Case                                 | User Story                                     |
| ------- | ---------------------------------------- | ---------------------------------------------- |
| Format  | Step-by-step scenario                    | Short sentence (“As a user, I want… so that…”) |
| Focus   | How the system and user interact         | What the user wants and why                    |
| Detail  | Detailed, includes all steps and options | Brief, high-level                              |
| Example | Borrow Book (with steps)                 | As a member, I want to borrow a book…          |

## Guidelines for Finding Use-Cases

1. **Define the system boundary:** What is inside/outside the system.
2. **Identify primary actors and their goals:** Who uses the system and what do they want to achieve.
3. **Define use-cases that satisfy user goals:** Each use-case should help a primary actor achieve a goal.

## Linking Use-Cases to Requirements

- Each use-case should be traceable to one or more requirements.
- Helps ensure all requirements are covered and changes are manageable.