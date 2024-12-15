# React Native State Update Bug

This repository demonstrates a common bug in React Native applications: incorrectly updating the component's state, leading to unexpected UI behavior and potential performance issues.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the correct implementation.

## Problem
Directly manipulating the `this.state` object without using `setState` will bypass React's reconciliation process and might lead to a component not re-rendering, resulting in an outdated UI.

## Solution
Always use the `setState` method to update the component's state.  `setState` is asynchronous, and calling `forceUpdate` should be avoided unless absolutely necessary.