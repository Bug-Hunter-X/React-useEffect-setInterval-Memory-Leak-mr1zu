# React useEffect setInterval Memory Leak

This repository demonstrates a common memory leak in React applications caused by improper usage of `setInterval` within the `useEffect` hook.  The example shows how failing to clear the interval leads to a resource leak when the component unmounts.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it lacks a cleanup function in the `useEffect` hook to clear the interval when the component unmounts, resulting in a memory leak.

## Solution
The `bugSolution.js` file provides a corrected version of the component. It includes a cleanup function that uses `clearInterval` to stop the interval when the component is unmounted.