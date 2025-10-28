# Lecture 7 (GRASP, etc.) Overview
## Why should a system be modular? (Seperation of Concerns)

- **Division of development:** Breaks work into smaller parts so teams can work independently.  
- **Readability:** Smaller modules are easier to understand and manage.  
- **Easier fault isolation:** Problems can be found and fixed within specific modules quickly.  
- **Easier tests:** Modules can be tested separately, improving reliability.  
- **Recycling:** Modules can be reused in other projects, saving time.  
- **Easier replacement:** Individual parts can be updated or swapped without affecting the whole system.

## Example:

![[Modularity Example.png | center | 600 ]]

## Low Coupling and High Cohesion
High Cohesion and Low Coupling are mutually achieved. If you achieve one you automatically achieve the other.
### Low Coupling
Low coupling details that a class should be as independent as possible and it should be associated with the fewest amount of classes needed for it to fulfil it's role/scope of it's role.

### High Cohesion
High cohesion specifies that a class must have a well-defined area of responsibility. If it does not live up to this requirement it should conceptually be rethought. High Cohesion also outlines that a class must have a set of operations that support the scope of it's responsibility or role.

![[Low Coupling High Cohesion Example.png | center | 600]]


## Model View Controller

The model view controller pattern is extremely useful if your system has a component of UI.

When using the MVC Pattern (Model View Controller Architecture Pattern) your UI should not directly interact with your system. There should be a kind of middleman (The Controller / Brain).
Conversely the system should not directly interact with the UI. All "communication" should flow through the Controller which as the diagram shows controls and decides how the data is displayed as well as modifies the data to normalise and clean it for usage on the system.

![[MVC Architecture Pattern.png | center | 600]]

## Class Diagrams: Domain vs Design

**Domain Models** focus on the real-world concepts and entities relevant to the problem area. They show the key objects, their attributes, and relationships without worrying about implementation details. Use domain models early in the project to understand and communicate the problem space clearly.

**Design models**, on the other hand, represent how the system will be built. They include classes, methods, and interactions needed to implement the solution. Design models are more detailed and technical, guiding developers during coding and system construction.

Domain models should be used to model and explore the problem domain, where design models should be used to plan and document the actual system design.

## Connections among Classes in Class Diagrams

### Association  
Association represents a structural relationship where one class is connected to another. It shows that objects of one class use or are linked to objects of another. This is usually a "has-a" relationship and can be one-to-one, one-to-many, or many-to-many.

![[Association Connection.png | center | 400]]
### Dependency  
Dependency is a weaker relationship where one class depends on another because it uses it temporarily, such as calling its methods or accessing its data. It indicates that changes in the supplier class may affect the dependent class.

![[Dependency Connection.png | center | 400]]
### Generalisation  
Generalisation models an "is-a" relationship between a more general superclass and a more specific subclass. The subclass inherits attributes and behaviors from the superclass, allowing for reuse and polymorphism.

![[Generalisation Connection.png | center | 400]]
### Realisation (Interface)  
Realisation shows that a class implements an interface. It means the class agrees to provide the behavior defined by the interface, ensuring a contract for certain methods without specifying how they are implemented.

![[Realisation Connection.png | center | 400]]
### Composition  
Composition is a strong form of association representing a whole-part relationship where the part cannot exist independently of the whole. If the whole is destroyed, its parts are also destroyed. It implies ownership and lifecycle dependency.

![[Composition Connection.png | center | 400]]
### Aggregation  
Aggregation is a weaker whole-part relationship where the part can exist independently of the whole. It represents a shared ownership, meaning the part can belong to multiple wholes or exist on its own.

![[Aggregation Connection.png | center | 400]]

---

# The Principles of GRASP

GRASP stands for **G**eneral **R**esponsibility **A**ssignment **S**oftware **P**atterns. It is a set of principles used in object-oriented design to help assign responsibilities to classes and objects in a way that leads to maintainable, flexible, and understandable software.

The 9 fundamental GRASP principles are:
- Creator
- Information Expert
- Low Coupling
- High Cohesion
- Controller
- (Polymorphism)
- (Pure Fabrication)
- (Indirection)
- (Protected Variations)

## GRASP: Creator

The creator tells you who is responsible for creating a class.

B is the creator of A if:
- B Aggregates A
- B contains A
- B uses A
- B has initialising data for A

The more of these requirements are fulfilled, the better.

These requirements are what's called a "soft criteria" meaning that the idea behind these criteria is the ensure that the object creation is done by the class that is most closely associated with or has the most "knowledge" about the class to be created, which ensures cohesive design.

## GRASP: Information Expert

The information expert is not about creating objects or classes but it is the principle for assigning responsibility to objects (Given that we have a high number of classes in our system).

The information expert class is the one that has the necessary information to fulfil the responsibility of implementing a method.

## GRASP: Low Coupling

Low coupling details that a class should be as independent as possible and it should be associated with the fewest amount of classes needed for it to fulfil it's role/scope of it's role.

This is ensured through isolation of changes which makes the design easier to understand and easier to recycle for implementation of future functionality or features.

Responsibility should be assigned so coupling is low.

## GRASP: High Cohesion

High cohesion specifies that a class must have a well-defined area of responsibility. If it does not live up to this requirement it should conceptually be rethought. High Cohesion also outlines that a class must have a set of operations that support the scope of it's responsibility or role.

This creates the environment for having an easier time understanding the system or software, easier maintenance of code, easier implementation of tests and easier recycling of code.

High Cohesion and Low Coupling are mutually achieved. If you achieve one you automatically achieve the other.

![[Cohesion + Coupling.png | center | 600]]

## GRASP: Controller

The controller pattern is not just an architecture pattern (See [[MVC (Model View Controller)]]), it is also a principle of GRASP.

