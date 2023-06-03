# JavaScript Variables

## What are variables?

In JavaScript, variables are used to store values that can be used and manipulated throughout your code. They provide a way to reference and manage data. Here are the different ways to declare and use variables in JavaScript, along with examples:

1. **var**
The `var` keyword was traditionally used to declare variables in JavaScript. However, it has been largely replaced by `let` and `const` in modern JavaScript. Nonetheless, it's still valid and supported.

**Example**
```javascript
var age = 25;
var name = "John";
var isStudent = true;
```

2. **let**
The `let` keyword allows you to declare block-scoped variables. Variables declared with `let` are limited in scope to the block, statement, or expression in which they are declared.

**Example**
```javascript
let age = 25;
let name = "John";
let isStudent = true;
```

3. **const**
The `const` keyword is used to declare variables that have a constant (unchanging) value. Once a constant variable is assigned a value, it cannot be re-assigned or modified.

**Example**
```javascript
const PI = 3.14;
const name = "John";

// Trying to re-assign a constant will result in an error
PI = 3.14159; // Error: Assignment to constant variable

// However, objects and arrays declared with const can still have their properties modified
const person = {
  name: "John",
  age: 25
};

person.age = 30; // Valid - modifying the property of the object
```
