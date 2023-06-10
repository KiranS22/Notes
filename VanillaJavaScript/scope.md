# Scopes in JavaScript

In JavaScript, scopes define the accessibility and lifetime of variables and functions within the code. Understanding the different scopes is essential for understanding how variables are declared, accessed, and managed in JavaScript.

## Global Scope

The global scope is the outermost scope in JavaScript, encompassing the entire code. Variables declared in the global scope are accessible from any part of the code, including nested functions and blocks.

Example:

```javascript
let globalVariable = "I'm in the global scope";

function foo() {
  console.log(globalVariable); // Accessible within functions
}

console.log(globalVariable); // Accessible outside functions
```

In the example above, `globalVariable` is declared in the global scope and can be accessed both inside and outside of functions.

## Function Scope

A function scope is created whenever a function is defined. Variables declared within a function scope are accessible only within that function and any nested functions.

Example:

```javascript
function outerFunction() {
  let outerVariable = "I'm in the outer function";

  function innerFunction() {
    let innerVariable = "I'm in the inner function";
    console.log(innerVariable); // Accessible within the inner function
    console.log(outerVariable); // Accessible within nested functions
  }

  console.log(outerVariable); // Accessible within the outer function
  console.log(innerVariable); // Error: innerVariable is not defined
}
```

In the above example, `outerVariable` is accessible within both the outer function and the nested inner function. However, `innerVariable` is only accessible within the inner function.

## Block Scope (Introduced in ES6)

Block scope was introduced in ECMAScript 6 (ES6) with the `let` and `const` keywords. It defines a scope for variables within a block, which is typically denoted by a pair of curly braces `{}`.

Example:

```javascript
function foo() {
  if (true) {
    let blockVariable = "I'm in the block scope";
    console.log(blockVariable); // Accessible within the block
  }

  console.log(blockVariable); // Error: blockVariable is not defined
}
```

In this example, `blockVariable` is accessible only within the if block. It is not accessible outside of the block due to block scope.

## Lexical Scope

Lexical scope, also known as static scope, is determined by the physical placement of variables and functions in the source code. It describes how variables are resolved based on the nesting structure of scopes.

Example:

```javascript
let globalVariable = "I'm in the global scope";

function outerFunction() {
  let outerVariable = "I'm in the outer function";

  function innerFunction() {
    console.log(globalVariable); // Accessible due to lexical scope
    console.log(outerVariable); // Accessible due to lexical scope
  }

  innerFunction();
}

outerFunction();
```

In the above example, both `globalVariable` and `outerVariable` are accessible within the `innerFunction` due to lexical scoping. The inner function can access variables from its own scope as well as from its outer scopes, following the lexical structure of the code.

Understanding the different scopes in JavaScript is crucial for managing variable visibility, avoiding naming conflicts, and writing efficient and maintainable code. It allows developers to control the accessibility and lifetime of variables based on their intended usage and requirements.
