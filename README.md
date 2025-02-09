# React 19 StrictMode Warning: useEffect with no dependencies

This repository demonstrates a common warning encountered when using React 19's StrictMode.  The warning arises from using `useEffect` without specifying dependencies, leading to unintended side effects and potential performance issues.  This example shows the issue and provides a solution.

## Bug

The `bug.js` file contains a simple component with a `useEffect` hook that logs a message to the console. Because the effect has no dependencies, it runs after every render, causing unnecessary console output and potential performance problems within StrictMode.

## Solution

The `bugSolution.js` file demonstrates the correct way to use `useEffect`. By adding an empty dependency array (`[]`), we ensure the effect runs only once after the initial mount.