The controllers job is to handle communication between UI components and non-UI components. It is responsible for handling input events, communicating changes in the model layer to the view layer.

![[Controller.png | center | 600]]

In this diagram we have: User, View and Model. Following the Controller principle of GRASP we implement 2 Use Case Controllers ProcessSaleController and HandleReturnsController to process the sales and handle the returns. As seen on the diagram these formats and communicates the relevant information between the User, View and Model classes. Thereby indirectly letting the User and View classes interact with Model through the respective Controllers.

![[Use Case Controllers Class Diagram.png | center | 600]]

### Controller Bloat

Controller bloat occurs when a controller class takes on too many responsibilities, handling too much logic or coordinating too many tasks. This leads to low cohesion, making the controller hard to maintain, understand, and extend. It can also create tight coupling between unrelated parts of the system.

To avoid controller bloat, responsibilities should be distributed appropriately, often by creating multiple focused controllers or by delegating tasks to other classes. This keeps each controller manageable and aligned with the single responsibility principle.

**See the example below:**

![[Controller Bloat.png | center | 600]]

This design can be improved by creating unified controllers for similar classes:

![[Controller Bloat Fix.png | center | 600]]

The only difference here is that the unified controller takes in the vendorId as a parameter to differentiate between vendors.

## GRASP: Polymorphism

Polymorphism comes from the Greek words πολυ/poly (meaning many) and   
μορφή/morphi (meaning shapes or forms). Polymorphism is the principle that when we have several types of objects and when it is possible to do so we want to create a unified way of handling it.

Take the example where we have two classes, `Cat` and `Dog`. Both classes have a message called "talk", however a cat talks differently than a dog.

Using the principle of polymorphism an abstract class `Animal` is created which handles the shared behaviour between `Cat` and `Dog`.

```csharp
using System;

abstract class Animal
{
    // Abstract method to be implemented by subclasses
    public abstract void Talk();
}

class Cat : Animal
{
    public override void Talk()
    {
        Console.WriteLine("Meow");
    }
}

class Dog : Animal
{
    public override void Talk()
    {
        Console.WriteLine("Woof");
    }
}

class Program
{
    static void Main()
    {
        Animal myCat = new Cat();
        Animal myDog = new Dog();

        myCat.Talk();  // Output: Meow
        myDog.Talk();  // Output: Woof
    }
}
```


### Polymorphism Using Inheritance (Subtype Polymorphism)

**Nature**
- Polymorphism via inheritance arises from the **parent-child relationship** between classes.
- A **child class inherits** properties and methods from its **parent class**.
- The child class can **override** or **extend** the inherited methods to provide specific behavior.

**Key Characteristics**
- Most object-oriented languages like Java and C# support **single inheritance**, meaning a class can inherit from only one parent class.
- The child class **shares the same method signatures** as the parent but provides its own implementation.
- This allows treating objects of different child classes as instances of the parent class, enabling **dynamic method dispatch**.

**When to Use?**
- When there is a clear **"is-a" relationship**. For example, a `Dog` **is an** `Animal`.
- When you want to **reuse and extend** the base functionality of the parent class.
- When you want to **unify handling** of different subclasses through a common parent type.

```csharp
abstract class Animal
{
    public abstract void Talk();
}

class Cat : Animal
{
    public override void Talk() => Console.WriteLine("Meow");
}

class Dog : Animal
{
    public override void Talk() => Console.WriteLine("Woof");
}
```

Here, `Cat` and `Dog` inherit from `Animal` and override the `Talk()` method. You can treat both as `Animal` and call `Talk()` polymorphically.

### Polymorphism Using Interfaces

**Nature**
- Interfaces define a **contract**: a set of method declarations that implementing classes must provide.
- Interfaces contain **no implementation details**, only method signatures.
- Classes that implement an interface **agree to provide concrete implementations** for all its methods.

**Key Characteristics**
- A class can implement **multiple interfaces**, providing greater design flexibility.
- Interfaces allow polymorphism **without requiring a parent-child inheritance relationship**.
- This is especially useful in languages like Java that do not support multiple inheritance of classes.

**When to Use?**
- When various classes need to **adhere to a specific contract** but do not share a common parent class.
- When you want to **ensure certain classes have specific methods**, regardless of their place in the class hierarchy.
- When you want to **simulate multiple inheritance** by implementing multiple interfaces.

```csharp
interface ITalkable
{
    void Talk();
}

class Cat : ITalkable
{
    public void Talk() => Console.WriteLine("Meow");
}

class Dog : ITalkable
{
    public void Talk() => Console.WriteLine("Woof");
}
```

Here, both `Cat` and `Dog` implement the `ITalkable` interface, guaranteeing they provide a `Talk()` method. They can be used interchangeably where `ITalkable` is expected.

### Polymorphism using Method Overloading  
Multiple methods with the same name but different parameters in the same class. The correct method is chosen at compile-time.

```csharp
class Calculator
{
    public int Add(int a, int b) => a + b;
    public double Add(double a, double b) => a + b;
}
```

### Polymorphism Real-World Use Cases
Windows supports a wide variety of hardware devices like printers, graphics cards, audio devices, and more. The OS needs a standardised way to communicate with all these varied hardware components without knowing the specifics of each.

Imagine if Windows had to have a unique way of communicating with each specific model of every hardware device. This would require the operating system to be updated constantly as new hardware models are released, and the codebase would become immensely complex and
unmanageable.

In the following diagram, WindowsOS uses the DeviceDriver interface to communicate with devices.  PrinterDriver and GraphicsCardDriver are examples of specific drivers that implement this interface. This design allows new devices to be easily supported: a manufacturer simply writes a new driver that implements the DeviceDriver interface.

![[Windows Polymorphism Example.png | center | 600]]

