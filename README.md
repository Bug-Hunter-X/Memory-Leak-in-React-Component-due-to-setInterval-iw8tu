# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` inside `useEffect` without proper cleanup. This leads to memory leaks because the interval continues to run even after the component unmounts.

## Bug
The `bug.js` file shows a React component that uses `setInterval` to update a count every second.  However, it lacks the cleanup function within the `useEffect` hook's return value to stop the interval when the component is unmounted.

## Solution
The `bugSolution.js` file presents the corrected code. It uses `clearInterval` in the cleanup function to stop the interval when the component unmounts, resolving the memory leak.