# React useEffect Cleanup Function Missing

This example demonstrates a common error in React applications where the cleanup function is missing from a `useEffect` hook that adds an event listener. This can lead to memory leaks and unexpected behavior.

## Bug
The bug is in the `MyComponent` function.  The `useEffect` hook adds an event listener but doesn't provide a cleanup function to remove the listener when the component unmounts.  This means that the event listener continues to exist even after the component is no longer in the DOM, leading to potential memory leaks and unintended side effects.

## Solution
The solution involves adding a return statement to the `useEffect` hook, providing a cleanup function that removes the event listener.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the memory usage in your browser's developer tools.  The memory usage will not decrease after unmounting the component.

## How to fix
Review the `bugSolution.js` file for the corrected code.