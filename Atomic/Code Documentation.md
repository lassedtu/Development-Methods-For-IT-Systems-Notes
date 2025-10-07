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

[[Class]] or module comments describe the overall purpose of a [[Class]] or module. They explain what the class is for what kind of data it manages and how it interacts with other parts of the program. These comments are usually placed at the very top of the class file.

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

Docstrings are special comments at the start of functions [[Class]]es or modules. They are written in a structured format so tools can automatically generate documentation from them. In Java these are written using Javadoc style (`/** ... */`). Docstrings provide a standard way to explain the behavior inputs and outputs of code elements.

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
