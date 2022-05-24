# REACT

React is a JavaScript library created and (mostly) maintained by Facebook (Meta).
React is a JavaScript library for building User Interfaces.

## Intro

- React is a JavaScript library for building User Interfaces.
- React is only responsible for the View layer.
- React is not a framework.

## Installation

- Install react with npm install react
- Import React in every file you need it with import React from "react"
- Get the current React version with React.version
- React weighs 7KB when imported.

## React.CreateElement

- A React Element is the smallest building block.
- It's a representation of a small piece of your UI.
- React.createElement returns a React Element
- React.createElement(type, options, children)

## ReactDOM

- ReactDOM is the glue between React and the DOM.
- ReactDOM is separate from React because you can write React for native applications.
- Reconciliation is the process of syncing the Virtual DOM to the actual DOM.
- Install ReactDOM with npm install react-dom
- Import ReactDOM's render method with import {render} from "react-dom"

## Root Element

- The root element is completely managed by ReactDOM
- You should not directly change/update the content of the root element
- Apps built with React have a single root element (Most common use case)
- Existing Apps that integrate React to make a feature interactive, could have more than 1 root.

## JSX

- JSX is a special syntax for React that makes it easier to represent your UI
- JSX looks similar to HTML but it is not HTML
- JSX code you write gets transformed into React.createElement
- JSX is not part of your browser. You need a tool to transform it to valid JavaScript.
- JSX requires React to be in scope.
- Attributes in JSX get passed as the 2nd argument of React.createElement(...)
- <div className="active"></div> is how you would give the class active to this element.
- You need quotes around attribute values that are strings.
- A JSX element is an object
- you can treat a JSX element like an object
- you can assign a JSX element to a variable
- you can return a JSX element from a function
- Use self-closing syntax for self-closing elements in JSX
- Comments in JSX use the following syntax: {/_comment_/}
- When returning nothing from a component, make sure to return null;
- Conditional rendering allows you to return different Elements based on props (or other conditions).
- Spreading attributes in JSX allows you to take all the props (or a portion of the props) and pass them down to the element being rendered without having to write all the props one by one.
- Spreading attributes is mostly used when building UI Kits.

## JSX Expressions

- An expression is any valid JavaScript code that resolves to a value
- Expressions in JSX need to be wrapped inside curly braces: {expression}
- {2 + 3} is an example an expression.
- If the value of the attribute is a string, then wrap it with quotes
- If the value of the attribute is an expression, then wrap it with curly braces {}
- Number and boolean attribute values should be passed as an expression

## JSX Children

- JSX supports children
- Always wrap your JSX elements with () when written after a return.

## JSX Fragments

- You can only return 1 element in JSX
- Wrap multiple elements with React.Fragment
- The short syntax is <> that can be closed with </>
- The original syntax is: <React.Fragment> and </React.Fragment>

## Components

- A React Component is a function that returns one React Element describing a section of the UI.
- Components defined with a function are called function components.
- React Components promote code reuse and are easier to debug.
- A React Component's name has to start with an uppercase.
- Use UpperCamelCase when naming React Components
- The first part of a JSX tag determines the type of the React element.
- Capitalized types indicate that the JSX tag is referring to a React component.
- A React Component is a function that returns a React Element.
- Define one component per file for easier maintenance.
- Make the name of the file match the name of the Component.

## clsx

- clsx is a tiny utility for constructing className strings conditionally.
- You can install clsx with npm install clsx
- clsx({"your-class-name": booleanValue}) is the generic syntax for clsx.

## State

- State refers to any variable defined inside a Component with the intent to update later on.
- State variables can be updated from inside the Component.
- When a state variable is updated, the Component automatically re-renders
- useState allows us to create a state variable in a Component
- useState is a named export that needs to be imported
- You can import useState and React: import React, {useState} from "react";
- useState is one of many React Hooks.

## useState hook

- useState is a React Hook that hooks into the internals of React and notifies it that a state variable has changed.
- The useState() function takes the initial_value as the only argument.
- The useState() function returns an array of 2 items
- Always destructure the useState into abc and setAbc where abc is the name of the state
- The default value of the state variable returned by useState will be the same as the initial_value passed to useState().
- When you change the state, React will call the Component function again to re-render
- The initial_value passed to useState(initial_value) is only used the first time a Component renders.

## Events

- onClick should only be used on <button> elements for better accessibility.
- onEventName is the general syntax for adding events to an element.
- onKeyDown attaches the keydown event to an element.
- Moving from inline to named event handlers allows for more complexity inside the event handler.
- Use the handleSubjectEvent naming convention for event handlers
- When event handlers are defined inside the Component, they can use the state variables because of the closures concept.
