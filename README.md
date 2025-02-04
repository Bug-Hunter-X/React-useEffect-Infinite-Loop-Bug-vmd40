# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook. The provided `MyComponent` uses `useEffect` without specifying any dependencies, causing it to run after every render, leading to an infinite loop and performance degradation.  The solution showcases the proper use of the dependency array to control when the effect runs.

## Bug

The bug lies in the `useEffect` hook within `MyComponent`. Because no dependency array is provided, the effect runs after every render, creating a loop: the `console.log` updates, causing a re-render, triggering the `useEffect` again, and so on.

## Solution

The solution adds `[count]` as a dependency array to `useEffect`. Now, the effect only runs when the `count` variable changes, resolving the infinite loop and optimizing performance.