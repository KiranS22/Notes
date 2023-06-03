# JavaScript Data Types

JavaScript has two main categories of data types: **Primitive** and **Reference** types. Understanding these data types and their characteristics is important for writing effective JavaScript code. Let's explore these data types and discuss mutability versus immutability.

## Primitive Data Types

Primitive data types are **immutable**, meaning their values cannot be changed after they are created. Here are the commonly used primitive data types in JavaScript:

### 1. Number

The `Number` data type represents numeric values.

```javascript
let age = 25;
let price = 9.99;
```

### 2. String

The `String` data type represents a sequence of characters.

```javascript
let name = "John Doe";
let message = 'Hello, world!';
```

### 3. Boolean

The `Boolean` data type represents a logical value, either `true` or `false`.

```javascript
let isStudent = true;
let hasCar = false;
```

### 4. Undefined

The `Undefined` data type represents a variable that has been declared but has not been assigned a value.

```javascript
let undefinedVariable;
```

### 5. Null

The `Null` data type represents the intentional absence of any object value.

```javascript
let nullValue = null;
```

## Reference Data Types

Reference data types are **mutable**, meaning their values can be changed after they are created. These types store a reference to the actual data, rather than the data itself. Here are the commonly used reference data types in JavaScript:

### 1. Object

The `Object` data type represents a collection of key-value pairs and can store various types of data.

```javascript
let person = {
  name: "John Doe",
  age: 25,
  isStudent: true,
};
```

### 2. Array

The `Array` data type represents an ordered list of values.

```javascript
let numbers = [1, 2, 3, 4, 5];
let fruits = ["apple", "banana", "orange"];
```

### 3. Function

The `Function` data type represents a reusable block of code that can be called to perform a specific task.

```javascript
function greet(name) {
  console.log("Hello, " + name + "!");
}
```


## Mutability vs Immutability

As mentioned earlier, primitive data types are immutable, while reference data types are mutable. Let's understand this concept with examples:

```javascript
let x = 5;
let y = x;
x = 10;

console.log(x); // 10
console.log(y); // 5
```

In this example, changing the value of `x` does not affect the value of `y` because `x` and `y` are independent copies of the value.

However, with reference types, changes to one variable can affect other variables that reference the same data:

```javascript
let arr1 = [1, 2, 3];
let arr2 = arr1;
arr1.push(4);

console.log(arr1); // [1, 2, 3, 4]
console.log(arr2); // [1, 2, 3, 4
