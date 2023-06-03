# Objects in JavaScript

In JavaScript, objects are one of the most important data types. They are used to store and organize related data and functionalities together. An object consists of key-value pairs, where each key represents a property and each value represents the value of that property. Let's take a look at an example:

```javascript
let person = {
  name: "Kiran",
  age: 23,
  gender: "f",
  hobbies: ["programming", "music", "sleeping"],
  address: { street: "123 street", city: "london", postcode: 12345 },
  userInfo: () => {
    console.log("I am a function within an object");
  },
};
```

In this example, we have an object called `person` with several properties:

- `name` is a property with the value `"Kiran"`.
- `age` is a property with the value `23`.
- `gender` is a property with the value `"f"`.
- `hobbies` is a property with an array value `["programming", "music", "sleeping"]`.
- `address` is a property with an object value `{ street: "123 street", city: "london", postcode: 12345 }`.
- `userInfo` is a property with a function value that logs a message to the console.

To access the properties of an object, you can use dot notation or bracket notation:

```javascript
console.log("Name:", person.name);
console.log("Age:", person["age"]);
```

The output will be:

```
Name: Kiran
Age: 23
```

You can also modify the values of object properties:

```javascript
person.age = 20;
console.log("Updated Age:", person.age);
```

The output will be:

```
Updated Age: 20
```

## Object Methods

Objects can also have methods, which are functions defined as properties. In the previous example, `userInfo` is a method of the `person` object. You can call the method using dot notation:

```javascript
person.userInfo();
```

This will log the following message to the console:

```
I am a function within an object
```

## Object Utility Methods

JavaScript provides several utility methods to work with objects:

- `Object.keys()`: This method returns an array containing all the keys (property names) of an object.

```javascript
console.log(Object.keys(person));
```

The output will be:

```
["name", "age", "gender", "hobbies", "address", "userInfo"]
```

- `Object.values()`: This method returns an array containing all the values of an object.

```javascript
console.log(Object.values(person));
```

The output will be:

```
["Kiran", 20, "f", ["programming", "music", "sleeping"], { street: "123 street", city: "london", postcode: 12345 }, () => { console.log("I am a function within an object"); }]
```

- `Object.entries()`: This method returns an array of subarrays, each containing a key-value pair of the object.

```javascript
console.log(Object.entries(person));
```

The output will be:

```
[["name", "Kiran"], ["age", 20], ["gender", "f"], ["hobbies", ["programming", "music", "sleeping"]], ["address", { street: "123 street", city: "london", postcode: 12345 }], ["userInfo", () => { console.log("I am a function within an object"); }]]
```

- `hasOwnProperty()`: This method checks if an object has a specific property and returns

 a boolean value.

```javascript
console.log(person.hasOwnProperty("name"));
```

The output will be:

```
true
```

## Iterating over Object Properties

To iterate over the properties of an object, you can use the `for...in` loop. It iterates through the keys of the object, allowing you to access the corresponding values.

```javascript
for (let prop in person) {
  console.log(person[prop]);
}
```

This will log all the values of the `person` object to the console.

## Destructuring and Spread Operator

Destructuring and spread operator are useful features when working with objects and arrays.

Destructuring allows you to extract specific properties from an object into separate variables:

```javascript
let { name: person1name, hasCar = false } = person;
console.log("Person 1 Name:", person1name);
console.log("Has Car:", hasCar);
```

This will log the following output:

```
Person 1 Name: Kiran
Has Car: false
```

The spread operator (`...`) can be used to create copies of arrays or objects, or to combine them:

```javascript
let colors = ["red", "blue", "green"];
let colors2 = ["black", "orange", "yellow"];

console.log([...colors, "pink"]); // ["red", "blue", "green", "pink"]

let combinedArr = [...colors, "MID", ...colors2];
console.log(combinedArr); // ["red", "blue", "green", "MID", "black", "orange", "yellow"]

let person3 = { ...person, isNew: true, hobbies: ["Dancing"] };
console.log("Person 3:", person3);
```

The output will be:

```
Person 3: { name: "Kiran", age: 20, gender: "f", hobbies: ["Dancing"], address: { street: "123 street", city: "london", postcode: 12345 }, userInfo: () => { console.log("I am a function within an object"); }, isNew: true }
```

These are some of the basic concepts related to objects in JavaScript. Objects are a fundamental part of the language and understanding how to work with them is crucial for building complex applications.
