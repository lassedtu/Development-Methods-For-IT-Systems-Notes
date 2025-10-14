# Activity Diagram

An activity diagram shows how steps in a process or system flow from start to end. It helps you see what happens first what comes next and where choices or parallel actions occur.

It breaks big workflows into smaller steps so you can understand or improve them.

Main parts of an activity diagram:

- **Actions:** single tasks that cannot or should not be broken down further. They are the basic steps in a process. 
- **Transitions:** arrows showing the flow from one step to the next.
- **Start:** marks where the process begins.
- **Stop:** marks where the process ends. There are two types:
    - **Activity Final:** ends the entire activity. Everything stops.
    - **Flow Final:** ends only that specific flow. Other flows keep running.
- **Decision (Branch):** the flow splits into different paths based on a condition or choice. Only one path is followed.
- **Merge:** different paths come back together into one flow after a decision.
- **Loop (Iteration):** a flow that repeats certain actions until a condition is met.
- **Fork:** the flow splits into multiple paths that run at the same time.
- **Join:** multiple parallel paths come back together into one flow.
- **Swim Lanes / Partitions:** divide the diagram into sections showing who or what is responsible for each step.
- **Accept Event Action:** waits for an external event like a message or signal before continuing.
- **Wait Time Action:** pauses the flow for a set time before moving to the next step.


![[Activity Diagram.png]]

# Components of The Activity Diagram
I will now explain each component of the activity diagram using the diagram below if possible.

![[Activity Diagram 2.png | center | 600]]

## Actions
An action is a single or atomic operation meaning it cannot or should not be broken down into smaller steps. Actions represent the fundamental tasks or activities that occur within a process.

![[Action.png |center | 600]]
## Branch
A branch is a point where the flow can go in different directions based on a condition or choice (also called a guard). Only one path is followed depending on what happens or what the condition says.

![[Branch.png | center | 600]]
## Merge
A merge is a point where different paths come back together into one flow. It happens after a decision when only one of the paths was taken.

![[Merge.png | center | 600]]

## Loop (Iterations)
A loop is a part of the flow that repeats the same actions until a certain condition is met or no longer true.

``` Pseudocode
number_of_users ← 0
while number_of_users < 5 do
n = get_number_of_users()
number_of_users = number_of_users + n
end while
Display all user’s details
```

![[Activity Diagram Loop.png | center | 600]]

## Start
A start shows where the process or activity begins. It marks the first step in the flow.

![[Start.png| 400 | center]]
## Stop
A stop shows where the process ends. There are two types:
- **Activity Final:** ends the entire activity. Everything in the diagram stops.
- **Flow Final:** ends only that specific flow. Other flows can keep running.

### Activity Final:
![[Activity Final.png| center | 400]]
### Flow Final:

![[Flow Final.png | center | 400]]
## Fork
A fork is a point where the flow splits into two or more paths that run at the same time. Each path continues independently.

![[Fork.png | 400 | center ]]

## Join
A join is a point where multiple parallel paths come back together into one flow after running at the same time.

![[Join.png | 400 | center]]

## Swim Lanes / Partitions
A swim lane (or partition) divides the diagram into sections that show who or what is responsible for each action. Each lane represents a person group or system part that performs the steps inside it.

![[Swim Lanes.png | center | 600]]

## Event-based actions
### Accept Event Action 
Waits for an external event like a message or signal before continuing the flow.

![[Accept Event Action.png | center | 400]]
### Wait Time Action 
Pauses the flow for a set amount of time before moving to the next step.

![[Wait Time Action.png | center | 400]]

## Activity Diagram of KMP Algorithm

![[KMP Activity Diagram.png | center | 600]]

---

# Code Documentation

Code documentation explains what the code does and how to use it. It helps others or yourself understand the purpose behavior and structure of a program. Good documentation makes code easier to maintain debug and extend over time. It can appear directly in the code or in external files.

## Inline Comments

Inline comments are short notes written directly inside the code. They explain what specific lines or small blocks of code are doing. These comments are helpful when the code is not immediately obvious or when you want to clarify why something is done a certain way. Keep them brief and focused.

```java
int sum = a + b; // add two numbers and store the result
```

## Function/Method Comments

These comments describe what a function or method does. They explain its purpose the inputs it expects and the outputs it returns. Method comments help other developers know how to use the function without reading its internal code. They are often written in **Javadoc style** in Java so they can be processed by tools to generate formal documentation.

```java
/**
 * Adds two integers and returns the result
 * @param a first number
 * @param b second number
 * @return sum of a and b
 */
public int add(int a int b) {
    return a + b;
}
```

## Class/Module Comments

Class or module comments describe the overall purpose of a class or module. They explain what the class is for what kind of data it manages and how it interacts with other parts of the program. These comments are usually placed at the very top of the class file.

```java
/**
 * This class represents a simple calculator
 * It can perform basic arithmetic operations like add subtract multiply and divide
 */
public class Calculator {
    // methods go here
}
```

## Docstrings

Docstrings are special comments at the start of functions classes or modules. They are written in a structured format so tools can automatically generate documentation from them. In Java these are written using Javadoc style (`/** ... */`). Docstrings provide a standard way to explain the behavior inputs and outputs of code elements.

```java
/**
 * Multiplies two numbers
 * @param x first number
 * @param y second number
 * @return product of x and y
 */
public int multiply(int x int y) {
    return x * y;
}
```

## External Documentation

External documentation is kept outside the code in separate files such as `README.md` or manuals. It usually explains the project structure setup instructions usage examples and design decisions. External documentation is useful for new developers users or anyone who wants to understand the project without diving into the code itself.

```markdown
README.md example:

# Simple Calculator
This project implements a basic calculator in Java. 
It supports addition subtraction multiplication and division.

## Usage
1. Compile Calculator.java
2. Run Main.java
```

## Best Practices

Good documentation is clear simple and up to date. Avoid commenting obvious code. Focus on explaining **why** a piece of code exists how it works in context or any special considerations. Update comments when the code changes to prevent misleading information.

```java
// Good: explains why the code exists or what it achieves
// Bad: repeats obvious code

int count = 0; // Good: reset counter at start of loop

int i = 0; // Bad: don't write "initialize i to 0" - it's obvious
```
