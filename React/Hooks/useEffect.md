# Understanding useEffect in React

In React, `useEffect` is a built-in hook that allows you to perform side effects in functional components. Side effects may include fetching data, subscribing to events, or manually interacting with the DOM. In this markdown file, we will explain the basics of `useEffect` and how to use it effectively in React.

## Introduction to useEffect

The `useEffect` hook is used to handle side effects in functional components. Side effects are actions that occur outside of the regular component rendering process and may impact the component or its surrounding environment. Examples of side effects include fetching data from an API, setting up event listeners, or updating the document title.

`useEffect` is similar to lifecycle methods in class components, such as `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount`. It allows you to execute code based on certain conditions, such as when the component mounts, when specific props or state values change, or when the component unmounts.

## Basic Usage of useEffect

To use `useEffect`, you need to import it from the `react` package at the beginning of your functional component:

```jsx
import React, { useEffect } from "react";
```

The basic syntax of `useEffect` is as follows:

```jsx
useEffect(() => {
  // Side effect code here
  // This code will run after every render
});
```

The arrow function passed to `useEffect` represents the effect or side effect you want to perform. It will run after every render of the component.

## Controlling When useEffect Runs

By default, `useEffect` runs after every render. However, you can control when it runs by specifying dependencies as the second argument to the hook. Dependencies are an array of values that `useEffect` watches for changes. If any of the dependencies change, the effect will be executed.

```jsx
useEffect(() => {
  // Side effect code here
  // This code will run when the dependencies change
}, [dependency1, dependency2]);
```

For example, if you only want the effect to run once when the component mounts, you can provide an empty array `[]` as the second argument. This ensures that the effect does not have any dependencies and only runs on the initial render.

```jsx
useEffect(() => {
  // Side effect code here
  // This code will run once when the component mounts
}, []);
```

## Cleaning Up with useEffect

`useEffect` can also return a cleanup function to handle any necessary cleanup operations. This is particularly useful for unsubscribing from subscriptions, clearing timers, or releasing resources.

```jsx
useEffect(() => {
  // Side effect code here
  // This code will run after every render
});
```

The cleanup function returned by `useEffect` will be executed when the component is about to unmount or when the dependencies change before the next execution of the effect.

## Example Usage

Here's an example that demonstrates the usage of `useEffect` in a component:

```jsx
import React, { useEffect, useState } from "react";

function ExampleComponent() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `Count: ${count}`;
  }, [count]);

  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```


Understanding useEffect in React
In React, useEffect is a built-in hook that allows you to perform side effects in functional components. Side effects may include fetching data, subscribing to events, or manually interacting with the DOM. In this markdown file, we will explain the basics of useEffect and how to use it effectively in React.

Introduction to useEffect
The useEffect hook is used to handle side effects in functional components. Side effects are actions that occur outside of the regular component rendering process and may impact the component or its surrounding environment. Examples of side effects include fetching data from an API, setting up event listeners, or updating the document title.

useEffect is similar to lifecycle methods in class components, such as componentDidMount, componentDidUpdate, and componentWillUnmount. It allows you to execute code based on certain conditions, such as when the component mounts, when specific props or state values change, or when the component unmounts.

Basic Usage of useEffect
To use useEffect, you need to import it from the react package at the beginning of your functional component:

jsx
Copy code
import React, { useEffect } from 'react';
The basic syntax of useEffect is as follows:

jsx
Copy code
useEffect(() => {
  // Side effect code here
  // This code will run after every render
});
The arrow function passed to useEffect represents the effect or side effect you want to perform. It will run after every render of the component.

Controlling When useEffect Runs
By default, useEffect runs after every render. However, you can control when it runs by specifying dependencies as the second argument to the hook. Dependencies are an array of values that useEffect watches for changes. If any of the dependencies change, the effect will be executed.

jsx
Copy code
useEffect(() => {
  // Side effect code here
  // This code will run when the dependencies change
}, [dependency1, dependency2]);
For example, if you only want the effect to run once when the component mounts, you can provide an empty array [] as the second argument. This ensures that the effect does not have any dependencies and only runs on the initial render.

jsx
Copy code
useEffect(() => {
  // Side effect code here
  // This code will run once when the component mounts
}, []);
Cleaning Up with useEffect
useEffect can also return a cleanup function to handle any necessary cleanup operations. This is particularly useful for unsubscribing from subscriptions, clearing timers, or releasing resources.

jsx
Copy code
useEffect(() => {
  // Side effect code here
  // This code will run after every render
}[] // even if the code inside the useEffect does not have any dependancies, it is good practice to always unclude the dependancy array );


Example Usage
Here's an example that demonstrates the usage of useEffect in a component:
```
import React, { useEffect, useState } from 'react';

function ExampleComponent() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `Count: ${count}`;
  }, [count]);

  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```
In this example, the effect updates the document title with the current count value. The effect is triggered whenever the count state changes. The cleanup function restores the document title to its original value when the component unmounts or when the count changes.
