A domain model is a visual representation of the conceptual [[Class]]es, attributes, and relationships in the problem domain

It shows the real-world concepts and their relationships that are important for understanding the business or problem area

Domain models help bridge the gap between business understanding and software design by capturing the vocabulary and key concepts of the domain

## Purpose

- **Understand the problem domain** by identifying key concepts and their relationships
- **Establish common vocabulary** among [[Stakeholder]]s, analysts, and developers  
- **Capture business knowledge** in a visual, easy-to-understand format
- **Guide system design** by showing what the software needs to represent
- **Support requirements analysis** by clarifying business concepts

## Key Elements

### Conceptual [[Class]]es
- Represent real-world things, concepts, or ideas
- Examples: Customer, Order, Product, Account, Invoice
- Shown as boxes with [[Class]] names

### Attributes
- Properties or characteristics of conceptual classes
- Examples: Customer name, Order date, Product price
- Listed inside the class boxes

### Associations
- Relationships between conceptual classes
- Represent meaningful connections in the real world
- Shown as lines connecting classes
- Often labeled with relationship names

### Multiplicity
- Numbers that specify how many instances can participate in a relationship
- Examples: `1`, `*` (many), `0..1` (zero or one), `1..*` (one or many)
- Placed near the ends of association lines

## Examples by Domain

### Library Domain

![[Library Domain Model.png | center ]]

- **Classes**: Member, Book, Loan, Author, Category
- **Relationships**: Member borrows Book, Book written by Author
- **Attributes**: Member ID, Book ISBN, Loan date

### Hospital Domain  

![[Hospital Domain Model.png | center ]]

- **Classes**: Patient, Doctor, Appointment, Treatment, Room
- **Relationships**: Patient has Appointment with Doctor
- **Attributes**: Patient name, Doctor specialization, Appointment time

### E-commerce Domain

![[Ecommerce Domain Model.png | center ]]

- **Classes**: Customer, Order, Product, Payment, ShoppingCart
- **Relationships**: Customer places Order containing Products
- **Attributes**: Customer email, Product price, Order total

## Domain Model vs Class Diagram

| Domain Model | Class Diagram |
|--------------|---------------|
| Conceptual perspective | Software perspective |
| Real-world concepts | Software classes |
| Business vocabulary | Technical implementation |
| Analysis activity | Design activity |
| Shows **what exists** | Shows **how it's built** |

## Creation Process

1. **Identify conceptual classes** from requirements, [[Use Case]]s, and business knowledge
2. **Add attributes** that are important for the system to track
3. **Identify associations** between classes based on business relationships
4. **Add multiplicity** to specify relationship constraints
5. **Refine and validate** with [[Stakeholder]]s and domain experts

## Guidelines for Finding Classes

- Look for **nouns** in requirements and [[Use Case]]s
- Consider **physical objects** (Book, Computer)
- Consider **concepts** (Sale, Appointment, Account)
- Consider **events** (Purchase, Registration, Meeting)
- Consider **roles** (Customer, Manager, Student)
- Consider **places** (Store, Classroom, Office)

## Common Mistakes

- Including **software artifacts** (databases, user interfaces)
- Adding **implementation details** (methods, technical attributes)
- Creating **too many associations** without clear business meaning
- Missing **important conceptual classes** from the problem domain
- Confusing **domain concepts** with software design elements

## Relationship to Other Artifacts

- **Derived from** [[Use Case]]s, requirements, and business knowledge
- **Informs** software class design and database design
- **Supports** [[Business Rules]] understanding and validation
- **Referenced in** [[Supplementary Specification]] and design documents
- **Updated during** [[Elaboration]] as understanding deepens

## Domain Model in UP Phases

- **[[Inception]]**: Create initial domain model with key concepts
- **[[Elaboration]]**: Refine and detail the domain model extensively  
- **[[Construction]]**: Use domain model to guide implementation
- **[[Transition]]**: Validate domain model represents actual business correctly

## Benefits

- **Improves communication** between technical and business teams
- **Reduces misunderstandings** about business concepts
- **Guides software design** with business-focused structure
- **Documents business knowledge** for future reference
- **Supports system maintenance** by preserving business logic understanding
