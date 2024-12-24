# React useEffect Hook: Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include relevant state variables in the dependency array.  This can lead to unexpected behavior, such as infinite loops or performance issues.

## Problem

The provided `bug.js` file shows a component with a `useEffect` hook that's missing a dependency. The effect will run on every render, creating a loop as it constantly updates the console and attempts re-renders. This can cause unexpected behavior or significant performance problems in more complex applications.

## Solution

The solution, found in `bugSolution.js`, correctly includes the `count` state variable in the dependency array.  This ensures the effect only runs when the `count` value changes, as intended.  The `return` statement in the `useEffect` also cleans up resources after the effect has completed.