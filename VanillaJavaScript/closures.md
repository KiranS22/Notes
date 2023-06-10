# Closures

## Definition

A closure is a concept in programming where a function has access to the variables from its outer function or lexical scope, even after the outer function has finished executing. This allows the function to "close over" or capture those variables, hence the term "closure". Closures enable functions to maintain and access the values of variables that were in scope when the function was defined.

## Example

```javascript
const appleTree = () => {
  let aVariable = "apple";
  const tree = () => {
    return aVariable;
  };
  return tree();
};
console.log(appleTree()); // Output: "apple"
```

In this example, the `tree` function is defined within the `appleTree` function and uses the `aVariable` from the outer function. The `tree` function captures the value of `aVariable` and returns it. When we invoke the `appleTree` function, it returns the `tree` function, which in turn returns the value of `aVariable`, resulting in the output "apple". Even though `aVariable` is not declared within the `tree` function, it has access to it through the closure.

## Accessing an Outer Function's Variable with Closures

Closures allow an inner function to access and use variables from its outer function. This is achieved through scope chaining, where the inner function has access to the variables in its own scope as well as the variables in the scopes of its outer functions.

```javascript
const appleTree = () => {
  let aVariable = "apple";
  const tree = () => {
    return aVariable;
  };
  return tree();
};
console.log(appleTree()); // Output: "apple"
```

In this example, the `tree` function captures the `aVariable` from the `appleTree` function and returns its value. The inner function, `tree`, has access to the `aVariable` through the closure, even though it was not declared within the `tree` function. The value "apple" is printed as the output.

## Changing an Outer Function's Variable using Closures

Closures not only allow access to outer function variables but also enable inner functions to modify those variables.

```javascript
const appleTree2 = () => {
  let tree = { type: "apple", grown: false };
  const growTree = () => {
    tree.grown = true;
  };
  growTree();
  return tree;
};
console.log(appleTree2()); // Output: { type: "apple", grown: true }
```

In this example, the `growTree` function captures the `tree` variable from the `appleTree2` function and changes its `grown` property to `true`. The inner function can modify the variable because it has access to it through the closure. The returned object `{ type: "apple", grown: true }` shows that the variable was successfully changed.

## Closures Closing Over Variables of a Returned Function

Closures can also close over variables of a returned function, allowing access and manipulation of those variables even after the outer function has finished executing.

```javascript
const treeMaker = () => {
  let trees = [];
  const addTree = (tree) => {
    trees.push(tree);
    return trees;
  };
  return addTree;
};

const treeFunc = treeMaker();
treeFunc("Pine");
```

In this example, the `treeMaker` function returns the `addTree` function. When we invoke `treeMaker`, it assigns the returned `addTree` function to the `treeFunc` variable. Later, we can call `treeFunc` with the argument "Pine", which pushes "Pine" into the `trees

` array and returns the modified `trees` array. Even though the outer function has finished executing, the `addTree` function still has access to the `trees` array through the closure, allowing us to manipulate the array indirectly.

## Private State using Closures

Closures provide a way to create and maintain private state within functions. By encapsulating variables within an outer function and returning inner functions that can access and modify those variables, we can achieve data privacy.

```javascript
const createCounter = () => {
  let count = 0;
  return () => {
    count++;
    return count;
  };
};

let counter = createCounter();
console.log(counter()); // Output: 1
console.log(counter()); // Output: 2

let anotherCounter = createCounter();
console.log(anotherCounter()); // Output: 1
console.log(anotherCounter()); // Output: 2
```

In this example, the `createCounter` function returns an inner function that increments a `count` variable and returns its updated value. The `count` variable is encapsulated within the outer function and is not directly accessible from outside. Each time we invoke `createCounter`, it creates a new instance of `count` and returns an inner function specific to that instance. This allows us to have multiple independent counters that maintain their own state. Each counter has its own closure, capturing its respective `count` variable. The output shows that the counters work independently, incrementing from 1 each time they are called.

Closures are a powerful concept in programming that enables functions to retain access to variables from their outer scopes, facilitating encapsulation, data privacy, and flexible code organization.
