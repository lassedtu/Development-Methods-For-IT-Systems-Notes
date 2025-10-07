A [[class]] diagram is a type of static structure diagram in UML (Unified Modeling Language) used to describe the structure of a system by showing its classes, their attributes, operations, and the relationships among objects. Class diagrams provide a blueprint for building the system by defining software classes and how they interact.

## Purpose

- **Model the software structure** by defining classes and their relationships
- **Show attributes and operations** that classes have
- **Help developers understand** how the system is organized
- **Support design and implementation** by clarifying [[class]] responsibilities
- **Facilitate communication** among developers and stakeholders
- **Bridge analysis and design** phases of software development

## Key Elements

### Classes

Classes are blueprints for objects—they act as a sort of high-level data type.

- Represent software entities or concepts
- Shown as rectangles divided into three compartments:
    - **Top compartment**: Class name (capitalized first letter, noun, singular)
    - **Middle compartment**: Attributes or properties
    - **Bottom compartment**: Operations or methods

**Naming Convention**: `MovieTicketSystem`, `Person`, `Court`

### Example

![[Class Example.png | center | 400]]
### Attributes

- Define the data held by a [[class]] (contain the state of the object)
- Examples: `name`, `id`, `price`
- Include data type specifications: `int`, `char`, `float`, `double`, `boolean`, `String`
- **Visibility indicators**:
    - `+` Public: accessible from anywhere
    - `-` Private: accessible only within the class
    - `#` Protected: accessible within the class and subclasses

### Operations (Methods)

- Define the behavior or functions of a class
- Examples: `calculateTotal()`, `addItem()`, `getName()`, `setName()`
- Also include visibility indicators
- Define the behavior of the object

### Objects

Objects are instances of classes—they represent actual runtime entities.

**Naming Convention**: Lower case first letter (like a variable)

- Example: `MovieTicketSystem movieTicketSystem1;`
- Example: `Person person1;`

### Relationships (Associations)

Associations are connections between classes that represent relationships between objects.

**Must specify**:

- **Line** connecting the classes
- **Name** describing the relationship
- **Multiplicity** indicating cardinality

**Types include**:

- **Association**: a structural link between classes
- **Aggregation**: a whole-part relationship where parts can exist independently
- **Composition**: a stronger whole-part relationship where parts cannot exist without the whole
- **Inheritance (Generalization)**: a class inherits attributes and operations from a parent class
- **Dependency**: a class depends on another for some function

### Multiplicity

Indicates how many instances of a class relate to instances of another class.

|Symbol|Meaning|
|---|---|
|`0..1`|zero or 1|
|`1`|exactly 1|
|`0..*`|zero or more|
|`*`|zero or more|
|`1..*`|1 or more|
|`1..5`|1 to 5|

Placed near the ends of association lines.

### Association Classes

Association classes are part of the association between two other classes—they contain additional information about the relationship itself.

**Characteristics**:

- Provide additional information about the association
- Contain their own attributes
- Contain their own methods
- Can have their own associations

Example: A `Booking` association class between `Player` and `Court` might store booking time and duration.

## Analysis Classes vs Design Classes

### Analysis Classes (Domain Concepts)

- Derived from domain models
- Consist of data and behavior
- **Software implementation details are NOT specified**
- Focus on real-world concepts
- Used during requirements analysis

### Design Classes

- Consist of data and behavior
- **Software implementation details ARE specified**
- Include specific data types (`int`, `String`, etc.)
- Include visibility modifiers (`+`, `-`, `#`)
- Include complete method signatures
- Used during software design phase

## Class Diagram vs [[Domain Model]]

|Class Diagram|Domain Model|
|---|---|
|Software perspective|Conceptual perspective|
|Shows software classes (design classes)|Shows real-world concepts (domain concepts)|
|Includes attributes with types and operations|Focuses on attributes without implementation details|
|Shows inheritance and detailed relationships|Shows business relationships|
|Specifies visibility and data types|Does not specify implementation details|
|Used for design and implementation|Used for analysis and understanding the problem domain|

## Creation Process

### 1. Identify Classes (Domain Concepts)

**From requirements**: Look for **nouns** in problem descriptions

Example from badminton court system:

> "We would like to have a system that can manage our badminton courts. We have **players** and **coaches** who can book the **courts**. There are fixed intervals you can book courts in. The coaches can book all courts in a **hall**."

Identified classes: `Court`, `Player`, `Coach`, `Hall`

### 2. Define Responsibilities Using CRC Cards

**Class, Responsibility, Collaborators (CRC) Cards** - A brainstorming tool:

- **Nouns** become classes
- **Verbs** become responsibilities of the classes
- **Collaborators** become the other classes this class interacts with

### 3. Define Attributes and Operations

For each class:

- Specify attribute names and types
- Specify method names, parameters, and return types
- Add visibility indicators

### 4. Determine Relationships

Identify associations between classes:

- What classes need to interact?
- What is the nature of their relationship?
- What are the multiplicities?

### 5. Specify Multiplicity and Roles

Add multiplicity values to association ends to indicate cardinality.

### 6. Add Inheritance Hierarchies

Identify generalization relationships where applicable.

### 7. Review and Refine

Review with the development team and iterate.

## Packages

Packages provide logical grouping of model elements such as classes.

**Benefits**:

- Can show logical architecture of the system
- Organize classes into manageable modules
- Support layered architectures:
    - **Presentation layer**
    - **Business logic layer**
    - **Data access layer**
- Support multi-layered architectures for complex systems

![[Package.png | 600 | center]]