## Procedural vs Object-Oriented Programming

### Procedural Programming

Procedural programming organizes code as a hierarchy of calls to procedures and functions. The main program calls various procedures in sequence to accomplish tasks.

**Structure:**

- Main Program at the top
- Hierarchy of function/procedure calls
- Data and functions are separate

**Example:**

``` python
def computeArea(height, width):
    area = height * width
    return area
```

### Object-Oriented Programming (OOP)

Object-oriented programming organizes code around classes and objects. Classes send messages to each other to accomplish tasks instead of calling procedures directly.

**Structure:**

- Multiple classes that interact
- Classes send messages to each other
- Data and methods are bundled together in classes

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"{self.year} {self.make} {self.model}")

# Creating an object of the Car class
my_car = Car("Toyota", "Corolla", 2020)
my_car.display_info()  # Output: 2020 Toyota Corolla
```


---

## Classes

A class is a framework or blueprint for any concept in your domain. It defines the structure and behavior for objects of that type.

**Examples of concepts that can be classes:**

- Human
- Animal
- Student

### Class Structure

A class contains:

1. **Variables/Fields** - Store the state/data
2. **Methods** - Define the behavior/actions

**Example: Student Class**

``` java
public class Student {
    // Variables
    private String studentName;
    private String studentID;
    private Date dateOfBirth;

    // Constructor
    public Student(String studentName, String studentID, Date dateOfBirth) {
        this.studentName = studentName;
        this.studentID = studentID;
        this.dateOfBirth = dateOfBirth;
    }

    // Methods
    public void enrolInCourse() {
        // Implementation for enrolling in a course
    }

    public void unenrolInCourse() {
        // Implementation for unenrolling from a course
    }

    public void findStudyGroup() {
        // Implementation for finding a study group
    }

    // Getters and setters (optional)
    public String getStudentName() {
        return studentName;
    }

    public void setStudentName(String studentName) {
        this.studentName = studentName;
    }

    public String getStudentID() {
        return studentID;
    }

    public void setStudentID(String studentID) {
        this.studentID = studentID;
    }

    public Date getDateOfBirth() {
        return dateOfBirth;
    }

    public void setDateOfBirth(Date dateOfBirth) {
        this.dateOfBirth = dateOfBirth;
    }
}
```

---

## Objects

An instance of a class is called an object. A class can be viewed as a "high-level" datatype or better, a reference datatype. The class is in this view the datatype for the variable that holds the object.

### Exercise Example: Pasta Class

**Class: Pasta**

Fields/Properties:

- Shape
- Size
- Length
- Width (or radius)

**Object: Spaghetti**

- Shape = tube
- Size = big
- Length = long
- Width = thin

This demonstrates how a class (Pasta) serves as a blueprint, and an object (Spaghetti) is a specific instance with concrete values for each field.

---

## Constructors

A constructor is a method in a class that upon the creation of an object of the class is called. It can be seen and remembered as the "constructor" of the object because it builds the object.

The constructor is automatically executed when you create a new instance of a class, allowing you to initialise the object's fields and set up its initial state.

#### Example: Car class with constructor labelled
```python
public class Car {
    private String make;
    private String model;
    private int year;

    # Constructor to initialize the Car object
    public Car(String make, String model, int year) {
        this.make = make;
        this.model = model;
        this.year = year;
    }

    public void displayInfo() {
        System.out.println(year + " " + make + " " + model);
    }
}

# Usage
Car myCar = new Car("Toyota", "Corolla", 2020);
myCar.displayInfo();  // Output: 2020 Toyota Corolla
```

---

## Naming Conventions

### Class Naming Convention

- **Capitalised first letter**
- **Noun**
- **Singular**

Examples: `Student`, `Teacher`, `Pasta`, `Car`

### Object Naming Convention

- **Lowercase first letter**

Examples: `student`, `teacher`, `spaghetti`, `myCar`

---

## Sequence Diagrams

Sequence diagrams capture the sequence of events in a use case over time. They show how objects interact with each other through messages.

### Key Components

1. **Actors/Objects** - Shown at the top (e.g., Student, Teacher)
2. **Time axis** - Vertical axis showing progression of time downward
3. **Messages** - Horizontal arrows showing communication between objects
4. **Activation boxes** - Rectangles showing when an object is active/executing methods
5. **Conditions** - Can include conditional logic
6. **Loops** - Can show repeated interactions

![[Sequence Diagram.png | center | 600]]
#### Reading the Diagram

The sequence diagram shows three objects at the top from left to right:

- `:DiceGame`
- `d1:Die`
- `d2:Die`

The first event at the top is a call to `play()` from an actor (represented by a circle) to the `:DiceGame` object.

Then, the `:DiceGame` object sends messages to the two dice objects:

- To `d1:Die`:
  - `roll()`
  - `x = getFaceValue()`

- To `d2:Die`:
  - `roll()`
  - `y = getFaceValue()`

This sequence shows how the `DiceGame` coordinates rolling two dice and retrieving their face values by sending messages to each `Die` object.

---

## Key Differences: Procedural vs OOP

|Aspect|Procedural|Object-Oriented|
|---|---|---|
|Organization|Hierarchy of procedure calls|Classes sending messages|
|Data & Functions|Separate|Bundled together in classes|
|Main Unit|Function/Procedure|Class/Object|
|Communication|Direct function calls|Message passing between objects|
|Structure|Linear/hierarchical|Network of interacting objects|
