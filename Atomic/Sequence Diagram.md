A **sequence diagram** is a type of [[Unified Modelling Language (UML)]] diagram that models the dynamic behavior of a system by showing how objects interact with each other over time. It captures the sequence of messages exchanged between objects to carry out a specific use case or process.

## Purpose

- Visualises the chronological order of interactions between objects.
- Helps understand how operations are carried out step-by-step.
- Clarifies the flow of control and data between system components.
- Useful for developers and analysts to design and verify system behavior.

## Key Components

| Component          | Description                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------|
| **Actors/Objects**  | Entities involved in the interaction, shown as lifelines at the top (e.g., `Student`, `Teacher`, or system objects). |
| **Lifelines**       | Vertical dashed lines representing the existence of an object over time.                    |
| **Time Axis**       | Vertical axis progressing downward, representing the passage of time.                       |
| **Messages**        | Horizontal arrows indicating communication between objects (method calls, returns, signals).|
| **Activation Boxes**| Narrow rectangles on lifelines showing when an object is active or executing a process.     |
| **Conditions**      | Optional guards or conditions that control message flow (e.g., `[condition]`).              |
| **Loops**           | Represent repeated interactions, often shown with a frame labeled `loop`.                   |

## How to Read a Sequence Diagram

- Objects or actors are arranged horizontally at the top.
- Time flows from top to bottom.
- Messages are shown as arrows from the sender’s lifeline to the receiver’s lifeline.
- Activation boxes highlight when an object is performing an action.
- Conditional and looping constructs indicate decision points and repeated behavior.

## Example: Dice Game Sequence Diagram

![[Sequence Diagram.png | center | 600]]

This diagram shows three objects at the top from left to right:

- `:DiceGame` (the main game controller)
- `d1:Die` (first die)
- `d2:Die` (second die)

### Sequence of Events

1. An actor (represented by a circle) calls the `play()` method on the `:DiceGame` object.
2. The `:DiceGame` object sends a `roll()` message to `d1:Die` to roll the first die.
3. It then calls `getFaceValue()` on `d1:Die` to retrieve the result, storing it in variable `x`.
4. Similarly, `:DiceGame` sends `roll()` and `getFaceValue()` messages to `d2:Die`, storing the result in `y`.
5. This sequence demonstrates how `DiceGame` coordinates the rolling and value retrieval of two dice by sending messages to each die object.