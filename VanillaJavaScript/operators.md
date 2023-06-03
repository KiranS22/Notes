## What are Operators?

JavaScript operators are symbols used to perform operations on values or variables. They can be categorized into different types, including arithmetic, assignment, comparison, logical, bitwise, and more. Here are some examples of JavaScript operators:

**Arithmetic Operators:**

Arithmetic operators are used to perform mathematical calculations. Examples of these include:

- `+` used for addition
- `-` used for subtraction
- `*` used for multiplication
- `**` used to calculate the left value, to the power of the right value
- `%` used to find the remaining sum after division
- `/` used for division
- `++` used to increment a number by one
- `--` used to decrease a number by one

**Example**
```javascript
let x = 5;
let y = 2;

console.log(x + y); // Addition: 7
console.log(x - y); // Subtraction: 3
console.log(x * y); // Multiplication: 10
console.log(x / y); // Division: 2.5
console.log(x % y); // Modulus (remainder): 1
console.log(x ** y); // Exponentiation: 25
console.log(++x);   // Increment: 6
console.log(--y);   // Decrement: 1
```

**Assignment Operators:**

Assignment operators are used to assign values to variables.

**Example**
```javascript
let x = 5;

x += 3; // Equivalent to: x = x + 3
console.log(x); // Output: 8

x -= 2; // Equivalent to: x = x - 2
console.log(x); // Output: 6

x *= 4; // Equivalent to: x = x * 4
console.log(x); // Output: 24

x /= 3; // Equivalent to: x = x / 3
console.log(x); // Output: 8

x %= 5; // Equivalent to: x = x % 5
console.log(x); // Output: 3
```

**Comparison Operators:**

Comparison operators are used to compare values. Examples of these include:

- `>` used to calculate if one value is greater than another
- `<` used to calculate if one value is less than another
- `>=` used to calculate if a value is greater than or equal to another value
- `<=` used to calculate if a value is less than or equal to another value
- `==` used to check if two values are equal (value only)
- `===` used to check if two values are equal (by both type and value)
- `!=` used to check if two values are not equal (value only)
- `!==` used to check if two values are not equal (by both type and value)

**Example**
```javascript
let x = 5;
let y = 3;

console.log(x > y);   // Greater than: true
console.log(x < y);   // Less than: false
console.log(x >= y);  // Greater than or equal to: true
console.log(x <= y);  // Less than or equal to: false
console.log(x == y);  // Equal to: false
console.log(x === y); // Equal to (strict): false
console.log(x != y);  // Not equal to: true
console.log(x !== y); // Not equal to (strict): true
```

### Logical Operators

Logical operators are used to combine or manipulate boolean (logical) values. JavaScript has three logical operators: `&&` (AND), `||` (OR), and `

!` (NOT). These operators can be used to create complex conditions or make decisions based on multiple conditions.

Here are examples of logical operators in action:

**AND (`&&`) Operator:**

The AND operator returns `true` if both operands are `true`; otherwise, it returns `false`. It evaluates the second operand only if the first operand is `true`.

```javascript
let x = 5;
let y = 10;

console.log(x > 0 && y > 0);   // Output: true
console.log(x > 0 && y < 0);   // Output: false
console.log(x < 0 && y > 0);   // Output: false
```

**OR (`||`) Operator:**

The OR operator returns `true` if at least one of the operands is `true`; otherwise, it returns `false`. It evaluates the second operand only if the first operand is `false`.

```javascript
let a = 15;
let b = 7;

console.log(a > 10 || b > 10);  // Output: true
console.log(a > 10 || b < 5);   // Output: true
console.log(a < 10 || b < 5);   // Output: false
```

**NOT (`!`) Operator:**

The NOT operator is a unary operator that negates the boolean value of its operand. If the operand is `true`, the NOT operator returns `false`, and if the operand is `false`, it returns `true`.

```javascript
let isSunny = true;

console.log(!isSunny);  // Output: false
console.log(!(5 > 10)); // Output: true
```

These logical operators are frequently used in conditional statements, loops, and other situations where you need to perform logical operations on boolean values.
