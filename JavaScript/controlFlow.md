
# Control Flow in JavaScript
Control flow refers to the order in which statements are executed in a program. In JavaScript, control flow is determined by conditional statements and loops, which allow us to make decisions and repeat actions based on certain conditions. Understanding control flow is essential for writing programs that perform different actions depending on specific situations.

## Conditional Statements

Conditional statements allow us to make decisions in our code based on specified conditions. The most commonly used conditional statements in JavaScript are:

### 1. If Statement

The `if` statement executes a block of code if a specified condition is true. Here's the basic syntax:

```javascript
if (condition) {
  // code to be executed if the condition is true
}
```

### 2. If-Else Statement

The `if-else` statement allows us to execute one block of code if the condition is true, and another block of code if the condition is false. Here's the syntax:

```javascript
if (condition) {
  // code to be executed if the condition is true
} else {
  // code to be executed if the condition is false
}
```

### 3. If-Else If-Else Statement

The `if-else if-else` statement allows us to test multiple conditions and execute different blocks of code accordingly. Here's the syntax:

```javascript
if (condition1) {
  // code to be executed if condition1 is true
} else if (condition2) {
  // code to be executed if condition2 is true
} else {
  // code to be executed if all conditions are false
}
```

## Loops

Loops are used to repeat a block of code multiple times until a certain condition is met. They help automate repetitive tasks and iterate over arrays or other data structures. JavaScript provides different types of loops:

### 1. For Loop

The `for` loop repeats a block of code a specified number of times. It consists of an initialization, a condition, and an increment or decrement expression. Here's the syntax:

```javascript
for (initialization; condition; increment/decrement) {
  // code to be executed in each iteration
}
```

### 2. While Loop

The `while` loop repeats a block of code while a specified condition is true. It checks the condition before executing the code block. Here's the syntax:

```javascript
while (condition) {
  // code to be executed in each iteration
}
```

### 3. Do-While Loop

The `do-while` loop is similar to the `while` loop, but it checks the condition after executing the code block. This guarantees that the code block is executed at least once. Here's the syntax:

```javascript
do {
  // code to be executed in each iteration
} while (condition);
```
