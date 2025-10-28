# Class Diagrams and GRASP

Class diagrams are used for structure and static modeling of a system. They provide a visual representation of the static structure showing the layout of components but not the activities or behaviors inside them. The instance of a class leads to objects in the system.

## Analysis vs Design Class Diagrams

### Domain Model (Analysis)

Domain models focus on the conceptual perspective. They show class names and possibly attributes but typically do not include operations or methods. The goal is to understand the high-level domain without delving into implementation specifics.

### Design Model

Design models include class names attributes and operations. They provide the software model that prepares for actual coding and system development. A design model can contain 10 to 100 times more classes than the analysis model because it includes:

- Classes that do not exist in the domain
- Classes for design patterns
- Controllers and adapters

## Perspectives of Class Diagrams

The perspective chosen is influenced by the development stage:

### Conceptual Perspective

Used during domain model development. Focus mainly on understanding high-level concepts and relationships without specifics.

### Specification Perspective

Used during analysis and early design. Begin to outline specifics and detailed functionalities. Understand what the system should do and lay groundwork for design.

### Implementation Perspective

Used during design model development. Focus on concrete details including classes methods and data structures. Prepares for actual coding and system development.

## UML Class Notation

### Basic Class Structure

A class in UML consists of three compartments:

1. **Class name** at the top
2. **Attributes** in the middle
3. **Operations/Methods** at the bottom

### Visibility

UML uses symbols to represent visibility:

- `+` Public (Java: `public`)
- `#` Protected (Java: `protected`)
- `-` Private (Java: `private`)

### Attributes

Attributes follow this syntax:

```
visibility name : type multiplicity = default {property string}
```

Examples:

- `- passengerList : String [0..*] = checkedInList {ordered}`
- `- age : int`
- `+ GRAVITY : double = 9.81 {readOnly}`

### Derived Attributes

The symbol `/` indicates a derived attribute which can be derived from other attributes in the model and does not need to be stored explicitly.

### Class Variables vs Object Variables

- **UML:** Underlined attributes represent class variables
- **Java:** Uses the `static` keyword

### When to Show Attributes

Include attributes that the requirements (such as use cases) suggest or imply a need to remember information. For example a receipt in the Process Sale use case normally includes a date and time store name and address and cashier ID.

## UML Associations

Associations represent relationships between classes. They specify a form of communication between classes typically by sending messages or method calls. An association represents a reference to an object.

### Multiplicity

Multiplicity defines how many instances of one class can be associated with instances of another class:

- `1` exactly one
- `0..1` zero or one
- `*` or `0..*` zero or more
- `1..*` one or more
- `n..m` between n and m

### Attributes vs Associations

Attributes and associations are basically the same but visually different. As a rule of thumb:

- Use **attributes** for simple types
- Use **associations** for classes (or attributes can also work)

### Reflexive Association

A concept may have an association to itself. This is known as a reflexive association. For example a Briefcase with Subfolder which itself contains a subfolder.

### Dependency

Dependency is a "light association" that represents a temporary reference. A change in one class affects another class but the relationship is weaker than a full association.

## Types of Relationships

### Aggregation

Aggregation models a "whole-part" relationship where parts exist independently of the whole. For example printers and computers. A LabClass can have students or a StudyProgram can have Courses.

### Composition

Composition is a stronger form of aggregation where parts do not exist outside of the whole. It represents strong coupling. The child object belongs to zero or one parent object. For example a brick house and its bricks.

In Java it is rarely necessary to distinguish between aggregation and composition. In C++ composition can be achieved by declaring objects directly within classes rather than using pointers or references:

```cpp
class Engine { /*...*/ };
class Car {
    Engine myEngine;
};
```

### Generalization (Inheritance)

Properties from a superclass are inherited to subclasses. Subclasses can add their own specialization. Abstract classes cannot be instantiated.

### Interface

An interface is a contract on functionality. It is in the family with abstract classes. Classes implement the interface and use it to define expected behavior.

## Class Diagrams in Sequence Diagrams

Classes from class diagrams can appear in sequence diagrams to show interactions between objects over time. The sequence diagram shows the dynamic behavior while the class diagram shows the static structure.

## Architecture and Key Principles

### Separation of Concerns

Separation of concerns is a frequently occurring design principle. It involves the division of a system into separate areas to achieve modularity in the code.

**Examples:**

- The internet protocol stack
- UI-related design and frontend/backend separation
- Service-Oriented Architecture
- Layered applications

**Why modularity?**

- Division of development
- Readability
- Easier fault isolation
- Easier tests
- Recycling of components
- Easier replacement of parts

### Layered Architecture

