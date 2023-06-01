<h1 style="color:purple;">JavaScript Variables</h1>
<h2 style="text-decoration:underline">What are variables?</h2>
<p>In JavaScript, variables are used to  store values that can be used and manipulated throughout your code. They provide a way to reference and manage data. Here are the different ways to declare and use variables in JavaScript, along with examples:</p>
<p> 1. <b>var</b> <br>The var keyword was traditionally used to declare variables in JavaScript. However, it has been largely replaced by let and const in modern JavaScript. Nonetheless, it's still valid and supported.</p>
<br/>
<h3>Example</h3>
```
var age = 25;
var name = "John";
var isStudent = true;
```

<p> 2. <b>let</b> <br>The let keyword allows you to declare block-scoped variables. Variables declared with let are limited in scope to the block, statement, or expression in which they are declared..</p>
<br/>
<h3>Example</h3>
```
let age = 25;
let name = "John";
let isStudent = true;
```
<p> 3. <b>const</b> <br> The const keyword is used to declare variables that have a constant (unchanging) value. Once a constant variable is assigned a value, it cannot be re-assigned or modified.</p>

<h3>Example</h3>
```
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
