# React useEffect Missing Dependency Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from omitting necessary dependencies in the `useEffect` dependency array, leading to unexpected behavior and, in some cases, infinite re-renders.

## Description
The initial `App.js` file contains a `useEffect` hook that updates the document title based on a counter. However, the `count` variable is missing from the dependency array. This means the effect runs after every render, regardless of changes in `count`, leading to an infinite loop of title updates.

## Solution
The `bugSolution.js` file fixes the bug by including `count` in the dependency array.  This ensures that the effect only runs when the `count` variable changes.

## How to Reproduce
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the behavior and then compare with the fix.