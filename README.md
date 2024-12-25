# React useEffect Hook Memory Leak

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include a cleanup function to clear intervals or timeouts. This can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a component that uses `setInterval` within `useEffect` without a cleanup function. When the component unmounts, the interval continues to run, leading to a memory leak.

## Solution
The `bugSolution.js` file provides the corrected code, including a cleanup function that uses `clearInterval` to stop the interval when the component unmounts.