A layered architecture organizes the logical structure of a system into layers. It is often drawn using UML package diagram notation. A UML package can group anything: classes other packages use cases and more.

**The essential idea of using layers:**

- Organizing logical structure
- Defining collaboration and coupling direction

**What problems does using layers address?**

- Source code change management
- Application logic reusability
- Business logic reusability
- Coupling and cohesion

### Model View Separation Principle

The Model View Separation Principle divides a system into:

- **Model:** Manages data and business logic
- **View:** Handles presentation and user interface

This separation ensures that the view does not directly manipulate the model and the model does not depend on the view.

### Model View Controller (MVC)

Objects are allocated a role (model view or controller) with a well-defined responsibility. MVC achieves low coupling and high cohesion and creates a design that is:

- Easy to understand
- Easy to test
- Easy to maintain

### MVC and Robustness Diagram (BCE Diagram)

The robustness diagram is also known as the BCE Model. It is a variant of the class diagram not included in the UML specification. It was introduced to help bridge the gap between high-level analysis models (use case diagrams) and detailed design models (class diagrams and sequence diagrams).

**BCE Components:**

- **Boundary (MVC View):** Represents any external interface. It can be broader than just a UI. In a web application the boundary could be HTML pages or RESTful API endpoints through which users or other systems interact with the application.
- **Controller (MVC Controller):** Handles user requests and coordinates actions. For example in a shopping cart application when a user decides to check out the controller would handle this request calculate the total cost and decide what to display next.
- **Entity (MVC Model):** Represents data and business logic. For example in a blog application an entity might represent a blog post storing the title content and author and providing methods to save or retrieve a post from a database.

BCE diagrams are very easy to draw and are usually done on a whiteboard.

## Good Class Design Principles

A well-designed class should be:

- **Complete and sufficient:** Meets the client's expectations of functionality with no more and no less than needed
- **Simple:** Methods are simple and the class does not contain multiple ways to perform the same functionality
- **Low coupling:** The class is as independent as possible
- **High cohesion:** The class has a well-defined area of responsibility

## GRASP Principles

GRASP stands for General Responsibility Assignment Software Patterns. These are design principles that help assign responsibilities to classes in object-oriented design.

### Low Coupling

A class should be as independent as possible. A class should be associated with only the few classes necessary for it to fulfill its scope of responsibility. Low coupling helps with:

- Isolation of changes
- Easier to understand the design
- Easier to recycle components

**Principle:** Assign responsibility so coupling is low.

### High Cohesion

A class must have a well-defined area of responsibility. A class must have a set of operations that support the scope of responsibility. High cohesion supports low coupling because if there are several areas of responsibility in a class several links quickly arise. Benefits include:

- Better understanding
- Easier maintenance
- Easier tests
- Easier recycling

**Principle:** Ensure a uniform area of responsibility.

### Creator

The Creator principle answers: Who is responsible for creating a class?

**B is the creator of A if:**

- B aggregates A
- B contains A
- B uses A
- B has initializing data for A

For example: Who creates SalesLineItem? The class that aggregates or contains it should be responsible.

### Information Expert

This principle assigns responsibility to objects based on the information they have. The class that has the necessary information to fulfill the responsibility should be assigned that responsibility.

**Process:**

- If there are relevant classes in the design model use them
- Otherwise use the domain model

For example: Who is responsible for calculating the total? The class that has access to all the items and their prices.

### Controller

The Controller principle determines which classes should be responsible for:

- Handling input events
- Communicating changes in the model layer to the view layer

Typically there is a controller per use case scenario. These are called use case controllers.

**Beware of Controller Bloat:** When controllers become too large they lack cohesion. Consider using facade controllers or splitting responsibilities.

### Opposition Between Creator and Low Coupling

Sometimes the Creator principle and Low Coupling principle conflict. For example which class should create a Payment object?

- **Creator:** The class that aggregates or contains Payment should create it
- **Low Coupling:** Creating it in that class might increase coupling

In such cases you must evaluate the trade-offs and choose the design that best balances the principles.

## Other GRASP Principles

Additional GRASP principles include:

- **Polymorphism:** Using polymorphic operations to handle variations in behavior
- **Pure Fabrication:** Creating a class that does not represent a domain concept to achieve low coupling and high cohesion
- **Indirection:** Introducing an intermediary to mediate between components and reduce coupling
- **Protected Variations:** Designing to protect elements from variations in other elements by wrapping them with a stable interface

## Design Patterns

Design patterns are design solutions to common problems that are generalizable across different contexts.

**GRASP:** Design principles for assigning responsibilities. Classes have responsibilities.

**GoF (Gang of Four):** A book of design patterns representing another set of software patterns for solving recurring design problems.