## Main Themes

- [[Models of Software Development]]
- [[Unified Process (UP)]]
- [[Object-Oriented Analysis and Design (OOAD)]]
- [[Unified Modelling Language (UML)]]


## Learning Objectives

- Explain the need for a software development process.
- Develop a use case for a given problem.
- Develop a domain model for a given problem and analyse it.


---

# Introduction

Software development involves much more than just coding.

**Additional steps include (but are not limited to):**
- Clearly defining what to develop.
- Knowing a programming language.
- Verifying that functionalities are implemented correctly.
- Splitting goals into manageable tasks.
- Considering constraints and possible points of failure.


---

# Stakeholders

A **stakeholder** is anyone who has an interest in your project (financial, educational, or otherwise).

---

# Common Causes of Failure in Software Development

- Poor project management.
- Poor cost estimation.
- Poor requirements specification.

---

# Development Tasks

- **What?** — requirements, constraints, use cases.
- **When?** — deadlines.
- **How?** — tools for development, communication, tracking.


---

# Example: Chat Program

|**Requirements**|**Constraints**|**Use Cases**|
|---|---|---|
|Send messages|Only works in Danish||
|Record audio|Limited resources||
|Save contacts|Maximum message size limit||

---

# Software Development Methods

## Waterfall

The **Waterfall model** was the first structured approach to software development.
- Activities occur in **linear, sequential phases**.
- Once you move forward, you cannot go back (like a real waterfall).


**Phases:**  
Requirements → Design → Implementation → Verification → Maintenance

**Pros:**
- Easy to understand.
- Easy to track (linear and sequential).
- Well documented (all requirements defined upfront).


**Cons:**
- Inflexible (requirements fixed at the start).
- Hard to adapt to changes in goals.
- Testing happens late in the process.


---

## Agile

Agile is an **umbrella term** for modern, flexible methodologies:
- Extreme Programming (XP)
- Feature-Driven Development (FDD)
- Unified Process (UP) ← _focus of the textbook_
- Scrum
- Kanban


**Key Idea:** Development is split into **iterations** (short, fixed-length mini-projects).

- Each iteration has its own requirements, design, implementation, and testing.
- Iterations evolve the product step by step.


**Pros:**
- Early feedback reduces risks.
- Flexible and adaptable.


**Cons:**
- Finding the right iteration length can be challenging (typically 2–6 weeks).


---

# Unified Process (UP)

UP is both **iterative** (repeats over time) and **incremental** (builds features step by step).

**Phases:**
1. Inception
2. Elaboration
3. Construction
4. Transition


![[UP Resources and Time Diagram.png]]

- **Construction** is the longest phase, where most programming happens.
- Activities like business modelling and requirements gathering are most intense in the early phases and taper off later.


### Executable Architecture Baseline
- A partial implementation of the system.
- Created during elaboration.
- Serves as the foundation for further development.


### Fundamental Principles of UP
- **Iterative & Incremental** — system grows with each iteration.
- **Use Case–Driven** — focus on end-user functionality.
- **Risk-Driven** — identify and address risks in every iteration.
- **Architecture-Centric** — focus on building, testing, and stabilising the core architecture.


### Advantages of Iterative Development
- Short, manageable steps.
- Visible progress early.
- Adaptable to changing requirements.
- Early feedback and user involvement.
- High-risk issues addressed first.


Phases are not repeated within one iteration.
- You can’t deploy before transition.
- You can’t construct before elaboration.


![[UP Phases.png]]

---

# Requirement Specification

## What is a Use Case?

A **use case** describes required functionality from the user’s perspective.

**Format:** _verb + noun_  
Examples:

- Play DiceGame
- Write book
- Watch movie
- Save file


**Example Use Case – Play DiceGame:**

1. Player throws dice.
2. System shows result.
3. If the sum is 6 → player wins, else loses.


---

# Object-Oriented Analysis and Design (OOA/D)

OOA/D is about **seeing the world in terms of concepts**.

- Example (classroom): benches, students, teacher.
- Example (hospital): beds, patients, doctors.
- Example (zoo): animals, zookeepers, cages.

## Classes and Objects

- **Class** → blueprint for objects.
- **Object** → instance of a class.

Example in Python:

```python
class Teacher:     
	def __init__(self, name):
		self.name = name  

Deena = Teacher("Deena")
```

## Analysis vs Design vs Modelling

- **Analysis** → identify objects in the problem domain.
- **Design** → define how these objects become software.
- **Modelling** → visualise the problem and solution.

**Example Domain Model:**  
![[Domain Model.png]]

- Boxes = classes.
- Arrows = relations.
- Numbers on arrows = how many objects are involved.

---

# Unified Modelling Language (UML)

UML is a **visual language** for specifying, constructing, and documenting systems.

Two main groups of diagrams:

1. **Structure diagrams** - technical structure of the system.
2. **Behaviour diagrams** - system behaviour.

## Common UML Diagrams

- **Sequence / Interaction Diagram** → flow of messages between objects.  
![[Sequence Diagram.png]]

- **Class Diagram** → shows class structure and relations, can be translated directly into code.  
![[Class Diagram.png]]

- **Domain Model** → visualises real-world concepts, less code-oriented.  
![[Domain Model.png]]
    

---

# Disclaimer

- UML diagrams are for **understanding and communication**, not just documentation.
- Don’t overcomplicate: simple diagrams are best.
- More diagrams ≠ clearer understanding.