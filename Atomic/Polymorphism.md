Polymorphism comes from the Greek words πολυ/poly (meaning many) and   
μορφή/morphi (meaning shapes or forms). Polymorphism is the principle that when we have several types of objects and when it is possible to do so we want to create a unified way of handling it.

Take the example where we have two classes, `Cat` and `Dog`. Both classes have a message called "talk", however a cat talks differently than a dog.

Using the principle of polymorphism an [[abstract class]] `Animal` is created which handles the shared behaviour between `Cat` and `Dog`.

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


### Polymorphism Using [[Inheritance]] (Subtype Polymorphism)

**Nature**
- Polymorphism via [[inheritance]] arises from the **parent-child relationship** between classes.
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

