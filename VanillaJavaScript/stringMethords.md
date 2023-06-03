# String Methods in JavaScript

Strings in JavaScript have built-in methods that allow us to perform various operations and manipulations on strings. Let's explore some commonly used string methods:

## .length

The `.length` property returns the number of characters in a string, including spaces. Here's an example:

```javascript
let str1 = "Hello String";
console.log(str1.length); // Output: 12
```

## .indexOf

The `.indexOf()` method returns the index of the first occurrence of a specified substring within a string. It returns -1 if the substring is not found. Here's an example:

```javascript
let str1 = "Hello String";
console.log(str1.indexOf(" ")); // Output: 5
```

## .includes

The `.includes()` method checks if a string contains a specified substring and returns `true` or `false` accordingly. Here's an example:

```javascript
let str1 = "Hello String";
console.log(str1.includes("A")); // Output: false
```

## .charAt

The `.charAt()` method returns the character at a specified index in a string. The index is zero-based. Here's an example:

```javascript
let str1 = "Hello String";
let res = str1.charAt(2);
console.log(res); // Output: l
```

## .slice

The `.slice()` method returns a new string that is a portion of the original string. It takes two optional parameters: the starting index and the ending index (exclusive). Here's an example:

```javascript
let str1 = "Hello String";
let substr = str1.slice(6);
console.log(substr); // Output: String
```

## .split

The `.split()` method splits a string into an array of substrings based on a specified delimiter. Here's an example:

```javascript
let str1 = "Hello String";
let strArr = str1.split(" ");
console.log(strArr); // Output: ["Hello", "String"]
```

## .startsWith and .endsWith

The `.startsWith()` method checks if a string starts with a specified substring and returns `true` or `false` accordingly. The `.endsWith()` method checks if a string ends with a specified substring and returns `true` or `false`. Here's an example:

```javascript
let str1 = "Hello String";
let start = str1.startsWith("H"); // true
let end = str1.endsWith("l"); // false
let startMulti = str1.startsWith("Hell"); // true

console.log("start", start, "end", end, "multistart", startMulti);
```

## .toUpperCase and .trim

The `.toUpperCase()` method converts a string to uppercase letters. The `.trim()` method removes whitespace from both ends of a string. Here's an example:

```javascript
let str1 = "Hello String";
let caseChange = str1.toUpperCase();
console.log(caseChange); // Output: HELLO STRING

let str2 = "           Hello                ";
let trimmed = str2.trim();
console.log("string2", str2, "trimmed", trimmed); // Output: string2            Hello                 trimmed Hello
```

These are just a few examples of the many string methods available in JavaScript. String methods help manipulate and extract information from strings, making them powerful tools for working with text data.

Remember to practice and experiment with these methods to become comfortable using them. Happy coding!
