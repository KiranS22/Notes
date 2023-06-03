# JavaScript Functions

## What are functions in JavaScript?
A function is a reusable block of code that performs a specific task or calculates a value. Functions help organize code into modular and reusable pieces, improving code readability, maintainability, and reusability.

## Ways to declare a function
There are 3 main ways to declare a function in JavaScript. These are:

### 1. Function Declaration
```javascript
function greet(name) {
  console.log("Hello, " + name + "!");
}

// Calling the function
greet("Alice"); // Output: Hello, Alice!
greet("Bob"); // Output: Hello, Bob!
```
In the example above, we can see the function declaration syntax. It starts with the `function` keyword, which tells JavaScript that you are about to write a function. The curly braces `{}` indicate the body of your function, where you write the code you want to execute.

### 2. Function Expression
```javascript
const greet = function(name) {
  console.log("Hello, " + name + "!");
};

greet("Alice"); // Output: Hello, Alice!
```
In a function expression, a function is defined as a value assigned to a variable. In the example above, we assign an anonymous function to the variable `greet`. The function takes a `name` parameter and logs a greeting message to the console. We can then call the `greet` function using the variable name.

### 3. Arrow Function Syntax (ES6)
```javascript
const greet = (name) => {
  console.log("Hello, " + name + "!");
};

greet("Alice"); // Output: Hello, Alice!
```
Arrow function syntax is a concise way to define functions introduced in ECMAScript 6 (ES6). It uses the `=>` syntax. In the example above, we define an arrow function that takes a `name` parameter and logs a greeting message to the console. The arrow function can be assigned to a variable (`greet` in this case) and called using the variable name.


###  Calling a Function
Calling a function in JavaScript refers to executing or invoking the function to perform its defined task.To call a fuinction in JavaScript we use parenthsis `()` When a function is called, the code inside the function's body is executed, and any specified arguments are passed to the function if needed. Here's an explanation of how to call a function in JavaScript:
```javascript
const greet = (name) => {
  console.log("Hello, " + name + "!");
};

greet("Alice"); // Output: Hello, Alice!
```
In this example, the function greet is called by writing greet("Alice"). The string "Alice" is passed as an argument to the function, and it will be used as the name parameter inside the function body. The output will be Hello, Alice!

The way we call JavaScript functions is the same regardless of the syntax used


### Function Parameters
Function parameters are placeholders or variables specified in the function declaration. They allow you to pass values into the function when calling it, making functions more flexible and reusable. Parameters act as local variables within the function's scope and are used to receive and process the input values.

Here's an example of a function with parameters:

```javascript
function greet(name) {
  console.log("Hello, " + name + "!");
}

greet("Alice"); // Output: Hello, Alice!
greet("Bob"); // Output: Hello, Bob!
```

In this example, the `greet` function has a single parameter called `name`. When calling the `greet` function, we pass a value as an argument inside the parentheses. For instance, `greet("Alice")` passes the string `"Alice"` as the argument for the `name` parameter. The function then uses the value of the `name` parameter to construct and log a greeting message to the console.

Function parameters can also have default values. If a parameter is not provided with an argument during the function call, the default value is used instead. Here's an example:

```javascript
function greet(name = "Guest") {
  console.log("Hello, " + name + "!");
}

greet(); // Output: Hello, Guest!
greet("Alice"); // Output: Hello, Alice!
```

In this modified `greet` function, the `name` parameter has a default value of `"Guest"`. When we call `greet()` without providing an argument, the default value is used, and the output is `Hello, Guest!`. However, if we pass an argument such as `greet("Alice")`, the value `"Alice"` replaces the default value, and the output becomes `Hello, Alice!`.

Functions can have multiple parameters separated by commas:

```javascript
function addNumbers(num1, num2) {
  return num1 + num2;
}

let result = addNumbers(3, 5);
console.log(result); // Output: 8
```

In this example, the `addNumbers` function takes two parameters, `num1` and `num2`. We pass the values `3` and `5` as arguments when calling the function, and the function returns the sum of the two numbers.

Function parameters play a crucial role in making functions flexible and adaptable to different inputs. They allow functions to accept values dynamically and perform operations accordingly.
