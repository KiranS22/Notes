# Introduction to React.js

React.js is a popular JavaScript library for building user interfaces. It allows you to create reusable UI components that efficiently update and render based on changes in application state. In this markdown file, we will cover the basics of React.js and explain how to create a React app using function components.

## Getting Started

Before we begin, make sure you have Node.js installed on your machine. React.js requires Node.js and npm (Node Package Manager) to be installed to set up a development environment.

### Step 1: Installing the Create React App CLI

To create a new React app, we'll use the Create React App CLI, which is an officially supported way to create new React projects. Open your terminal or command prompt and run the following command to install the Create React App CLI globally:

```shell
npm install -g create-react-app
```

### Step 2: Creating a New React App

Once you have the Create React App CLI installed, you can create a new React app using a single command. Run the following command in your terminal:

```shell
npx create-react-app my-app
```

Replace "my-app" with the desired name for your React app. This command will create a new directory called "my-app" (or the name you specified) and set up a new React project inside it.

### Step 3: Running the React App

After the app is created, navigate into the project directory using the following command:

```shell
cd my-app
```

To start the development server and run your React app, use the following command:

```shell
npm start
```

This command will compile your React code, start the development server, and open your app in a web browser. You should see a "Welcome to React" message displayed in the browser.

## Understanding React Components

React organizes UI elements into reusable components, which can be thought of as building blocks for your application. Components encapsulate their own logic, styles, and rendering, allowing you to build complex UIs by combining and nesting components together.

In React, function components are the recommended approach for creating components. A function component is a simple JavaScript function that accepts properties (props) as arguments and returns JSX (JavaScript XML) to define the component's structure.

Here's an example of a simple function component:

```jsx
import React from 'react';

function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

export default Greeting;
```

To use this component in other parts of your application, you can import and render it within other components. The main component that serves as the entry point of your application is typically called the "App" component.

```jsx
import React from 'react';
import Greeting from './Greeting';

function App() {
  return (
    <div>
      <h1>My React App</h1>
      <Greeting name="John" />
    </div>
  );
}

export default App;
```

In this example, we import the `Greeting` component from a separate file and render it within the `App` component. This allows us to compose our UI by combining different components together.

By importing components into the `App` component, we can create a hierarchical structure of components that represent the different parts of our application. This modular approach makes it easier to manage and reuse components throughout the app.

## Conclusion

In this markdown file, we covered the basics of React.js and explained how to create a new React app using function components. We also discussed the concept of importing components into the `App` component and creating a hierarchical structure of components.

React.js provides a flexible and efficient way to build user interfaces, and function components are the recommended
