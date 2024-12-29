# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## The Bug
The `bug.js` file contains a component that uses `useEffect` to log the current count. However, the `count` variable is not included in the dependency array.  This means the effect runs after every render, causing the component to continuously re-render and log to the console. 

## The Solution
The `bugSolution.js` file corrects the issue by adding `count` to the dependency array. Now, the effect only runs when the `count` value changes.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite logging in the console.  Then switch to the solution file and re-run.