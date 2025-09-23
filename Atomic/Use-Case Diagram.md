A use-case diagram is a type of [[Unified Modelling Language (UML)]] diagram that visually represents the interactions between users ([[Actor]]s) and a system. It shows the system’s main functions ([[use case]]s) and who uses them.

## Purpose

- Visualises the functional requirements of a system.
- Clarifies how different actors interact with the system.
- Helps identify system boundaries and main user goals.
- Useful for communication between stakeholders, developers, and testers.

## Key Elements

- **[[Actors]]:**  
  Shown as stick figures outside the system boundary. Actors can be people, organisations, or external systems that interact with your system.
- **[[Use Case]]s:**  
  Shown as ovals inside the system boundary. Each use-case represents a specific function or goal the system provides.
- **[[System Boundary]]:**  
  Drawn as a rectangle that contains all the use-cases. The system’s name is usually written at the top.

## Stereotypes

- [[Stereotypes]] clarify the type of actor (human, system, organisation).
- Written as `<<Stereotype>>` above the actor’s name.
    - Example: `<<human>>` Customer, `<<system>>` Payment Gateway, `<<organization>>` School

## Placement of Actors

- **[[Primary actor]]s** are placed on the left side of the system boundary.
- **[[Secondary actor]]s** are placed on the right side.
- **[[Offstage actors]]** are often placed at the bottom or away from the main actors (sometimes with a dashed line to show indirect involvement).

## Connections

- Solid lines connect actors to the use-cases they interact with.
- Actors are always outside the system boundary while use-cases are inside.

## Example Diagrams

![[Use Case Diagram.png]]
![[Use Case Diagram 2.png]]
![[Use Case Diagram 3.png]]